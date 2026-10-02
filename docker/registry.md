# Docker Registry

## Table of content

1. [Login](#login)
2. [Tag an image](#tag-an-image)
3. [Push an image](#push-an-image)
4. [Pull an image](#pull-an-image)

## Login

1. Login to Docker Hub
    ```sh
    docker login
    ```
2. Login to a private registry
    ```sh
    docker login {registry_url}
    ```

## Tag an image

1. Tag a local image so it can be pushed to a registry
    ```sh
    docker tag {image_name}:{tag} {registry_url}/{project_name}/{image_name}:{tag}
    ```

## Push an image

1. Push an image to a registry
    ```sh
    docker push {registry_url}/{project_name}/{image_name}:{tag}
    ```

## Pull an image

1. Pull an image from a registry
    ```sh
    docker pull {registry_url}/{project_name}/{image_name}:{tag}
    ```
