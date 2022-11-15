1. SSH into app server 3

       ssh banner@stapp03
       sudo su -


2. Install httpd
   
        yum install -y httpd


3. Change httpd port

        vi /etc/httpd/conf/httpd.conf

        change
            ` Listen 8086`
            ```
            Header set X-XSS-Protection "1; mode=black"
            Header always append X-Frame-Options SAMEORIGIN
            Header set X-Content-Type-Options nosniff
            ```

4. Start the service

        systemctl start httpd
        systemctl status httpd