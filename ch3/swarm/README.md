# Docker Swarm

## make docker-compose.yml

## management cluster
* enable swarm mode. output join token.
```
$ docker container exec -it manager docker swarm init
```
* register worker on swarm cluster
```
$ docker container exec -it worker01 docker swarm join --token {token}
```

* develop overlay network
```
docker container exec -it manager docker network create --driver=overlay --attachable {app_name}
```
