# Configuração de Ambiente  

Django é um framework de alto nível voltado para Web Python. Tem como objetivo promover um desenvolvimento rápido e limpo, atingindo prazos e expectativas com qualidade.  
Como algumas aplicações são baseadas em python, é preferencial que, a instalação das dependências do Django seja feita em um ambiente virtual que será o escopo de atuação do framework e demais atualizações de dependências.  

Para configurar corretamente siga os passos abaixo direto no seu terminal:  
**OBS:** Configuração realizada em linux 64 bits.  

**Passo 1**  
Verifique se você possui uma versão do python em sua máquina.  
      ``$ python3 --version``  

**Passo 2**  
Caso não tenha essa ou nenhuma versão instalada, execute:  
**Ubuntu**  
      ``$ sudo apt-get install python3.4``  

Feito isso, vamos agora instalar o ambiente virtual (**virtualenv**).  

**Passo 3**  
Primeiro vamos verificar se possui uma versão do virtualenv através do comando:  
	``$ virtualenv --version``  
	
**Passo 4**  
Caso não possua uma versão instalada, efetue o download usando:  
	``$ sudo apt-get install python-virtualenv``  

Pronto, com o virtualenv instalado podemos continuar.  

**Passo 5**  
Inicie agora um diretório qualquer(com nome a seu gosto):  
	``$ mkdir meu_django``  
Acesse o diretório:  
	``$ cd meu_django``  
E aqui vamos criar o ambiente virutal chamado ambvirtual(nome definido a seu gosto), digite:  
	``python3 -m venv ambvirtual``  

**Passo 6**  
Feito isso, perceba que teremos um novo diretório chamado ambvirtual.  
Vamos iniciar sua execução através de:  
	``$ source ambvirtual/bin/activate``  

Para finalizar essa etapa, seu terminal deve-se parecer com algo assim:  
	``(ambvirtutal) ~/meu_django $``  

**Passo 7**  
Agora dentro da virtualenv basta instalar o Django:  
	``(ambvirtual) ~$ pip install django``  

OBS.: caso não possua o pip instalado em sua máquina, execute o comando:  
        ``apt-get install python-pip``  

E para ter a versão mais recente, execute:   
        ``pip install -U pip``
ou 
        ``pip install --upgrade pip`` 
 
Pronto! Seu ambiente para desenvolvimento Django está configurado.    


# DOJO de linguagem (material didático)
Agora que o ambiente está instalado, antes de criar um projeto Django,
vamos discutir sobre: como o Django funciona? Qual é a sua arquitetura?
Como o código pode ser modularizado?

## Arquitetura Django
O Django trabalha com uma arquitetura semelhante a tão famosa Model, View,
Controller (MVC), já bem estabelecida do Ruby on Rails e formando base da
maioria dos projetos Java Web. Porém, o Django utiliza-se de nomenclaturas
diferentes para representar seus semelhantes nas linguagens a pouco citadas:
Model, View, Template. Carinhosamente apelidados, de forma cômica, de MTV.

### Model
As models são responsáveis pelas abstrações dos objetos da vida real no código.
Lembra-se das classes, com atributos e métodos? Pois bem, se encaixam aqui.
Elas se encarregarão de dar as caras e funcionalidades para as futuras instâncias
dos objetos. A seguir, será demostrado um exemplo de uma model. Não se atente, por
enquanto, à sintaxe. Foque nos atributos declarados e nos métodos def.

``` python
class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)

    def speak(self):
        print("Hello World!")
```
### View

### Template

## Criando um projeto Django
Dentro do ambiente virtual, basta executar o comando django-admin para utilizar
a interface que o Django disponibiliza. Iremos criar o projeto chamado my_twitter.
`django-admin startproject my_twitter`

Este comando irá criar uma pasta chamada my_twitter contendo vários arquivos e uma pasta.
Esta pasta representa o app principal do projeto, onde contém o arquivo de configuração
e o arquivo principal de Url's. Os principais são:

* Pasta com o nome do projeto: my_twitter
* Arquivo de configuração: settings.py 
* Arquivo de Url's: urls.py
* Arquivo de gerenciamento do projeto: manage.py

A árvore de diretórios neste momento irá ser representada da seguinte forma:<br><br>
.<br>
├── [4.0K]  my_twitter/<br>
│   ├── [   0]  __init__.py<br>
│   ├── [3.0K]  settings.py<br>
│   ├── [ 767]  urls.py<br>
│   └── [ 398]  wsgi.py<br>
└── [ 808]  manage.py*<br>


# DOJO de testes (material didático)


# Repositórios educativos


# Material didático produzido na disciplina (times, coaches, etc)