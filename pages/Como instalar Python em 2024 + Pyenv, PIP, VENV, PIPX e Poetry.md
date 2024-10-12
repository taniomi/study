tags:: [[jornada-dados]] [[python]]

- Jornada de Dados [02] Como instalar Python em 2024 + Pyenv, PIP, VENV, PIPX e Poetry
  [Como instalar Python em 2024 + Pyenv, PIP, VENV, PIPX e Poetry](https://youtu.be/9LYqtLuD7z4)
- # POR QUÊ?
	- Evitar o: "mas na minha máquina funciona..."
	- Python tem mais de 20 versões, se os projetos não forem isolados, há muita possibilidade de incompatibilidade.
- # PYENV
	- > Parecido com escolher a versão do Minecraft?
	- Instalar: pyenv (linux | mac users) | pyenv-win (windows users)
	  
	  [pyenv for Windows](https://github.com/pyenv-win/pyenv-win)
	- Follow quick start in README.md
	- Se erro de que o arquivo não pode ser executado, use o código a seguir para permitir que o script rode:
	  
	  ``PS > Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser``
	- Checar se pyenv instalou
	  ``  $ pyenv --version``
		- Se PYENV variable is not set, recommended to set the variable:
			- Criar variáveis de usuário PYENV, PYENV_HOME e PYENV_ROOT com o caminho:
			    ``C:\Users\[user]\pyenv\pyenv-win``
			- Também mudar a variável Path para adicionar os caminhos a seguir e movê-los para o topo da lista:
			  ``  C:\Users\[user]\pyenv\pyenv-win\bin (binário)
			    C:\Users\[user]\pyenv\pyenv-win\shims (interpretadores python)``
	- Instalar versões do python
	  ``  $ pyenv install [python version]``
	- Versão python padrão
	  ``  $ pyenv global [python version]``
	- Linkar cada projeto a uma versão específica de python
	  ``  $ pyenv local [python version]``
	- Sempre instalar versão do python mais moderna e que as libs usadas no projeto aceitem
- # PIP & VENV
	- [Install packages in a virtual environment using pip and venv](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)
	- ## Limpando dependências
		- Dependências de bibliotecas devem ser geridas.
		- Listar libs instaladas
		    ``$ pip list``
		- Deletar todas as libs já instaladas
		  ``$ pip freeze | grep -v "^-e" | xargs pip uninstall -y``
		  
		  > Toda vez que instalar uma lib, criar ambiente virtual
	- ## Utilizando ambiente virtual
		- 1. Ir até pasta do projeto 
		  2. Criar ambiente virtual
		  ``$ python -m venv [.venv | nome do ambiente]``
		  3. Ativar ambiente virtual
		  ``$ source .venv/Scripts/activate``
		  4. Instalar bibliotecas no ambiente ativado
		  ``$ pip install [lib]``
		  5. Desativar ambiente virtual
		  ``$ deactivate``
- # PIPX
	- Pip vem com o python já, isso significa que é bem estável, mas mais demorado para receber novas funções
	- PipX: gestão das libs na sua máquina
	    [pipx — Install and Run Python Applications in Isolated Environments](https://github.com/pypa/pipx)
		- https://github.com/pypa/pipx
	- ## Instalar libs com pipX
		- ``$ pipx install [lib name]``
	- ## Libs para instalar globalmente
		- poetry: facilita gestão de dependência de pacotes
			- [Poetry — PYTHON PACKAGING AND DEPENDENCY MANAGEMENT MADE EASY](https://python-poetry.org/)
		- ipython: torna python mais visualmente amigável no bash (inputs and outputs)
- # POETRY
	- Por quê?
		- Centraliza a gestão de dependências de pacotes
		- Ajuda na hora de desenvolver libs, já joga para o PyPI, tem tracking
	- ## Configurar Poetry para gerenciar os ambientes virtuais
	  id:: 669aca2a-b3fb-4e14-8d47-08ac4ad7a31c
		- ``$ poetry config virtualenvs.in-project true``
	- ## Criar novo projeto com poetry
		- https://python-poetry.org/docs/basic-usage/
		  
		  1. Criar projeto
		    ``$ poetry new [project name]``
		  
		  2. Definir qual versão do python com pyenv
		    > pyenv faz gestão da versão do python, poetry faz gestão das libs do python
		  
		  ``$ pyenv local [python version]``
		  
		  3. Configurar poetry para usar a versão local do python definida com pyenv
		    ``$ poetry env use [python version]``
		  > Esse comando já cria a pasta do venv!
		  
		  4. Instalar libs
		    ``$ poetry add [lib name]``
	- ## Visualizar libs instaladas com poetry no venv
		- ``$ poetry shell``
		  ``$ pip freeze``
	- ## Deletar uma lib
		- ``$ poetry remove [lib name]``
	- Poetry remove a lib e todas as dependências
	- ## Codando com ambiente virtual gerenciado pelo POETRY
		- 1. Activate the virtual environment:
		    ``$ poetry shell``
		  
		  2. Open cwd in vscodium | vscode
		    ``$ codium . | code .``
		  
		  3. Make sure the interpreter for python or jupyter is the one from the virtual environment
		    ".venv(Python [venv version])"
	- ## Exportando dependências para requests.txt de poetry.lock
		- ``$ poetry export --output requirements.txt``