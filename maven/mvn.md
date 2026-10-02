# Maven commonly used commands

## Table of content

1. [Wrapper installation](#wrapper-installation)
2. [Commonly used commands](#commonly-used-commands)

## Wrapper installation

Official documentation: [Maven Wrapper plugin](https://maven.apache.org/wrapper/maven-wrapper-plugin)

1. Go to the main folder of the project and run this command
    ```sh
    mvn -N wrapper:wrapper
    ```
2. Specify the version of Maven to install (3.10.0 at the time of writing)
    ```sh
    mvn -N wrapper:wrapper -Dmaven=3.10.0
    ```

## Commonly used commands

1. Build the project (as a result an executable jar file will be created)
    ```sh
    mvn clean package
    ```
