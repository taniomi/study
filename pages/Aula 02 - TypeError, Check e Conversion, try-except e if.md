tags:: [[data-eng]], [[jornada-dados]]

- instructor:: [[luciano-galvao]]
- [GitHub](https://github.com/lvgalvao/data-engineering-roadmap/tree/main/Bootcamp%20-%20Python%20para%20dados/aula02)
- ## Type Check [^1]
	- Verificação de tipo (`type check`) é o processo de verificar o tipo de uma variável. Isso pode ser útil para garantir que operações ou funções sejam aplicadas apenas a tipos de dados compatíveis, evitando erros em tempo de execução.
	- ### Exemplo de Type Check
		- Para verificar o tipo de uma variável em Python, você pode usar a função `type()` ou `isinstance()`.
		  
		  ```
		  numero = 10
		  if isinstance(numero, int):
		    print("A variável é um inteiro.")
		  else:
		    print("A variável não é um inteiro.")
		  ```
		- Este código verifica se `numero` é uma instância de `int` e imprime uma mensagem apropriada.
- # Referências
- [^1]: https://github.com/lvgalvao/data-engineering-roadmap/tree/main/Bootcamp%20-%20Python%20para%20dados/aula02#type-check