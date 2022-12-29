1. SSH into required server

        ssh tony@stapp01
        sudo su -

2. Update daemon and Install squid and logrotate 

        yum update -y && yum install squid logrotate -y

3. Update logrotate configuration

        cd /etc/logrotate.d/squid

        change `weekly` to `monthly`
        update rotation from `5` to `3`