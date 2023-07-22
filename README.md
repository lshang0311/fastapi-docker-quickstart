# Deploy with docker compose

- From the root folder `fastapi`, run
```commandline
docker-compose up -d --build
```
- List the containers
```commandline
docker ps
```

Output:
```text
CONTAINER ID   IMAGE         COMMAND       CREATED              STATUS              PORTS                                               NAMES
59329b5986a4   fastapi_api   "/start.sh"   About a minute ago   Up About a minute   80/tcp, 0.0.0.0:8000->8000/tcp, :::8000->8000/tcp   fastapi-application

```

- Navigate to http://localhost:8000 in the web browser find the following json response:
```text
{
"message": "OK"
}
```

# FastAPI and Docker Quick Start

- Slightly modified from [awesome-compose/fastapi](https://github.com/docker/awesome-compose/tree/master/fastapi)

- Also see [FastAPI in Containers - Docker](https://fastapi.tiangolo.com/deployment/docker/)

# Destroy ALL

* Stop and remove all running containers:

```commandline
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
```

* To forcefully remove all Docker images

```commandline
docker rmi --force $(docker images -q)
```

* Remove all Docker volumes:

```commandline
docker volume prune
```



