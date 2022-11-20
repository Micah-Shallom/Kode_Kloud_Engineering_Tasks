1. SSH into server

      ssh steve@stapp02
      sudo su -

2. Find and copy into /blog

      find /var/www/html/blog -type f -name '*.js' -exec cp --parents {} /blog \;