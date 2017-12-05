# Integração Contínua (Travis - Docker - Docker-Compose)

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