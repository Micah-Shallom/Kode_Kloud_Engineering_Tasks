1. SSH into app server

        ssh tony@stapp01

2. Check user

        id tony

3. Move into root user

        sudo su -

4. Edit sudoers 

        visudo

    ```
    tony ALL=(ALL) NOPASSWD=NO
    ```

    