1. SSH into App server 3

        ssh banner@stapp03
        sudo su -

2. Checking files and folders

        ll /home/usersdata


3.  find the files name by user & copy with folder structure 

        find /home/usersdata/ -type f -user ravi -exec cp --parents {} /ecommerce \;


4. List the files copied in the destination folder 

        ll /ecommerce/home/usersdata