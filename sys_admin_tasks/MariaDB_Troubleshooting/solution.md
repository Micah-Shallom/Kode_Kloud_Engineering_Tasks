1. SSH into server

    ssh peter@stdb01
    sudo su -

2. Start mariadb service
    
    systemctl start mariadb

3.  Check complete status of failed mariadb service

        systemctl status mariadb -l

4. Check the logs
        
         cat /var/log/mariadb/mariadb.log 

5. Check the permissions 
        
        ll /var/run/mariadb/ -a

6. Change permission to allow all

        chmod -R 777 /var/run/mariadb
        
7. Restart mariadb

        systemctl restart mariadb