# Commonly used Docker commands

## Table of content

1. [Build an image](#build-an-image)
2. [Run a container](#run-a-container)
3. [Connect to a container](#connect-to-a-container)
4. [Manage volumes](#manage-volumes)

## Build an image

1. Build an image with a build argument
    ```sh
    docker build --build-arg JAR_FILE=target/*.jar -t {project_name}/{image_name} .
    ```
2. Build an image with the JAR file location hardcoded in the Dockerfile
    ```sh
    docker build -t {project_name}/{image_name} .
    ```
3. Build a new image using the test stage as the target and view the test results.
   Include `--progress=plain` to view the build output, `--no-cache` to ensure the tests always run,
   and `--target=test` to target the test stage.
    ```sh
    docker build -t {project_name}/{image_name} --progress=plain --no-cache --target=test .
    ```

## Run a container

1. Run the application in Docker
    ```sh
    docker run --name {container_name} -p 8080:8080 {project_name}/{image_name}
    ```
2. Start an existing container
    ```sh
    docker start {container_name}
    ```

## Connect to a container

1. Open a shell in a new container
    ```sh
    docker run -it --entrypoint /bin/sh {project_name}/{image_name}
    ```
2. Open a shell in a running container
    ```sh
    docker exec -it {container_name} /bin/sh
    ```

## Manage volumes

1. Show volumes
    ```sh
    docker volume ls
    ```
2. Remove a volume
    ```sh
    docker volume rm {volume_name}
    ```
