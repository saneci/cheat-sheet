# Bash commonly used commands

## Table of content

1. [Update packages](#update-packages)
2. [Restart the system](#restart-the-system)
3. [Read logs](#read-logs)
4. [Create folders](#create-folders)

## Update packages

1. Refresh the list of available packages
    ```sh
    sudo apt update
    ```
2. Show what should be updated (or have been updated)
    ```sh
    apt list --upgradable
    ```
3. Upgrade packages
    ```sh
    sudo apt upgrade
    ```

## Restart the system

1. Restart now
    ```sh
    sudo shutdown -r now
    ```

## Read logs

1. Follow the log output (until it is interrupted manually)
    ```sh
    tail -f ~/{app_dir}/logs/{app_name}.log
    ```

## Create folders

1. Create a folder
    ```sh
    mkdir /home/{dir_name}
    ```
2. Create a folder with nested subfolders
    ```sh
    mkdir -p /home/{dir_name}/{sub_dir_name}
    ```
