1. SSH into the server

        ssh tony@stapp01
        sudo su -

2. Check if the httpd status is running

        systemctl status httpd

3. Start the service
   
        systemctl start httpd && systemctl enable httpd

4. Check the cause of error and see the current running process obstructing apache port

        lsof -i :5004

5. Identify the process and kill it

        kill -9 PID

6. Restart httpd process

        systemctl restart httpd
        
completed
