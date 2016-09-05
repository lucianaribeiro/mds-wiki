# Configuração de Ambiente
## Instalando Ruby on Rails no Ubuntu
### Usando RVM (Ruby Version Manager)

O RVM é uma ferramenta muito popular e bem suportada pela comunidade, utilizada para facilitar a mudança entre as versões do Ruby e gerenciar as gemas. Convenientemente o RVM pode ser utilizado para instalar o Ruby.

### Preparação do sistema

Para a instalação do Ruby on Rails, é necessário uma preparação prévia na sua máquina. 
Também é necessário ter acesso de superusuário (root) para atualizar os softwares do sistema.
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

### Instale Node.js

Para desenvolvimento no Ubuntu Linux é melhor instalar o ambiente javascript Node.js server-side.

`$ sudo apt-get install nodejs`

e configure o `$PATH`.

Se não tiver o Node.js instalado, será necessário adicionar ao Gemfile para cada aplicação Rails que for criada:

`gem 'therubyracer'`

### Verifique o Gerenciador de Gems

RubyGems é o gerenciador de Gems no Ruby.

Verifique a versão do gerenciador instalado com o seguinte comando:

`$ gem -v`

`2.3.1`

Para atualizar utilize `$ gem update --system`.

### Instale o Bundler

Bundler é uma ferramenta essencial para gerenciar as gems quando se está desenvolvendo e rodando aplicações Rails.

`$ gem install bundler`

### Opções de instalação Rails
Verifique a versão do Rails atual:

`$ rails -v`

`Rails 5.0.0`

Instale então o rails:

`$ gem install rails`

e verifique sua versão após a instalação: 

`$ rails -v`

Desta forma será instalado a última versão estável, se for necessária uma versão específica utilize o comando a seguir.

Por exemplo, se for necessária a versão do Rails 3.2.18:

`$ gem install rails --version=3.2.18`
`$ rails -v`

Fonte de informação: [Site RAILSAPPS](http://railsapps.github.io/installrubyonrails-ubuntu.html)

# Arquitetura MVC Ruby on Rails

# DOJO de linguagem (material didático)
## Codecademy
> ### Ruby
> https://www.codecademy.com/pt-BR/learn/ruby
> ### Rails
> https://www.codecademy.com/pt-BR/learn/learn-rails
> ### Rails Authentication
> https://www.codecademy.com/pt-BR/learn/rails-auth

## Caelum
> ### Ruby on Rails
> https://www.caelum.com.br/apostila-ruby-on-rails/ruby-on-rails/

> ### Ruby Gems
> https://rubygems.org/

# DOJO de testes (material didático)

> ### Code school
> https://www.codeschool.com/courses/testing-with-rspec

> ### Usando o RSpec para testar sua aplicação Rails - Modelos
> https://nandovieira.com.br/usando-o-rspec-para-testar-sua-aplicacao-rails-modelos

# Repositórios educativos


# Material didático produzido na disciplina (times, coaches, etc)