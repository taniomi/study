tags:: dataeng

- https://youtu.be/ywvtrqHcmEw
- # ([17:15](https://www.youtube.com/watch?v=ywvtrqHcmEw&t=1035s)) O que é o Databricks e como ele se destaca
	- ## O que o Databricks oferece?
		- Computação na forma de um _cluster spark_. O _spark_ é uma ferramenta de código aberto. O cluster fica alocado num cloud provider (EC2, da AWS)
			- [_spark_](https://spark.apache.org/): conjunto de ferramentas e bibliotecas (framework) para processar dados de forma mais rápida, otimizando o processo de lidar com grandes volumes de dados. **(nota: spark é open-source)**
		- O Databricks pega o spark e coloca ele em uma roupagem mais bonitinha, oferecendo uma interface, gerenciamento de cluster, e integração com storage e ferramentas para ML e BI.
		- Esse _cluster spark_ é efêmero, se desligar o cluster, tudo morreu e foi pro espaço, então os dados que você produz no cluster tem que ser persistido em algum _storage_.
			- _storage_: (é como um pendrive virtual, conectar com o storage é como espetar o pendrive em alguma porta USB)
				- tipos: data lake, data lakehouse, data warehouse
				- providers: AWS (S3), Azure (SQL Server)
		- Databricks não é um cloud provider, mas utiliza cloud providers (AWS, Azure, GCP) para trabalhar em cima.
		- Databricks proporciona uma plataforma que embarca o time de engenharia, ciência, análise e negócio. Isso sem ter um time para cuidar da infraestrutura!
- # ([36:20](https://www.youtube.com/watch?v=ywvtrqHcmEw&t=2180s)) Instalação e configuração do ambiente + Passos iniciais para criar um Data Lakehouse
	-