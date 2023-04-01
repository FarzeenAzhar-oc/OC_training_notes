#commands 
- Docker volume is utilised for persistence of data
- We plug physical file system path i.e its **mounted** on container's virtual filesystem.
- On startup data is automatically created

## 3 volume type
1. Host volumes
	`docker run -v <host data path>:<container data path>`
	We can decide where on the host file system the reference is made.
2.  Anonymous volume
		`docker run -v <container data path>`
		Docker creates it's own volume
		
3. Named volumes
			`docker run -v name:<container data path>`	
		Can use `name` as reference

## Docker Volume locations
- Docker volumes depends on diff OS
	- linux : /var/lib/docker/volumes