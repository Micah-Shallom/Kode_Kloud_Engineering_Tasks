1. ssh banner@stapp03
2. sudo su -
3. vi /etc/httpd/conf.d/main.conf
4. add the following
   ``` <VirtualHost *:6100>

ServerName stapp02.stratos.xfusioncorp.com

Redirect 301 / http://www.stapp02.stratos.xfusioncorp.com:6100/

</VirtualHost>

 

<VirtualHost *:6100>

ServerName www.stapp02.stratos.xfusioncorp.com:6100/blog/

Redirect 302 /blog/ http://www.stapp02.stratos.xfusioncorp.com:6100/news/

</VirtualHost>
```

5. vi /etc/httpd/conf/httpd.conf
6. Change Listen to Listen 6100
7. systemctl restart httpd
8. systemctl status httpd