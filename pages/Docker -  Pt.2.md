tags:: [[data-eng]], [[jornada-dados]]

- # Perguntas diversas
	- ## Qual a diferença entre *terraform* e *kubernetes*?
		- *terraform*: cuida da infraestrutura da cloud
		- *kubernetes*: cuida do Dockerfile
		  id:: 66fdafb8-ef2e-4444-a431-e37c5070cbc3
	- ## Por que async?
		- ![image.png](../assets/image_1727901930212_0.png)
		- Com o *async*, dá pra fazer, por exemplo, diversas requisições usando a lib requests sem esperar cada uma terminar de rodar.
		- Por que fazer isso? Se os seus requests dependem somente da página que você quer acessar, neste caso.
		- Aliás, com o FastAPI dá para encapsular requests de cientistas de dados e transformar em API, acredito que isso bate com o princípio de boa arquitetura de dados, com áreas que são "loosely coupled".
	- ## Como saber o que posso baixar e rodar no Docker?
		- No https://hub.docker.com/ tem muitas imagens disponíveis.
		- ```bash
		  docker pull mysql
		  ```
- # Múltiplos contâineres com docker-compose.yml
	- timestamp:: 00:20:01
	- O docker-compose é usado pra subir mais de um contâiner de uma vez só. É uma versão primitiva do *kubernetes*. Ex.: subir PostgreSQL e o pgAdmin 4 pra acessar o banco [^1].
	- ## Postgres +Streamlit + Python
		- timestamp::  00:39:00
	- ## ❓Como não expor credenciais no docker-compose
		- timestamp::  00:50:30
		- Quando rodar `docker run`, incluir as credenciais como variáveis de ambiente.
- # Momento coach
  background-color:: yellow
	- timestamp:: 00:57:00
- # docker-compose.yml
	- Checar versão [^2]:
	  ```bash
	  docker-compose --version
	  ```
	- Se for v2, não precisa especificar versão no docker-compose.yml [^3]
- # Referências
	- [^1]: ([PostgreSQL + Docker Compose: criando rapidamente ambientes e populando bases para testes](https://renatogroffe.medium.com/postgresql-pgadmin-4-docker-compose-montando-rapidamente-um-ambiente-para-uso-55a2ab230b89))
	- [Linux Tips](https://www.youtube.com/@LinuxTips)
	- [Fábio Akita - Começando aos 40](https://youtube.com/playlist?list=PLdsnXVqbHDUc7htGFobbZoNen3r_wm3ki&si=MfqmGNuHnt8aJBWP)
	- [^2]: ([How to Create a MySql Instance with Docker Compose](https://medium.com/@chrischuck35/how-to-create-a-mysql-instance-with-docker-compose-1598f3cc1bee))
	- [^3]: ([Do you need to put the version at the top of docker-compose.yml file?](https://forums.docker.com/t/do-you-need-to-put-the-version-at-the-top-of-docker-compose-yml-file/135863))