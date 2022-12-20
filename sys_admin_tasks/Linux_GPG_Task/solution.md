1. SSH into storage server

    ssh natasha@strstapp01

2. Import Public and Private keys into gpg keyrings

    gpg --import public_key.asc
    gpg --import private_key.asc

3. Encrypt the file

    gpg --encrypt -r kodekloud@kodekloud.com --armor < encrypt_me.txt  -o encrypted_me.asc

4. Decrypt the file 

    gpg --decrypt decrypt_me.asc > decrypted_me.txt