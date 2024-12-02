tags:: [[dio/docker]], [[data-eng]]

- instructor:: [[denilson-bonatti]]
- # Limitando memória e CPU
	- ```bash
	  docker stats ubuntu-c # check for container stats
	  docker update ubuntu-c -m 128M --cpus 0.2 # limit memory and CPU
	  ```
- # Informações, logs e processos
	- ```bash
	  docker container logs [container name]
	  docker container top [container name] # see container processes
	  ```
- # Redes
	- ```bash
	  # in docker server
	  ip a
	  docker network ls # list networks
	  docker network inspect bridge # containers will be added to the bridge network
	  
	  # test a connection to another container
	  docker exec -ti ubuntu-c bash # go into ubuntu
	  apt-get install -y iputils-ping # install ping
	  ping 172.17.0.4 # ping ip from another element in bridge
	  ```
	- It is possible to create a network and isolate some containers from others, creating a network only for them.
	- ```bash
	  docker network create [net name]
	  docker run -dti --name [container name] --network [net name] [image]
	  docker network inspect [net name] # check ip for created container
	  docker run -dti --name [container name] --network [net name] [image]
	  
	  # both containers should not be in the bridge network
	  docker network inspect bridge
	  ```