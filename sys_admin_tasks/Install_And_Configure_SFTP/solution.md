=============
    1  useradd anita
    2  passwd anita
    3  mkdir -p /var/www/web
    4  ll -lsd /var/www/web
    5  chown root:root  /var/www
    6  chmod -R 755 /var/www
    7  ll -lsd /var/www/
    8  vi /etc/ssh/sshd_config
    9  systemctl restart sshd
   10  systemctl status sshd
