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
-