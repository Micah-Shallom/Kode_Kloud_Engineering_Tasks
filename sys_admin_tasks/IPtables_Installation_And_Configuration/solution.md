1. SSH into application server
   
        ssh tony@stapp01
        sudo su -

2. Install Iptables services

        yum install -y iptables-services

3. Start and enable iptables 

        systemctl start iptables 
        systemctl enable iptables

4. Add Iptable rules

        iptables -A INPUT -p tcp --destination-port 8088 -s 172.16.238.14 -j ACCEPT
        iptables -A INPUT -p tcp --destination-port 8088 -j DROP

5. Save IPTables config

        service iptables save

6. Restart iptables services

    systemctl restart iptables


7. Repeat on the other 2 webservers