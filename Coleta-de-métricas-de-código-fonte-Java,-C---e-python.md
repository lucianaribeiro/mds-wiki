#1. Analizo

##1.1. Instalação

Esta instalação está disponível em inglês na página [https://github.com/analizo/analizo/blob/master/INSTALL.md](https://github.com/analizo/analizo/blob/master/INSTALL.md).

###Pacote Debian

1) Crie um arquivo "analizo.list" na pasta /etc/apt/sources.list.d/

```
cd /etc/apt/sources.list.d/
gedit analizo.list
```

O arquivo se abrirá no editor de texto, adicione as linhas:

```
deb http://analizo.org/download/ ./
deb-src http://analizo.org/download/ ./
```

Salve e feche o editor de texto.

2) Adicione a chave de assinatura do repositório para sua lista de chaves confiáveis:

```
# wget -O - http://analizo.org/download/signing-key.asc | apt-key add -
```

3) Atualize a lista de pacotes:

```
$ apt-get update
```

4) Instale o analizo:

```
$ apt-get install analizo
```
