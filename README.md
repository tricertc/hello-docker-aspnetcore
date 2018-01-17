# Hello Docker

## Build your image and run a container

```
docker build -t hello-docker-aspnetcore .
docker run --name hello-docker-aspnetcore-1 -p "5000:80" -d hello-docker-aspnetcore
```

Then go to http://localhost:5000 in your browser.

### View logs

```
docker logs hello-docker-aspnetcore-1
```

### Access the shell
```
docker exec -it hello-docker-aspnetcore-1 sh
```

Type **exit** to leave shell

### Stop the running container

```
docker stop hello-docker-aspnetcore-1
```

### Cleanup the container and image

Stop the container first if it is running.

```
docker rm hello-docker-aspnetcore-1
docker rmi hello-docker-aspnetcore
```