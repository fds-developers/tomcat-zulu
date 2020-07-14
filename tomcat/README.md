# tomcat 9 on azul/zulu-openjdk11

see https://hub.docker.com/r/azul/zulu-openjdk

see https://hub.docker.com/_/tomcat

see https://github.com/docker-library/tomcat/blob/master/9.0/jdk11/openjdk/Dockerfile

https://localhost:8080/

## build docker image

container image : fds/tomcat

container : zulutomcat11

```
docker build -t fds/tomcat:9-zuluopenjdk11 .

docker run --rm -it -p 8443:8443 -p 9090:8080 --name tomcat9zulu11 fds/tomcat:9-zuluopenjdk11
```

### connect to container

```
docker exec -it tomcat9zulu11 /bin/bash
```

```
docker pull azul/zulu-openjdk:11
docker exec -it azul/zulu-openjdk:11 /bin/bash
```
