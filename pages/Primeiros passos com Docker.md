tags:: [[dio/docker]], [[data-eng]]

instructor:: [[denilson-bonatti]]

- # Download de imagens
- id:: 67436af5-1ae4-4985-b457-93f8296d6f41
  ```bash
  docker images  #show images
  docker ps -a   #show executions
  ```
- # Executando um contâiner
	- id:: 67436e81-f1f6-4a59-a9fd-76b675b4df64
	  ```bash
	  docker run $imagename sleep 10  # runs the command to sleep 10s
	  docker stop [$id or $name]  # stop the container
	  docker run -it ubuntu  # runs in interactive and terminal mode
	  ```
- # Velha e nova sintaxe
	- ```bash
	  docker ps  # old
	  docker container ls  # new
	  docker run # old
	  docker container run  # new
	  ```
- # Executando aplicações no contâiner
	- ```bash
	  docker run -dti ubuntu # detach, terminal, interactive
	  docker exec -it $containerid /bin/bash  # execute bash in ubuntu
	  ```
	- Executar o bash no Ubuntu implica poder fazer qualquer operação de terminal
- # TAGs
	- Especifica a versão que você quer da imagem.
	- Ex.:
	  ```bash
	  docker pull debian:9
	  docker run -dti debian:9 --name Debian9
	  ```
- # Criando container do MySQL
  id:: 67451c97-9d8b-43c5-a877-8aa500df1ba5
	- ```bash
	  docker pull mysql # specify version tag if necessary
	  
	  # especificar root password e porta para acessar no host (padrão 3306)
	  docker run -e MYSQL_ROT_PASSWORD=[pass] -p 3306:3306 --name mysqldb -d mysql
	  
	  # abrir bash no mysql
	  docker exec -it mysqldb bash
	  
	  # logar no mysql (como nas aulas de CSB30!)
	  mysql -u root -p --protocol=tcp
	  ```
	- ```bash
	  # o docker cria um novo dispositivo de rede, o docker tem uma faixa de rede!
	  # cada container recebe um ip na faixa de rede do dispositivo
	  ip a
	  
	  # IPAddress will have the ip of the container
	  docker inspect mysqldb
	  
	  # It is possible to access with the mysql-client the db in the docker container
	  # from outside the docker container through the port 3306
	  mysql -u root -p --protocol=tcp
	  ```