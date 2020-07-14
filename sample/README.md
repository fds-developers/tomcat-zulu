# tomcat9 - azul openjdk11

https://localhost:8080/

## build docker image

container image : sample

container : sample

```
docker build -t sample:0.0.1 .

docker run --rm -it -p 8080:8080 --name sample sample:0.0.1
```

### connect to container

```
docker exec -it sample /bin/bash
```

```
docker pull fds/tomcat:9-zuluopenjdk11
docker exec -it fds/tomcat:9-zuluopenjdk11 /bin/bash
```
