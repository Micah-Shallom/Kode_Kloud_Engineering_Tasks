1.  SSH into appserver

        ssh tony@stapp01

2.  Install crontie and start the crond service

        yum install -y cronie 
        systemctl start crond.service
        systemctl status crond.service

3.  Check to see if there is a preexisting crontab setup

        crontab -u root -l

4.  Add the crontab configuration from the task

        crontab -e

5.  Paste the config into the editor

        */5 * * * * echo hello > /tmp/cron_text

6.  Watch the temp repository for 5mins to see the creation of the cron_text file

        watch -n 5 ls /tmp

7.  Repeat for appserver 2 and 3