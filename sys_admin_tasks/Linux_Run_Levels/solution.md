1. SSH into the server

        ssh tony@stapp01
        sudo su -

2. Check the current linux run level

        systemctl get-default


3. Change the multilevel-target to graphical target

        systemctl set-default graphical.target

4. submit