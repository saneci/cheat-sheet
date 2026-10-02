# Commonly used Docker Compose commands

## Table of content

1. [Build and run services](#build-and-run-services)
2. [Manage services](#manage-services)

## Build and run services

1. Build docker images and run services specified in the docker-compose.yaml file
    ```sh
    docker compose up --build
    ```
2. Stop services and remove images
    ```sh
    docker compose down
    ```

## Manage services

1. Show running services
    ```sh
    docker compose ps -a
    ```
2. Run a service
    ```sh
    docker compose run {service_name}
    ```
3. Stop a service
    ```sh
    docker compose stop {service_name}
    ```
