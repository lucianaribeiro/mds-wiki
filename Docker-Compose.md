# Orquestração de Containers com Docker Compose

## Sobre o Docker Compose
O docker compose é uma ferramenta para orquestrar e executar diversos container [docker](https://www.docker.com/). Auxilia na organização evitando imensas linhas de comando docker com muitas passagens de parâmetros. 

## Configuração
### O arquivo yml
O compose usa um arquivo de configuração chamado `docker-compose.yml`, nesse arquivo define-se os serviços que serão levantados pelo compose. Os serviços usam uma imagem base, podendo ser criada a partir de um `Dockerfile` ou baixada do [docker hub](https://hub.docker.com/). Veja o exemplo abaixo:

```yml
version: '3'

services:
  redis:
    image: .
    ports:
      - "6379:6379"
```
No exemplo, cria-se um serviço `redis` utilizando o `Dockerfile` que se encontra na mesma pasta que o docker-compose.yml indicado pelo caractere `.`. Poderia-se também utilizar a imagem oficial do redis disponivel no docker hub, basta substituir o `image: .` por `image: redis`, onde o valor `redis` na chave refere-se ao nome da imagem.

### portas
A comunicação com um container é normalmente feita via porta exposta. No exemplo acima, a porta `6379` do container é mapeada para a porta de mesmo número do `host`. Isto significa que ao acessar a porta 6379 no localhost o conteúdo apresentado refere-se à aplicação em execução no container. 

A ordem de mapeamento é sempre a porta do host para a do container `"host:conatainer"`.

### volumes
```yml
services:
  nginx:
    image: nginx
    ports:
      - "80:80"
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf:ro
```
### depends_on
```yml
  web:
    build: .
    ports:
      - "8000:8000"
    depends_on:
      - redis
```

### command
```yml
  web:
    build: .
    command: python3 manage.py runserver 0.0.0.0:8000
```

### environment
```yml
postgres:
    image: postgres
    environment:
        POSTGRES_PASSWORD: 1234
        POSTGRES_DB: postgres
        POSTGRES_USER: eu
```

## Executando o Docker Compose
Após configurado o docker-compose.yml, pode-se executar e subir todos os serviços com o comando:
```
docker-compose up
```

### Comandos úteis:
- `docker-compose up` : Constrói as imagens, (re)cria, inicia e anexa containers a um serviço. A flag `-d` executa os cantainers em segundo plano. 
- `docker-compose down` : Termina a execução dos containers, os remove e remove networks e volumes criados por `up`. 
- `docker-compose stop` : Termina a execução dos containers sem removê-los. 
- `docker-compose start` : Inicia containers existentes para um serviço. 
- `docker-compose logs` : Exibe saída de log dos serviços, a flag `-f` segue a saída de log. 
- `docker-compose exec web bash` : Executa o comado `bash` no serviço `web`. 

Obs: Estes comandos exigem sudo, a menos, que tenha configurado para que não.