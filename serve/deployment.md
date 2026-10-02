# Deployment

## Table of content

1. [Create a folder to deploy](#create-a-folder-to-deploy)
2. [Deploy](#deploy)
3. [Install PostgreSQL](#install-postgresql)

## Create a folder to deploy

1. Connect to the server
    ```sh
    ssh {user}@{server_ip_address}
    ```
2. Create the app directory
    ```sh
    sudo mkdir /opt/{app_name}
    ```

## Deploy

1. Copy the jar file to the server
    ```sh
    scp target/{app_name}-{version}.jar {user}@{server_ip_address}:/home/{user}
    ```
2. Copy the jar file to the `/opt` folder
    ```sh
    sudo cp /home/{user}/{app_name}-{version}.jar /opt/{app_name}
    ```

## Install PostgreSQL

1. Pull the Docker image
    ```sh
    docker pull postgres:18
    ```
2. Run the container
    ```sh
    sudo docker run -itd \
    -e POSTGRES_USER={db_user} \
    -e POSTGRES_PASSWORD={db_password} \
    -p 5432:5432 \
    -v /data:/var/lib/postgresql/data \
    --name postgresql postgres:18
    ```
3. Install the psql client
    ```sh
    sudo apt install postgresql-client
    ```
4. Configure the PostgreSQL repository (for more information
   see https://www.postgresql.org/download/linux/ubuntu/)
    ```sh
    sudo /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh
    ```
5. Connect to the database
    ```sh
    psql -h 127.0.0.1 -U {db_user} -d {db_name}
    ```
