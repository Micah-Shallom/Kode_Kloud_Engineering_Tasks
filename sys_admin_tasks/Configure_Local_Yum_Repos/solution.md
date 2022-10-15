1. SSH into the backup server

        ssh clint@stbkp01
        sudo su -

2. Ideally we would have needed to use the `createrepo` command to create a package repository but in this case, it has already been spun up as `/packages/downloaded_rpms/`. Hence we need to create a repository in `/etc/yum.repos.d`

        vi /etc/yum.repos.d/local_yum.repo

3. Inside the editor mode, write the following configurations

         [local_yum] <------- repository ID
         name = local_yum
         baseurl = file:///packages/downloaded_rpms
         gpgcheck = 0
         enabled = 1

    :wq

4.  Check if the repository has been created

        yum repolist all

5. Install the wget package present in `/packages/downloaded_rpms/`

        yum install -y wget