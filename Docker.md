## Stop & Remove all Containers
```bash
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

## Remove dangling volumes
```bash
docker volume prune
```

## Remove all secrets
```bash
docker secret rm $(docker secret ls -q)
```

## Remove any stopped containers and all unused images
```bash
docker system prune -a
```

## Remove all images
```bash
docker rmi $(docker images -a -q)
```

## Remove all services
```bash
docker service rm $(docker service ls -q)
```


## Add Env Variable to Docker Service
```bash
docker service update --env-add <you environment variable> <service_name>
```
