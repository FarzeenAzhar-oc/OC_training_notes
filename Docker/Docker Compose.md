#commands 
- For running multiple docker containers
- In [Docker Network](Docker%20Network.md) we manually called run each time for different components, this process can be automated using [Docker Compose](.md)
-  We map the commands in a .yaml file, for more info check [tutorial on yaml](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) and [docker yaml specs](https://docs.docker.com/compose/compose-file/) for more specific info on yaml in docker compose.
- **Plus point!!!** you don't have to create a network, docker compose does it for you.

## Using Docker Compose 
`docker-compose -f <file name> up`
`-f ` to specify file
`up` to specify to start all containers in yaml

- NOTE: you can configure wait logic

- Containers aren't persistent, i.e each time you restart container, data is lost. To prevent this one can use [Docker Volume](Docker%20Volume.md)

# Stop in docker compose

```
docker-compose -f <file-name> down
```