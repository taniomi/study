tags:: [[dio/docker]], [[data-eng]]

- instructor:: [[denilson-bonatti]]
- # Montando mount local de armazenamento
	- Para persistir dados, indicar path (também dá para indicar num *Dockerfile*)
	- ```bash
	  docker run -e MYSQL_ROOT_PASSWORD=[pass] --name mysqldb -d -p 3306:3306 --volume=/data/mysqldb:/var/lib/mysql mysql
	  # --volume=[local path]:[container path]
	  ```
- # Tipos de mount
	- ## bind
		- Vincular um repositório ou arquivo do host ao contâiner
		- ```bash
		  --volume=[local path]:[container path]
		  ```
	- ## named
		- Criados em `/var/lib/docker/volumes`
		- ```bash
		  docker volume create [volume name]
		  ```
		- ```bash
		  --volume [vol name]:[containerpath]
		  ```
	- ## dockerfile volume
		- Igual aos *named*, mas não têm nome
		- O Docker recomenda o uso de volumes em vez do uso de binds, pois os volumes são criados e gerenciados pelo Docker.
		  background-color:: yellow
- # Tipos de mount na prática
	- ## bind
		- ```bash
		  docker run -dti --mount type=bind,src=[path host],dst=[path container],ro ubuntu
		  # ro: read only option
		  ```
	- ## volume
		- ```bash
		  # show volumes created/managed by docker (docker/volumes/)
		  docker volume ls
		  
		  # create volume
		  docker volume create [volume name]
		  
		  # attach volume to container
		  docker run --mount type=volume,src=[volume name],dst=[path container] ubuntu
		  
		  # remove volume
		  docker volume rm [volume name]
		  ```
		- Mais de um container pode estar apontando para o mesmo volume (como se fossem dois containers da mesma aplicação no mesmo db).