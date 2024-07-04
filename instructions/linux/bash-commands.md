## Table of content

1. [Update packages](#update-packages)
2. [Restart system](#restart-system)
3. [Read logs](#read-logs)
4. [Create folders](#create-folders)


### Update packages

- Update packages
    ```sh
    sudo apt install
    ```
- Show what should to be updated (or have been updated)
    ```sh
    apt list --upgradable
    ```
- Upgrade packages
    ```sh
    sudo apt upgrade 
    ```


### Restart system

1. Restart now
    ```sh
    sudo shutdown -r now
    ```
2. Step2
    ```sh
        
    ```


### Read logs

- Read logs forever (until interrupt manual)
    ```shell
    tail -f ~/logs/book-library-1.1.1-log.txt
    ```
  

### Create folders

- `mkdir /home/<dir_name>` - 
