tags:: [[dio/intro-cloud-computing]]
id:: 6716cb05-6f71-4cdc-b2ea-409a2f59805a

- # Computação em nuvem: Domínio do Objetivo
	- ## O que é cloud computing?
		- Cloud computing veio para substituir a infraestrutura local. Ao invés de ter na própria empresa uma sala com servidores, hacks, memória, ventiladores, ar condicionado, etc., usa-se recursos que estão fisicamente em outro lugar.
		- Um computador pode emular ser um computador com specs diferentes. Como? Um computador fisicamente possui uma quantidade específica de memória, capacidade de processamento, etc. Mas e se ele "escondesse" parte desses recursos e disponibilizasse somente metade para rodar um Windows? E na outra metade dos recursos rodar um Linux?
		- E se juntar várias máquinas para aumentar a capacidade, como se adicionasse um SSD? A máquina acaba tendo recursos variáveis, além de poder disponibilizar esse recurso que "sobra" para outra tarefa de processamento.
	- ## O que é nuvem privada?
		- É ter uma rede de computadores que só é visível e acessível dentro da empresa. É o *on-premise*.
	- ## O que é nuvem pública?
		- AWS, Azure, etc., são cloud providers. Render também é cloud provider?
		- São nuvens que podem ser acessadas não só na empresa, mas de outras redes.
	- ## O que é nuvem híbrida?
		- Quando nuvem privada e pública estão conectadas. Bem comum, difícil ter tudo na nuvem. Muito caro ter tudo *on-premises*?
	- ## O que é multicloud?
		- Quando é utilizado mais de um cloud provider.
		- Nuveto: tem coisa na AWS, na Azure, no MySQL, no grafana, no linode.
- # Comparação de Modelos de Nuvem
	- ## Nuvem pública
		- Paga apenas pelos recursos que são utilizados (pay-as-you-go)
		- Mais rápido de (des)provisionar recursos
		- O provedor de cloud cuida do hardware, da infraestrutura
		  id:: 6717ade3-976c-4f68-88f1-2475a4988ef4
	- ## Nuvem privada
		- Tudo é responsabilidade do usuário (infra, software, hardware)
		- Questão de segurança fica totalmente sob o controle do usuário
	- ## Nuvem híbrida
		- Maior flexibilidade
			- Local da provisão
			- Qual/is cloud provider
		- Cloud providers oferece recursos de segurança, mas organização define como e quando utilizar
- # Comparação CapEx e OpEx
	- ## CAPEX: Capital Expenditure
		- Despesas com infraestrutura on-premises.
		- É o que o meu pai faz, comprar computador, ar condicionado, hack, cabeamento, memória, servidores, etc.
		- Depois desse investimento inicial, o custo diminui
		- Sobram custos de energia elétrica, manutenção.
	- ## OPEX: Operating Expenditure
		- Despesas operacionais na cloud.
		- Custos com produtos e serviços, pay-as-you-go
		- Databricks tem opção de provisionar máquinas de forma que você reserve a máquina pra você ou use conforme estiver disponível e pague menos (quando o que você estiver rodando não for tão importante e puder ficar lento ou mesmo cair)
	- ## Modelo baseado em consumo
		- Fatura por tempo que o serviço foi usado
		- Databricks: horas x DBUs
		  id:: 6717b0e9-cd3c-4912-aca9-6f15e9b900e2