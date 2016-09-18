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

É a camada lógica do sistema, ela contém os métodos de acesso as Models e as Templates. Funciona como uma ponte entre as outras duas camadas. As requisições são tratadas pelo próprio Django e não pela View.
 
### Template

É a camada encarregada de mostrar nossa aplicação para o usuário e a que manda as requisições para View. Em outras palavras, é a interface da aplicação e manda os dados do usuário para processamento ou mostra algo à ele.

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

## Divisão em Apps
O django trabalha com sistema de vários apps que formam a aplicação. A ideia é que esses apps
sejam plugáveis e portáveis. Dessa maneira, um app pode ser desenvolvido em uma aplicação e
utilizado em outra. Cada app possui toda estrutura necessária e imposta pela arquitetura do
django para que funcione bem: Views, models, templates, etc.

Um app é composto basicamente pelos seguintes componentes:
* Models
* Views
* Templates
* Tests
* Static
* Migrations
* Forms
* Tests

Segue abaixo um exemplo de um app convencional Django, criado pelo professor Fábio Mendes.
[Code School](https://github.com/fabiommendes/codeschool/tree/master/src/cs_auth).

## Criando um aplicativo Django
Vamos primeiramente, criar um aplicativo responsável por apresentar a página inicial do nosso
projeto. Vamos chamá-lo de home. E toda vez que o nosso site for solicitado por uma url, iremos
apresentar a página inicial definida neste app. 

Desta maneira, para criar o app, é necessário apenas utilizar o commando:
`django-admin startproject my_twitter`

# DOJO de testes (material didático)
## Testes Unitários
Testes unitários são testes que são expressados como métodos em uma classe _Python_ que seja uma subclasse de **unittest.TestCase**. Por exemplo:

```Python
import unittest

 class CalculatorTestCase(unittest.TestCase):
    """Every test class must to have a setUp method"""
    def setUp(self):
        self.calc = src.calculator.Calculator()

     def testAdd(self):
         self.assertEquals(self.calc.add(2, 5), 7)
         self.assertEquals(self.calc.add(0, 0), 0)
```

Uma vez que os testes estão escritos, a fim de executá-los, deve-se rodar o seguinte comando:

`$ ./manage.py test`

Quando os testes estão para ser rodados, o comportamento padrão do utilitário de teste é encontrar todas as subclasses de unittest.TestCase, imediatamente montar um conjunto de testes e rodá-lo.

Porém, quando só se quer rodar os testes para uma aplicação específica, basta adicionar o nome da aplicação à linha de comando. Por exemplo, se além de _'myproject.calculator'_, possui-se _'myproject.invoice'_, é possível rodar somente os testes unitários de _'myproject.invoice'_ através de:

`$ ./manage.py test invoice`

# Repositórios educativos


# Material didático produzido na disciplina (times, coaches, etc)

# Referências

[The Django Book, Chapter 5.](http://www.djangobook.com/en/2.0/chapter05.html)