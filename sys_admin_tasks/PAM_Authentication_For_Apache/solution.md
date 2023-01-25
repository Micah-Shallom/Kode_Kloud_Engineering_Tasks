1. SSH into server

        ssh tony@stapp01
        sudo su -

2. Install pwauth package

          yum --enablerepo=epel -y install mod_authnz_external pwauth 

3. Edit the configuration file and add the following

            vi /etc/httpd/conf.d/authnz_external.conf
            ```
            <Directory /var/www/html/protected>

            AuthType Basic

            AuthName "PAM Authentication"

            AuthBasicProvider external

            AuthExternal pwauth

            require valid-user

            </Directory>
            ```

4. Create protected directory

        mkdir -p /var/www/html/protected

5. Start httpd service and try to connect to it

        systemctl start httpd

        curl -u mark:8FmzjvFU6S http://localhost:8080/protected