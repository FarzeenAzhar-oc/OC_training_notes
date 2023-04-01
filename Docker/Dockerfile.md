#commands 
## A rough description of how everything works in industry
1. You create app locally
2. Push to git
3. Jenkins builds app and creates docker image
4. Pushes to Docker Repository

## What is a Dockerfile?
- Blueprint for creating  building images 


## Dockerfile syntax

| Image Env Blueprint | Dockerfile |
| ---- | ----|
| install image | `FROM <image>` |
| set env1=a \n set env2=b| `ENV env1=a \n env2=b`|
| run a linux command in container | `RUN <linux command>`|
| copy host file to container | `COPY <host path> <container path>`|
| start app with command | `CMD ['command', 'app']`|

### RUN vs CMD
CMD is an entry point command. Only one CMD.

```
docker build -t <app name>:<tag> <docker directory>
```

This whole process is stimulated by [jenkins](jenkins.md).