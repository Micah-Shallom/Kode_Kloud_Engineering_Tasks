1.  SSH into app server 2

        ssh steve@stapp02
        sudo su -

2.  Update, install epel repository and nginx

        yum update -y
        yum install -y epel-release
        yum install -y nginx

3.  Start and enable service

        systemctl start nginx
        systemctl enable nginx
        systemctl status nginx

4.  Unlink the index.html symbolic link/delete it

        cd /usr/share/nginx/html
        unlink index.html

5.  Create a new one and add welcome

        vi index.html ---> Welcome!

6.  Copy crt and key into html folder

        cp /tmp/nautilus.* .

7.  Configure nginx server

        vi /etc/nginx/nginx.conf

        # introduce into the "server" section
        server {
            listen       80 default_server;
            listen       [::]:80 default_server;
            listen       443 ssl;                ----->>>>>>ADD THIS LINE
            server_name  172.16.238.12;          ----->>>>>>HERE ADD IP ADDRESS OF SERVER2
            root         /usr/share/nginx/html;
            index        index.html              ------>>>>>>ADD THIS LINE
            ssl_certificate      /usr/share/nginx/html/nautilus.crt;
            ssl_certificate_key  /usr/share/nginx/html/nautilus.key;    


8.  Restart
        systemctl restart nginx


9. CURL appserver 2 from the jumphost

        thor@jump_host /$ curl -Ik https://172.16.238.12/



