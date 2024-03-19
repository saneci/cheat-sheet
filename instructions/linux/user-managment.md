## Table of content

1. [Add user](#add-user)
2. [Disable root access](#disable-root-access)
3. [Other commands for managing users](#other-commands-for-managing-users)


### Add user

1. Add user 
    ```sh
    adduser {username}
    ```
2. Add user to `sudo` group 
    ```sh
    usermod -aG sudo {username}
    ```
3. Login using new user
    ```sh
    su - {username}
    ```
4. Add a copy of your local public key to the new user's file
    ```sh
    cp -r ~/.ssh /home/{username}
    ```
5. Set username to be the owner of this directory (a group with the same name will also be created)
    ```sh
    chown -R {username}:{username} /home/{username}/.ssh
    ```
6. Login to the server as a new user without using a password
    ```sh
    ssh {username}@{server_ip_address}
    ```


### Disable root access

1. Open file `/etc/ssh/sshd_config`
    ```sh
    sudo nano /etc/ssh/sshd_config
    ```
2. Find the line `PermitRootLogin` and replace its current value with `PermitRootLogin no`
3. Exit the editor and save the changes with keyboard combination `Ctrl X -> Y -> Enter`
4. Restart the SSH service
    ```sh
    sudo service ssh restart
    ```


### Other commands for managing users

1. If you need to add a user to another group, it must first be created
    ```sh
    groupadd {group_name}
    ```
2. Then you can create a user as follows
    ```sh
    useradd -g {group_name} {username}
    ```
3. If the user already exists, you can add him to the desired group with the `usermod` command
    ```sh
    usermod -G {group_name} {username}
    ```
4. To change the user's primary group, use the `-g` switch
    ```sh
    usermod -g {group_name} {username}
    ```
5. To change the user's home directory, use the command
    ```sh
    usermod -d path/to/new/directory {username}
    ```
6. You can get information about the user with the command
    ```sh
    id {username}
    ```
7. You can change the password with the command
    ```sh
    passwd {username}
    ```
8. View a list of all created users
    ```sh
    cat /etc/passwd
    ```
9. Get only a list of names, without additional information
    ```sh
    sed 's/:.*//' /etc/passwd
    ```
10. You can display a list of users who are currently logged in with a simple command
    ```sh
    w
    ```
11. Delete user
    ```sh
    deluser {username}
    ```
12. Delete user group
    ```sh
    delgroup {group_name}
    ```
