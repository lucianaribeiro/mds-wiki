## Histórico de Revisão
| Data | Versão | Descrição | Revisor |
|:----:|:------:|:---------:|:-------:|
| 26/05/2017 | 1.0 | Estrutura de tópicos | Vitor Borges |
| 29/05/2017 | 1.1 | Escrita dos tópicos | Vitor Borges e Thiago Moreira |
| 30/05/2017 | 1.2 | Revisão dos tópicos | Danilo Barros e Lucas Rufino |
| 30/05/2017 | 1.3 | Validação dos tópicos e refatoração final | Danilo Barros, Lucas Rufino, Thiago Moreira e Vitor Borges |

## 1. Introdução
<p align="justify>">Atualmente, diversas tecnologias necessitam de consumir dados de WebServices/APIs e nas disciplinas de GPP/MDS não é diferente.</p>
<p align="justify>">Muitas das aplicações construídas no decorrer do semestre necessitam do consumo de dados por meio de servidores, principalmente nos projetos mobile, onde os dados consumidos são enviados para diversos clients diferentes.</p>
<p align="justify>">Com isso, muitas das equipes optam por utilizar esse consumo de dados por meio de APIs construídas em tecnologias REST para consumo de dados via requisições HTTP.</p>
<p align="justify>">Neste documento iremos explicar tecnologias amplamente conhecidas que se encaixam nessas características citadas anteriormente, mostrando uma introdução geral sobre o Node JS e  consumo de dados em um banco não-relacional RethinkDB.</p>

## 2. Tecnologias

### 2.1. Node JS

<p align="justify">Contruído com base em Javascript, o Node.js tem a capacidade de executar código Javascript fora dos navegadores. Além disso, ele pode ser usado também como complemento de outras aplicações ou até mesmo em uma aplicação nativa, permitindo que <i>scripts</i> em JS sejam executados das mais variadas formas, proporcionando um melhor aproveitamento do mesmo. Ele é muito utilizado ao lado do servidor, atendendo demandas de aplicações web e APIs. Apesar disto, ele tem a capacidade de ser executado sem um servidor, sendo uma vantagem relevante.</p>
<p align="justify">O Node.js utiliza o conceito de assincronidade no seu funcionamento, onde realiza varias atividades ao mesmo tendo, facilitando na realização de tarefas e otimizando o seu tempo. Quando o Node foi criado, em 2009, os desenvolvedores queriam deixar esse processo de assincronidade mais fácil e conveniente.</p>
<p align="justify">A arquitetura do Node.js é baseada no paradigma de Programação Orientada a Evento, onde, basicamente, utiliza métodos para monitorar os eventos que avisa o código especializado em responder a um determinado evento, que aquele evento que ele espera ocorreu. Com isso, o código que foi avisado responde ao evento. Esse métodos citados são chamados de callback, e são utilizados constantemente na execução do Node. A assincronidade só é possível devido a presença desses métodos, para ter controle das ações dos diversos <i>scripts</i> rodando ao mesmo tempo na aplicação.</p>

### 2.2. RethinkDB
<p align="justify">Construído em C++ mas que utiliza a sintaxe em Javascript (quando configurado com o Node), o banco de dados RethinkDB é não-relacional que possui uma vasta lista de queries flexíveis, operações intuitivas de monitoramento de API e é facil de configurar e aprender a utilizar.</p>
<p align="justify">A principal ideia do RethinkDB é que ele seja uma base de dados <i>realtime</i>, onde o desenvolvedor pode dizer ao RethinDB para continuamente atualizar resultados de query em tempo real, para o consumo de dados em diversos tipos de plataformas.</p>
<p align="justify">O RethinkDB deve estar dentro das alternativas a serem escolhidas quando:</p>

* Aplicações mobile e web colaborativas;
* Jogos multiplayer;
* Mercados em tempo real;
* Dispositivos conectados.


## 3. Instalação
<p align="justify">Explicaremos agora como ínstalar essas tecnologias na plataforma Linux.</p>
### 3.1. Instalando o Node JS

Para a instalação da mais nova versão do Node utilize os seguintes comandos:

``` bash
    $ curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -
    $ sudo apt-get install -y nodejs
```

Opcionalmente, installe o `build-essencial`  para utilizar addons nativos do npm:

``` bash
    $ sudo apt-get install -y build-essential
```

Com a instalação concluída, cheque se o npm e o Node foram instalados corretamente.

``` bash 
    $ node --version
    v7.10.0
```

``` bash 
    $ npm --version
    4.5.0
```

### 3.2. Instalando o RethinkDB

 <p align="justify">Para a instalação do RethinkDB em distribuições Linux Ubuntu 16.04 utilize os comandos: </p>
 
``` bash
    $ source /etc/lsb-release && echo "deb http://download.rethinkdb.com/apt $DISTRIB_CODENAME main" | sudo tee /etc/apt/sources.list.d/rethinkdb.list
    $ wget -qO- https://download.rethinkdb.com/apt/pubkey.gpg | sudo apt-key add -
    $ sudo apt-get update
    $ sudo apt-get install rethinkdb
```

Para verificar a correnta instalação do RethinkDB execute:

``` bash
    $ rethinkdb -v
    rethinkdb 2.3.5~0trusty (GCC 4.8.2)
```

<p align="justify">Para executar o Rethindb basta abrir o terminal e executar o comando `rethinkdb` e o mesmo será carregado na página do Browser default do seu sistema operacional utilizando a url https://localhost:8080 (porta padrão da tecnologia, mas que pode ser alterada).</p>

## 4. Configuração
<p align="justify">Será falado agora uma breve configuração de uma API RESTFull utilizando o RethinkDB e o Node.js.</p>
<p align="justify">O primeiro passo é criar um projeto em Node. Para isso, crie uma pasta com o nome do projeto que deseja criar.</p>

``` bash
    $ mkdir myAPI
    $ cd myAPI
```
Na pasta da aplicação, inicie um projeto Node.js com o comando npm e as configurações desejadas.

``` bash
     myApp-$ npm init
```
Após isso, deve-se inserir as informações referentes ao seu servidor. Ele pede o nome, versão, descrição, entry point, test command, git repository, palavras-chaves, autor e licença. No fim, ele pergunta se está tudo ok para criar o projeto. Se sim, digite `yes` no terminal.

Com isso, será criado um arquivo chamado `package.json` que é o coração da aplicação Node.js, pois nele definimos todas as dependências da API.

### 4.1. Configurando o Node JS

Após a criação do projeto, é recomendado instalar algumas depêndencias que melhoram a experiência da utilização do Node, facilitando em diversos aspectos, como por exemplo, simplificar a utilização de querys para requisições no banco.

As dependências recomendadas são:

**Express:** Poderoso gerenciador de rotas focado em alta performance, que simplifica requisições HTTP.
``` bash
    $ npm install express --save
```

**Body-parser:** Facilita a captura dos objetos que são passados ou recebidos na sua requisição HTTP.
``` bash
    $ npm install body-parser --save
```

**Morgan:** Gera logs de requisição para melhor acompanhamento das rotas.
``` bash
    $ npm install morgan --save
```

***Nodemon:*** Recarrega automaticamente o seu servidor, poupando o trabalho de reiniciá-lo sempre que houver alguma modificação.
``` bash
    $ npm install nodemon --save
```

O comando `--save` presente nestes comandos citados acima salva todas as dependências instaladas no `package.json`, facilitando o compartilhamento do código posteriormente. Para um terceiro instalar essas dependências do projeto, basta digitar o comando:
``` bash
    $ npm install
```

#### 4.1.1 Criando um servidor

Após os passos acima, você já é capaz de criar sua API. Mas para isso, é necessário criar o servidor para iniciar os procedimentos.

Devemos criar um arquivo na pasta raiz para rodar nossa aplicação. Neste exemplo usaremos o nome `app.js`.

Inicialmente, é preciso importar as depêndencias que serão necessárias para rodar o servidor. A importação é feita com o método `require` do Node.

``` javascript
    var express = require('express')
    var bodyParser = require('body-parser')
    var morgan = require('morgan')
```

Após isso, devemos evocar a função para utilizar os objetos do express em si.
``` javascript
    var app = express()
```

No fim, devemos subir o servidor utilizando nossa variável `app`. Para isso, passamos a porta que o servidor vai escutar e uma função que vai ser chamada assim que o servidor estiver no ar, como é mostrada no código abaixo.
``` javascript
    app.listen(3000, function() {
        console.log('Servidor rodando no endereço http://localhost:' + 3000)
    })
```

Após isso, seu servidor estará pronto para ser utilizado.

Utilize o comando abaixo para rodar o seu servidor.
``` bash
    $ node app
``` 

### 4.2. Configurando o RethinkDB

Uma tecnologia auxiliar ao RethinkDB que nos permite criar models e facilita nas queries é o Thinky, o qual utilizamos para configurar a base de dados.
Para instalar o Thinky, faça: 
``` bash
    myAPI-$ npm install --save thinky
``` 

Com isso, crie uma pasta com o nome `database` e configure o arquivo de banco de dados chamado `index.js`.

``` javascript
    //Path: myAPI/database/

    var thinky = require('thinky')()
    var { type, r } = thinky // importa 'type' para tipos de variáveis e 'r' como o próprio módulo do RethinkDB

    function init () {
      return new Promise((resolve, reject) => {
        thinky.dbReady().then(() => {
          resolve(thinky)
        })
      })
    }
    export { init, thinky, type, r }

```


## 5. Bibliografia

* http://nodebr.com/o-que-e-node-js/
* https://pt.stackoverflow.com/questions/80601/o-que-é-a-programação-orientada-a-eventos
* https://www.rethinkdb.com/faq/
* https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions