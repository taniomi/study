tags:: [[dio/docker]]

- instructor:: [[denilson-bonatti]]
- # Primeiro Dockerfile
	- ```Dockerfile
	  FROM ubuntu  # create container from image
	  # update apt, install python and clean any installation trash
	  RUN apt update && apt install -y python3 && apt clean
	  COPY app.py /opt/app.py  # copy a file to a destination
	  CMD python3 /opt/app.py  # run this command
	  ```
- # Criando imagem personalizada do Apache
	- ```dockerfile
	  FROM debian
	  RUN apt-get update && apt-get install -y apache2 && apt-get clean
	  
	  ENV APACHE_LOC_DIR="var/lock"
	  ENV APACHE_PID_FILE="var/run/apache2.pid"
	  ENV APACHE_RUN_USER="www-data"
	  ENV APACHE_RUN_GROUP="www-data"
	  ENV APACHE_LOG_IDR="var/log/apache2"
	  
	  ADD site.tar /var/www/html  # o add copia e já descompacta o arquivo site.tar
	  LABEL description = "Apache webserver 1.0"
	  VOLUME var/www/html  # local dos arquivos
	  EXPOSE 80  # webserver, porta 80
	  ENTRYPOINT ["/usr/sbin/apachectl"]
	  CMD ["-D", "FOREGROUND"]
	  ```
	- ```bash
	  docker image build -t debian-apache:1.0
	  docker run -dti -p 80:80 --name meu-apache0 debian-apache:1.0
	  
	  # criando um segundo container com a mesma imagem, só muda a porta
	  docker run -dti -p 8080:80 --name meu-apache1 debian-apache:1.0
	  ```
- # Imagens personalizadas a partir de linguagens de programação [^1]
	- ```dockerfile
	  FROM python:3
	  
	  WORKDIR /usr/src/app
	  
	  COPY requirements.txt ./
	  RUN pip install --no-cache-dir -r requirements.txt
	  
	  COPY . .
	  
	  CMD [ "python", "./your-daemon-or-script.py" ]
	  ```
	- A imagem do python é bem maior do que se criar uma imagem do ubuntu e colocar python lá dentro. Por quê?
	  background-color:: red
- # Gerando uma imagem MULTISTAGE
	- Compilações multiestágio
	- Criar bin (binário) de uma aplicação (imagem de linguagem de programação para programar)
	  logseq.order-list-type:: number
	- Rodar o bin (container linux)
	  logseq.order-list-type:: number
	- ## Por que vamos fazer isso?
		- Maior problema para construir imagens é manter ela pequena.
		- Toda instrução no Dockerfile adiciona dados, é preciso limpar
	- ## Prática
		- ```bash
		  docker pull golang
		  docker pull alpine  # linux
		  
		  docker images  # compare the image sizes!
		  ```
		- ```go
		  package main
		  import (
		  	"fmt"
		  )
		  
		  func main() {
		    fmt.Println("Qual é o seu nome?")
		    var name string
		    fmt.Scanln(&name)
		    fmt.Printf("Oi, %s! Eu sou a linguagem Go!", name)
		  }
		  ```
		- ```Dockerfile
		  # stage 1
		  FROM golang as exec
		  
		  COPY app.go /go/src/app/
		  
		  ENV GO111MODULE=auto  # para criar o executável bin em qualquer dir
		  
		  WORKDIR /go/src/app/
		  
		  RUN go build -o app.go .  # código gerando um executável, RUN é diferente
		  
		  # stage 2
		  FROM alpine
		  
		  WORKDIR /appexec
		  
		  COPY --from=exec /go/src/app /appexec
		  RUN chmod -R 755 /appexec
		  ENTRYPOINT ./app.go
		  ```
		- ```bash
		  docker image build -t app-go:1.0
		  docker run -ti --name meuappgo app-go:1.0
		  ```
		- A imagem do app-go tem 9.77MB, enquanto que a imagem do golang tem 862MB!
- # Upload de imagens para DockerHub
	- ```bash
	  docker login
	  
	  # my-go-app v.1.0
	  docker build . -t [dockerhub username]/my-go-app:1.0
	  
	  docker push [dockerhub username]/my-go-app:1.0
	  ```
- # Registry: criando um servidor de imagens
	- *registry*: servidor de imagens do Docker
	  id:: 674e4256-a88a-48e3-bb85-76cc78dcca42
	- Criar servidor só de imagens do Docker para ter imagens só da sua empresa.
	- Não quero colocar as imagens no DockerHub, porque não é uma imagem pública.
	- Lá no servidor/VM para imagens, já com Docker instalado:
	  logseq.order-list-type:: number
		- ```bash
		  docker run -d -p 5000:5000 --restart=always --name registry registry:2
		  # restart if anything happens and the container goes down
		  
		  docker ps  # check container
		  ```
	- Enviar a imagem para o servidor
	  logseq.order-list-type:: number
		- ```bash
		  docker logout  # desencargo de consciência
		  
		  docker image tag [image id] [server ip]:5000/my-go-app:1.0
		  
		  docker push [server ip]:5000/my-go-app:1.0
		  
		  curl [server ip]:5000/v2/_catalog  # see if image is on the server
		  ```
		- ```bash
		  # if https error, whitelist the server
		  nano /etc/docker/daemon.json
		  # write { "insecure-registries":["[server ip]:5000"]}
		  systemctl restart docker
		  ```
	- Fazer download da imagem do servidor para local
	  logseq.order-list-type:: number
		- ```bash
		  docker pull [server ip]:5000/my-go-app:1.0]
		  ```
- # Referências
	- [^1]: https://hub.docker.com/_/python/