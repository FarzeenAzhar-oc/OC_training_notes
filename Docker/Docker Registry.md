#commands 
1.  Create repository online in a docker registry
2.  Push into a registry

## Image naming concepts in docker repositories
`registryDomain/imageName:tag`
1. Do docker login
1. **Tag** an image with name given by repository
	```docker tag <image name in curr host> <image name for registry>```
2. Push
	```docker push <image name for registry>```

Now you can move onto to [Deploying an application](Deploying%20an%20application.md).