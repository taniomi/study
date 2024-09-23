tags:: jornada-dados

- Jornada de Dados [03] Como instalar Python + Entendendo PATH e Pyenv em detalhes
- # PYENV
	- ## Instalando pyenv clonando o repo do github
	- Ir para o diretório raiz do usuário
	    ``$ echo $USERPROFILE``
	    C:\Users\[user]
	    ``$ cd C:\Users\[user]``
	- Clonar repo
	    ``$ git clone https://github.com/pyenv-win/pyenv-win.git``
	- Checar instalação
	    ``$ ls .pyenv/ -al``
	- Definir as variáveis do sistema (igual na aula [02])
		- Criar variáveis de usuário PYENV, PYENV_HOME e PYENV_ROOT com o caminho:
		        ``C:\Users\[user]\pyenv\pyenv-win``
			- Também mudar a variável Path para adicionar os caminhos a seguir e movê-los para o topo da lista:
			    ``C:\Users\[user]\pyenv\pyenv-win\bin (binário)``
			    ``C:\Users\[user]\pyenv\pyenv-win\shims (interpretadores python)``
				- Outro modo de alterar paths:
					- Ir para Editor do Registro
					- Adicionar os PATHs na pasta:
					  ``HKEY_CURRENT_USER
					    └──Environment``
	- ## Utilizando várias versões do pyenv
		- Como instalação foi clonando o git, o repo clonado contém as infos de versão
		- Criar branch com outra versão do pyenv
		    ``$ cd .pyenv/``
		    ``$ git checkout tags/v[versão] -b v[versão]``
		- Voltar para a versão principal do pyenv (igual trocar de branch no git)
		    ``$ git checkout main``
		  OU
		    ``$ git switch main``
	- ## Diferentes versões do python com pyenv
		- Checar quais versões do python estão disponíveis para pyenv
		    ``$ pyenv install --list``
		- Instalar versão
		    ``$ pyenv install [python version]``
		- Ver versões instaladas
		    ``$ pyenv versions``
		- Versão python padrão
		    ``$ pyenv global [python version]``
		- Linkar cada projeto a uma versão específica de python
		    ``$ pyenv local [python version]``
	- ## Onde encontrar
		- Versões do python instaladas pelo pyenv
		    ``C:\Users\[user]\.pyenv\pyenv-win\versions``
		- Uma instalação
		    ``$ which [python/pyenv/etc.]``