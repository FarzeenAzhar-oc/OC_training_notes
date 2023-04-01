#commands 

- **Get id of all containers** `docker ps -aq`
- **Remove all containers** `docker rm $(docker ps -aq)`
- Remove all images `dcoker rmi $(docker imaged -q)`