1. SSH into the server

        ssh tony@stapp01

2. Edit your Apache server configuration file

        vi /etc/httpd/conf/httpd.conf

3. Add the following to the configuration file

        ServerTokens Prod
        ServerSignature Off

To Disable Directory Browsing on Apache

4. Edit httpd configuration file

        vi /etc/httpd/conf/httpd.conf

5.  Find the line

        Options Indexes FollowSymLinks

and remove Indexes from that line or replace with -Indexes

        Options FollowSymLinks