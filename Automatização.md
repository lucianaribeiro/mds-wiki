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

* Existem particularidades de linguagens específicas, e essas nuáncias não foram abordadas nesse documento.
