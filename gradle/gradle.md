# Gradle commonly used commands

## Table of content

1. [Manage daemons](#manage-daemons)
2. [Build the application](#build-the-application)
3. [Run the application](#run-the-application)
4. [Resolve problems](#resolve-problems)

## Manage daemons

1. Stop Gradle daemons
    ```sh
    ./gradlew --stop
    ```

## Build the application

1. Build the app
    ```sh
    ./gradlew clean build
    ```

## Run the application

1. Run the server with the active profile set to `dev`
    ```sh
    ./gradlew bootRun --args='--spring.profiles.active=dev'
    ```

## Resolve problems

1. Replace `CRLF` characters (saved in Windows) with `LF` so Bash can read and execute the script
    ```sh
    sed -i -e 's/\r$//' {script_name}.sh
    ```
2. Make `gradlew` executable and add the change to the Git repository
    ```sh
    git update-index --chmod=+x gradlew
    ```
