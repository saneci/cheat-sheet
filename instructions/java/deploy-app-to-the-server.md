## Table of content

1. [Header 1](#header-1)
2. [Header-2](#header-2)


### Build

1. Step1
    ```sh
    
    ```
2. Step2
    ```sh
    
    ```


### Create folder to deploy

1. Connect to the server
    ```sh
     ssh booklibrary@109.71.247.10
    ```
2. Create app directory
    ```sh
    sudo mkdir /opt/booklibrary
    ```

   
### Deploy

1. Copy jar file to the server
    ```sh
    sudo scp target/book-library-1.1.0.jar booklibrary@109.71.247.10:/home/booklibrary
    ```
2. Copy jar file to `/otp` folder
    ```sh
    sudo cp /home/booklibrary/book-library-1.1.0.jar /opt/booklibrary
    ```

### Install PostgreSQL

1. Pull Docker image
    ```sh
    docker pull postgres:16
    ```
2. Run container
    ```sh
    sudo docker run -itd \
    -e POSTGRES_USER=booklibrary \
    -e POSTGRES_PASSWORD=booklibrary \
    -p 5432:5432 \
    -v /data:/var/lib/postgresql/data \
    --name postgresql postgres
    ```
3. Install psql client
   ```sh
   sudo apt install postgresql-client
    ```
4. Configure PostgreSQL repository (for more information see https://www.postgresql.org/download/linux/ubuntu/)
   ```shell
   sudo /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh
   ```
5. Connect to the database
   ```sh
   psql -h 127.0.0.1 -U posgresql -d posgresql
   ```




3. 
   ```sh
   
   ```