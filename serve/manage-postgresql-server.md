# Manage PostgreSQL server

Initialize, start, stop, or control a PostgreSQL server
([official documentation](https://www.postgresql.org/docs/current/app-pg-ctl.html))

## Table of content

1. [Stop](#stop)
2. [Start](#start)

## Stop

1. Run cmd with admin permissions
2. Go to the PostgreSQL binary folder
    ```cmd
    cd C:\Program Files\PostgreSQL\18\bin
    ```
3. Stop the PostgreSQL server
    ```cmd
    pg_ctl stop -D ../data
    ```

## Start

1. Run cmd with admin permissions
2. Go to the PostgreSQL binary folder
    ```cmd
    cd C:\Program Files\PostgreSQL\18\bin
    ```
3. Start the PostgreSQL server
    ```cmd
    pg_ctl start -D ../data
    ```
