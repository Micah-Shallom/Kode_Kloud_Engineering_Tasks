We have a backup management application UI hosted on Nautilus's backup server in Stratos DC. That backup management application code is deployed under Apache on the backup server itself, and Nginx is running as a reverse proxy on the same server. Apache and Nginx ports are 5001 and 8095, respectively. We have iptables firewall installed on this server. Make the appropriate changes to fulfill the requirements mentioned below:



We want to open all incoming connections to Nginx's port and block all incoming connections to Apache's port. Also make sure rules are permanent.