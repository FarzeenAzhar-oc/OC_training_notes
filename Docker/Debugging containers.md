#commands 

**See logs** ```docker logs <conatiner id/ container name>```
`-f` to stream logs
- Container name: when container is created it gets a random name, one can give there own name as well
		- **Give name to docker** ```docker run --name <name> <image>```

# Docker exec

**Run terminal within docker container** ```docker exec -it <container id\ container name> <commd argumetns>```

`it` for interactive terminal 