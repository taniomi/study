tags:: [[dio/docker]], [[data-eng]]

- instructor:: [[denilson-bonatti]]
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