# Orquestração de Containers com Docker Compose

O docker compose é uma ferramenta para orquestrar e executar diversos container [docker](https://www.docker.com/). Auxilia na organização evitando imensas linhas de comando docker com muitas passagens de parâmetros. 

O compose usa um arquivo de configuração chamado `docker-compose.yml`, nesse arquivo define-se os serviços que serão levantados pelo compose. Os serviços usam uma imagem base, podendo ser criada a partir de um `Dockerfile` ou baixada do [docker hub](https://hub.docker.com/). Veja o exemplo abaixo:

```yml
version: '3'

services:
  redis:
    image: .
    ports:
      - "6379:6379"
```
No exemplo, cria-se um serviço `redis` utilizando o `Dockerfile` que se encontra na mesma pasta que o docker-compose.yml indicado pelo caractere `.`. Poderia-se também utilizar a imagem oficial do redis disponivel no docker hub, basta substituir o `image: .` por `image: redis`, onde o redis na chave refere-se ao nome da imagem.