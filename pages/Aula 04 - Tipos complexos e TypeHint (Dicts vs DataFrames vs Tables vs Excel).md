tags:: [[data-eng]], [[jornada-dados]]

- instructor:: [[luciano-galvao]]
- Checklist
	- DOING Parte 1 - typing, listas e dicts
	  :LOGBOOK:
	  CLOCK: [2025-03-25 Tue 19:35:31]--[2025-03-25 Tue 19:35:44] =>  00:00:13
	  CLOCK: [2025-03-25 Tue 19:35:44]--[2025-03-25 Tue 19:35:45] =>  00:00:01
	  CLOCK: [2025-03-25 Tue 19:35:45]
	  CLOCK: [2025-03-25 Tue 19:35:54]
	  :END:
	- TODO Parte 2 - trabalhando com arquivos e funções
	  :LOGBOOK:
	  CLOCK: [2025-03-25 Tue 19:35:57]
	  :END:
- [Github](https://github.com/lvgalvao/data-engineering-roadmap/tree/main/Bootcamp%20-%20Python%20para%20dados/aula04)
- ## Type Hint
	- Uma discussão infinita em ciência da computação.
- ### Tipagem Fraca vs. Forte
	- **Tipagem Forte**: Em linguagens com tipagem forte, uma vez que uma variável é atribuída a um tipo, não pode ser automaticamente tratada como outro tipo sem uma conversão explícita. Python é um exemplo de linguagem com tipagem forte. Isso significa que operações que misturam tipos incompatíveis (como adicionar um número a uma string) resultarão em erro.
	- **Tipagem Fraca**: Linguagens com tipagem fraca permitem maior flexibilidade nas operações entre diferentes tipos, fazendo conversões de tipo implícitas. JavaScript é um exemplo clássico, onde você pode adicionar números a strings sem erros, resultando em uma concatenação de texto.
- ### Tipagem Estática vs. Dinâmica
	- **Tipagem Estática**: Linguagens de tipagem estática, como Java e C++, exigem que o tipo de cada variável seja declarado explicitamente no momento da compilação. Isso ajuda a detectar erros de tipo antes da execução do programa, aumentando a segurança do tipo e potencialmente melhorando o desempenho.
	- **Tipagem Dinâmica**: Python é um exemplo de linguagem com tipagem dinâmica, onde os tipos são inferidos em tempo de execução e não precisam ser declarados explicitamente. Isso oferece flexibilidade e rapidez no desenvolvimento, mas pode aumentar o risco de erros de tipo que só serão detectados em tempo de execução.
	- Python tem uma tipagem forte e dinâmica.
	- A partir do python 3.5, foi adicionado o *type hint*.
	- Sem *type hint*:
	  ```python
	  idade = 30
	  altura = 1.75
	  nome = "Alice"
	  is_estudante = True
	  ```
	- Com *type hint*:
	  ```python
	  idade: int = 30
	  altura: float = 1.75
	  nome: str = "Alice"
	  estudante: bool = True
	  ```
	- Dá para usar *type hint* quando se define uma função[^1]:
	  ```python
	  def surface_area_of_cube(edge_length: float) -> str:
	      return f"The surface area of the cube is {6 * edge_length ** 2}."
	  ```
	  **Note:** The Python runtime **does not** enforce function and variable type annotations.
- ## Listas e Dicionários
	- Dicionário é uma *hash table*/*hash mapping*[^2].
- > Tenha o costume de ler documentação. Aprenda a ler documentação. A documentação é a source suprema sobre a linguagem ou biblioteca.
- **continue from: 34:21**
- ## Referências
	- [^1]: https://docs.python.org/3/library/typing.html
	- [^2]: https://docs.python.org/3/tutorial/datastructures.html#dictionaries