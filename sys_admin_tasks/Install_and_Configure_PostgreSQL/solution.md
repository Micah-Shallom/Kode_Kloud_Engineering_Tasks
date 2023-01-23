1. SSH into the database server

        ssh peter@stdb01
        sudo su -

2.  - Add the PostgreSQL repository to your system by running the command
    
            sudo yum install https://download.postgresql.org/pub/repos/yum/reporpms/EL-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm

    - Update your system's package list by running the command 


            sudo yum update


    - Install PostgreSQL by running the command:
    
            sudo yum install postgresql12-server


    - Initialize the database by running the command:


            sudo /usr/pgsql-12/bin/postgresql-12-setup initdb


    - Start the PostgreSQL service by running the command


            sudo systemctl start postgresql-12


    - Enable the PostgreSQL service to start automatically at boot by running the command


            sudo systemctl enable postgresql-12


3.  - Log in to the PostgreSQL prompt by running the command


            sudo -u postgres psql


    - Create a new database with the following command


            CREATE DATABASE kodekloud_db10;

    4.  Log in to the PostgreSQL prompt by running the command
   
            sudo -u postgres psql

    - Create a new user with the following command: 


            CREATE USER kodekloud_gem WITH PASSWORD 'YchZHRcLkL';
    - Grant the new user the necessary privileges on the database

            GRANT ALL PRIVILEGES ON DATABASE kodekloud_db10 TO kodekloud_gem;
            ALTER USER kodekloud_gem WITH PASSWORD 'YchZHRcLkL';

4.  - To configure local clients to connect to a PostgreSQL database using a database user with the md5 authentication method, you can edit the pg_hba.conf file.

    - Open the pg_hba.conf file with a text editor: 


            sudo nano /var/lib/pgsql/12/data/pg_hba.conf

    - Find the line that starts with "local" and ends with "peer" or "ident" and change it to "md5"
        ```
        # "local" is for Unix domain socket connections only
        local   all             all                                     md5
        ```
    - Save and close the file.
    - Reload the PostgreSQL server to apply the changes by running the following command


            sudo systemctl reload postgresql-12