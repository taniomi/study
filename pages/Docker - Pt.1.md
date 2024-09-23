tags:: jornada-dados

- # Por que o Docker?
	- Docker veio para ajudar a fazer deploy de apps (qualquer coisa que rode é um aplicativo, seja ETL, dashboard, etc.)
	- Docker roda a Docker engine, que é um kernel do Linux. O Docker roda Linux!
	- A ideia do Docker é que o container você faz como um git pull de imagens de aplicativos que deseja usar, e não é preciso instalar na unha, as configs do setup vêm na imagem.
	- O Docker usa o [Open CI (Open Container Initiative)][^1] para construir os containers
- # Como o Docker funciona?
	- ![image.png](../assets/image_1721401727142_0.png)
	- Docker e Podman usam Open CI e são equivalentes.
	- O *code* é o teu código, teu software.
	- O *dockerfile* é uma solução para todo o setup de criação de ambiente
		- e.g.: setup de ambiente python
		  ```bash
		  git clone ...
		  cd ...
		  pyenv local 3.12.1
		  pip install pipx
		  pipx install poetry
		  poetry env use 3.12.1
		  poetry add pandas
		  .
		  .
		  .
		  ```
	- A *imagem* é um linux com teu código na pasta `/src` e python instalado
	- A *imagem* é como a classe (forma) e o *container* é a instância (biscoito) da *imagem*
- # Buildando primeiro docker
	- Do que precisamos?
		- `dockerfile`
		- `code`
		- `.dockerignore`
	- Depois de terminar esses arquivos:
		- Crie imagem
		  ```bash
		  docker build -t docker-demo .
		  ```
		- Crie container
		  ```bash
		  docker run -d -p 8501:8501 --name docker-demo docker-demo
		  ```
		- `-d`: deattach command from terminal (command doesn't "freeze" terminal)
	- No Docker, é necessário compilar toda vez que tem modificação no código.
- # Docker first
	- O docker diminui drasticamente o tempo pra fazer setup e onboarding porque vai trazer certinho todas as libs com as versões certas.
	  ```bash
	  git clone ...
	  cd ...
	  docker build ...
	  docker run ...
	  ```
	- `Dockerfile` é o `yaml` do CI (Continuous Integration)
- # Referências
	- [^1]: https://opencontainers.org/ "Open Containers Initiative"