# **Basic docker test**

###### **Running app in Docker with few useless params**

`docker run -d --name boot_greeting_docker -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=reallyStrongPwd123' -p 8080:8080 rands7/docker-demo-springboot-greetings-project:latest`

maybe add `restart=always`

##### Url to test how it is working:

http://localhost:8080/greeting?name=User

##### Commands to build and push image:

- `mvn clean package docker:build`

- `mvn clean package docker:push`

##### Reminder just for me, maybe will be useful for someone else

###### Don't forget to update:

- todo's in pom.xml - set your data
- in case of issues go to ~/.docker -> rename/detele config.json
- pom -> maven -> open settings.xml -> add following server, and comment others

`<server>
    <id>docker.io</id>
    <username>login/username>
    <password>password</password>
</server>`

#### Other

- COPY / auth issue -> Docker logout may help

- Useful video guide: https://www.youtube.com/watch?v=YR06dGM5pWk

- App example from: https://spring.io/guides/gs/rest-service/

###### Some useful commands

- `docker images`
- `docker image rm <hash>`


