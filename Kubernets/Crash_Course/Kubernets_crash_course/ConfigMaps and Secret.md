# ConfigMap
- External configuration of your application
- E.g:
	- DB_URL = mongo-db-service
	- Say you have db and an  app
	- The url for db has to be given in app scripts
	- If the db url changes, you have to rewrite the script, build image, and yada yada
	- ConfigMap helps you to prevent this by letting you map DB_URL to actual url, DB_URL being used in app 

# Secret
- Like ConfigMap but for confidential data
- Encrypted
- E.g : To store password and username of database
- The encryption isn't very secure, so one is expected to use 3rd party apps for better encryption.

ConfigMap and Secret are connected to a pod and used by pod container using enviroment variables or as properties files
![ConfigMap](ConfigMap.svg)