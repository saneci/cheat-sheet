# Gradle commonly used commands


## Table of content

1. [Manage daemons](#manage-daemons)
2. [Gradle workflow](#gradle-workflow)
3. [Resolve problems](#resolve-problems)


### Manage daemons

- `./gradlew --stop` - stop Gradle daemons


### Gradle build

- `./gradlew clean build` - build app


### Run Gradle application

- `./gradlew bootRun --args='--spring.profiles.active=dev'` - to run server with active profile set to `dev`


### Resolve problems

- `sed -i -e 's/\r$//' <script_name.sh>` - command will replace `CRLF` (saved in Windows) characters with nothing,
  which will leave these lines with `LF` (\n) as the ending, and Bash will be able to read and execute the file
  by running `<script_name.sh>`
- `git update-index --chmod=+x gradlew` - do gradlew as executable and add to Git repository