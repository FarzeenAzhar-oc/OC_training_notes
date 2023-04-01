#commands 
- Docker creates isolated docker networks inside the host where the containers are running in.
-  Scenario: Two docker containers in the same network
	- They don't need local host, port etc
	- They only need the container names/ids to talk to each other
	- An outside application will connect to docker isolated network using localhost:<port number\> 

**See docker network** `docker network`
**Create Network** `docker network create <network name>`
- Add environmental variables to configure specific files with option `-e`
- You can utilise the docker page of image in docker hub to see options while running, i.e the network and other 

```console
docker run -d -p27017:27017 --network mongo-network --name mongodb \
	-e MONGO_INITDB_ROOT_USERNAME=admin \
	-e MONGO_INITDB_ROOT_PASSWORD=passwd \
	mongo
```

To run multiple docker containers see [Docker Compose](Docker%20Compose.md)