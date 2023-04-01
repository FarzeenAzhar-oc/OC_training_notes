## Basics of container

#commands

- Container is a running enviroment for IMAGE
- Runs on port 5000
- Port binding: talk to app running inside of container
- Container has virtual file system

## Access containers
- Using port
- See [Container Port vs HOST post](Container%20Port%20vs%20HOST%20post.md)
## Commands

- **Pull**: ```docker pull <image>```
- **Pull version** : ```docker pull <image> : <version>```
- **Check all existing images** ```docker image ls```
- **Create Container** ```docker run <image> ```
- **Create Container  with detach terminal** ```docker run -dt <image> ```
- **Check running container** ```docker ps```
- **Stop container** ```docker stop <container id>```
- **List running and stopped containers** ```docker ps -a```
- **Port binding** ```docker run -p<host port >:<docker port>```
- **Remove docker image** `docker rmi <image tag>`
Now see [Debugging containers](Debugging%20containers.md)

Also see [docker run vs dcker start](docker%20run%20vs%20dcker%20start.md)


