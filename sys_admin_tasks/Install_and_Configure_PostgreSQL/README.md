The Nautilus application development team has shared that they are planning to deploy one newly developed application on Nautilus infra in Stratos DC. The application uses PostgreSQL database, so as a pre-requisite we need to set up PostgreSQL database server as per requirements shared below:



a. Install and configure PostgreSQL database on Nautilus database server.

b. Create a database user kodekloud_gem and set its password to YchZHRcLkL.

c. Create a database kodekloud_db10 and grant full permissions to user kodekloud_gem on this database.

d. Make appropriate settings to allow all local clients (local socket connections) to connect to the kodekloud_db10 database through kodekloud_gem user using md5 method (Please do not try to encrypt password with md5sum).

e. At the end its good to test the db connection using these new credentials from root user or server's sudo user.