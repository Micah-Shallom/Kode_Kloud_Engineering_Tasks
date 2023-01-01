1.  SSH into the backup server
```
        ssh clint@stbkp01
        sudo su -
```
2.  Add IPTable rules to allow connection to nginx port and IPTable rule to reject connection to apache port
```
        iptables -A INPUT -p tcp --dport 8085 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT

        iptables -A INPUT -p tcp --dport 5001 -m conntrack --ctstate NEW -j REJECT

```
3.  Start the iptables service
```
        systemctl start iptables
        systemctl restart iptables
```
4.  Save the iptable rules to ensure firewall configuration persistence
```
        service iptables save
```

5.  View Iptable rules
```
        iptables -L
```

6.  Test Firewall configuration by connection to nginx port from the jumpbox server     
```
        ping stbkp01:8085
```