tags:: [[dataeng]]

- https://youtu.be/ywvtrqHcmEw
- # ([17:15](https://www.youtube.com/watch?v=ywvtrqHcmEw&t=1035s)) O que é o Databricks e como ele se destaca
	- ## O que o Databricks oferece?
		- Computação na forma de um *cluster spark*. O *spark* é uma ferramenta de código aberto. O cluster fica alocado num cloud provider (EC2, da AWS)
			- [*spark*](https://spark.apache.org/): conjunto de ferramentas e bibliotecas (framework) para processar dados de forma mais rápida, otimizando o processo de lidar com grandes volumes de dados. **(nota: spark é open-source)**
		- O Databricks pega o spark e coloca ele em uma roupagem mais bonitinha, oferecendo uma interface, gerenciamento de cluster, e integração com storage e ferramentas para ML e BI.
		- Esse *cluster spark* é efêmero, se desligar o cluster, tudo morreu e foi pro espaço, então os dados que você produz no cluster tem que ser persistido em algum *storage*.
			- *storage*: (é como um pendrive virtual, conectar com o storage é como espetar o pendrive em alguma porta USB)
				- tipos: data lake, data lakehouse, data warehouse
				- providers: AWS (S3), Azure (SQL Server)
		- Databricks não é um cloud provider, mas utiliza cloud providers (AWS, Azure, GCP) para trabalhar em cima.
		- Databricks proporciona uma plataforma que embarca o time de engenharia, ciência, análise e negócio. Isso sem ter um time para cuidar da infraestrutura!
- # ([36:20](https://www.youtube.com/watch?v=ywvtrqHcmEw&t=2180s)) Instalação e configuração do ambiente + Passos iniciais para criar um Data Lakehouse
	- ## Como escolher a *runtime version* do cluster do Databricks?
		- Tem a versão do Databricks, do Scala (linguagem em que o Spark é escrito) e do Apache Spark
		- LTS: Long Term Support (significa que o seu cluster vai funcionar por bastante tempo)
		- Photon Acceleration: otimização para Spark utilizada principalmente para queries SQL (+ caro)
		- Node type: tipo de máquina do seu provedor de cloud (AWS, Azure)
			- Como vai ficar dividido seu cluster, um computador (driver) vai fazer a orquestração dos workers, distribuindo tarefas para processamento. Tanto os workers quanto o driver têm memória e cores para processamento, o que os diferencia é para o quê são utilizados.
	- > Dica: começar com o menor cluster possível, e depois aumentar à medida que for necessário
	- ## Advanced options
		- Diferença de *on-demand* e *spot*
			- *on-demand*: pagamento da máquina reservada do seu provedor de cloud
			- *spot*: máquinas disponíveis no momento, normalmente mais baratas do que reservar, mas é possível ficar sem máquinas disponíveis e às vezes o preço aumenta
			- Possível escolher máquinas spot e limitar o preço máximo (ex.: 90% of on-demand instance price)
		- Spark config
			- spark.databricks.delta.autoCompact.enabled true
			  spark.databricks.delta.optimizeWrites.enabled true
			  spark.databricks.delta.properties.defaults.enableChangeDataFeed true
			  spark.driver.maxResultSize 30g
		- JDBC/ODBC
			- É possível conectar PowerBI com Databricks. O Databricks processa os dados e o PowerBI consome.
	- ## Libraries
		- Se instalar biblioteca no cluster, todos os notebooks acoplados ao cluster podem acessar.
		- Se instalar no notebook (pip install) a lib só fica acessível para aquela sessão para aquele notebook, e toda vez que o notebook rodar, a lib instala de novo. (environment nível notebook!)
- # ([54:59](https://youtu.be/ywvtrqHcmEw?t=3299)) Catálogos de Dados
	-