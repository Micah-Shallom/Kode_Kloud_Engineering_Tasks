We have a requirement where we want to password protect a directory in the Apache web server document root. We want to password protect http://<website-url>:<apache_port>/protected URL as per the following requirements (you can use any website-url for it like localhost since there are no such specific requirements as of now). Setup the same on App server 3 as per below mentioned requirements:



a. We want to use basic authentication.

b. We do not want to use htpasswd file based authentication. Instead, we want to use PAM authentication, i.e Basic Auth + PAM so that we can authenticate with a Linux user.

c. We already have a user mark with password 8FmzjvFU6S which you need to provide access to.

d. You can access the website using APP button on the top bar.