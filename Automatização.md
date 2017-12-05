### Integração Contínua (Travis - Docker - Docker-Compose)

No arquivo .travis.yml é necessário configurar o docker e o docker-compose.

* Passo 1: Defina os serviços utilizados, no caso o docker:

```
services:
  - docker
```

* Passo 2: Defina a versão do docker-compose a ser instalada:

```
env:
  - DOCKER_COMPOSE_VERSION=1.15.0
```

* Passo 3: Instale o docker-compose na integração contínua:

```
before_install:
  - sudo rm /usr/local/bin/docker-compose
  - curl -L https://github.com/docker/compose/releases/download/${DOCKER_COMPOSE_VERSION}/docker-compose-`uname -s`-`uname -m` > docker-compose
  - chmod +x docker-compose
  - sudo mv docker-compose /usr/local/bin
```

* Passo 4: Crie os containers e execute os scripts necessários de build/testes:

```
script:
	- docker-compose up --build -d
		...
```
### Deploy (Heroku)

Após ter feito as configurações de integração contínua, caso deseje utilizar o heroku para deploy, é necessário, primeiramente, criar uma conta no heroku. Com isso feito é preciso criar uma aplicação. 

* Passo 1: Na dashboard do heroku selecione a opção "New" e depois "Create new App":

![Image]()

* Passo 2: Digite o nome do seu app e selecione a região, por default será United States

![Image]()

* Passo 3: Verifique qual a api-key do usuário, selecione "Account Settings" e clique em "Reveal"

![Image]()

* Passo 4: Agora no travis.ci, entre no local onde a integração contínua está configurada e selecione a opção "More Settings"

![Image]()

* Passo 5: Adicione a api-key do heroku como uma variável de ambiente, "Environment Variables":

![Image]()

* Passo 6: Configure o arquivo .travis.yml com deploy, onde o provider é o heroku que já é integrado com o travis, a api-key é a variável de ambiente do usuário criador do app, o app é aquele criado no heroku e a branch a ser executada o deploy, normalmente a master. Exemplo:

```
deploy:
  provider: heroku
  api_key: $SECRET_USER_KEY
  app: exemplo-gpp-mds
  on: master
```

Observações:

* Existem particularidades de linguagens específicas, e essas nuâncias não foram abordadas nesse documento.

#### Gulp

O Gulp é uma ferramenta de automação de tarefas feita em JavaScript e rodando em cima do Node.js. Como o core da execução é o Node, precisamos começar nossos trabalhos definindo o arquivo de vai gerenciar os módulos gulp que você utilizará no seu projeto(Caelum).

##### Sincronização com o *Browser*

Os arquivos estáticos mudam constantemente e existe uma dificuldade de atualização dos arquivos no *browser*, simplesmente para modificações de arquivos html, js e css é necessário um dar *reload* na página utilizada. Normalmente, os arquivos se mantém em cache e é comum que estes continuem na versão anterior. O gulp juntamente com o browser-sync oferece uma solução para isso. Onde arquivos ou pastas são observadas e quando são atualizadas a página em questão é recarregada. Portanto, é mais simples para em ambiente de desenvolvimento, principalmente, com a utilização de frameworks web como o rails e o django. Não se preocupando com atualização dos arquivos estáticos no navegador. Abaixo existe um exemplo de como configurar arquivos a serem observados e auto-sincronizar com o gulp.

**gulpfile.js**

```
'use strict';

// Indica as dependências necessárias 
var gulp = require('gulp');
var browserSync = require('browser-sync').create();

// Define o diretório a ser utilizado
var directoryjs = './*.js'

// Por padrão, o gulp executa um server utilizando a porta 3000
// Abaixo existe a definição das configurações do servidor, sendo que  o proxy será incluido no localhost:3000
// Onde a porta 8000 é o padrão do django
gulp.task('browserSync', function() {
  browserSync.init({
    open: false,
    notify: false,
    proxy: 'localhost:8000'
  })
});

// Define os arquivos a serem observados e caso haja modificação nesses arquivos,
// o browser será recarregado
gulp.task('watch', function() {
  gulp.watch(directoryjs, browserSync.reload);
});

// É a função principal, como a main em c, onde é executado o restante das funções
gulp.task('default',['browserSync', 'watch']);

```