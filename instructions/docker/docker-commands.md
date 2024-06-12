## Commonly used Docker commands

### Table of content

1. [Header 1](#header-1)
2. [Header-2](#header-2)


### Build and run

* запуск с аргументом
    ```sh
    docker build --build-arg JAR_FILE=target/*.jar -t saneci/book-library .
    ```
* запуск с захордкоженым в Dockerfile расположением jar-файла
    ```sh
    docker build -t saneci/book-library .
    ```
- запустить приложение в докере
    ```sh
    docker run --name app -p 8080:8080 saneci/book-library
    ```
- start container
    ```sh
    docker start app
    ```
- Run the following command to build a new image using the test stage as the target and view the test results.
  Include `--progress=plain` to view the build output, `--no-cache` to ensure the tests always run,
  and `--target-test` to target the test stage.
  ```shell
  docker build -t {project_name}/{image_name} --progress=plain --no-cache --target=test .
  ```


### Connect to container

- Open a shell
    ```sh
    docker run -it --entrypoint /bin/sh {project_name}/{image_name}
    ```
- If you have a running container, and you want to peek into it
    ```sh
    docker exec -it app /bin/sh
    ```


### Volumes

- Show
    ```sh
     docker volume ls
    ```
- Remove
    ```sh
    docker volume rm {volume_name}
    ```
