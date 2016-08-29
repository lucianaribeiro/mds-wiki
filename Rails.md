# Configuração de Ambiente
## Instalando Ruby on Rails no Ubuntu
### Usando RVM (Ruby Version Manager)

Utilizada para facilitar a mudança entre as versões do Ruby e gerenciar as gemas, muito popular e bem suportada pela comunidade. Convenientemente a RVM pode ser utilizada para instalar o Ruby.

### Preparação do sistema

Será necessária uma preparação prévia para a instalação do Ruby on Rails na sua máquina. 
Será necessário acesso de superusuário (root) para atualizar os softwares do sistema.
Primeiramente atualize o gerenciador de pacotes:

`$ sudo apt-get update`

Instale o [CURL](http://en.wikipedia.org/wiki/CURL):

`$ sudo apt-get install curl`

### Instale Ruby usando RVM
Use RVM, para instalar o Ruby e gerenciar suas versões do Rails.

Se houver uma versão antiga do Ruby instalada na máquina, não há necessidade de removê-la. RVM deixará a versão do sistema como está e usará o SHELL para interceptar qualquer chamada ao Ruby. 

O [site do RVM](https://rvm.io/rvm/install/) explica como instalar o RVM. Está é a forma mais simples:

`$ \curl -L https://get.rvm.io | bash -s stable --ruby`

A flag `--ruby` instalará a versão mais recente do Ruby.

### Se já existe alguma versão do RVM
Se você já tem uma versão do RVM instalado, atualize para a última versão e instale o Ruby:

`$ rvm get stable --autolibs=enable`

`$ rvm install ruby`

`$ rvm --default use ruby-2.3.1`

Neste exemplo utiliza-se a versão 2.3.1 do Ruby, mas pode ser modificado para outra versão se necessário.

# DOJO de linguagem (material didático)



# DOJO de testes (material didático)


# Repositórios educativos


# Material didático produzido na disciplina (times, coaches, etc)