# Teste Automatizado

# Objetivo

Esse documento irá tratar de instruções para a realização de um pequeno teste automatizado em um site genérico utilizando Selenium IDE.

## Introdução

O controle da qualidade em um produto de software não é fácil de ser controlado, visto a complexidade atribuída a certos produtos de software, sendo necessário sempre atender a visão do cliente ao software. Os testes unitários testam parte do código, normalmente testam funções separadamente. O teste automatizado ou teste aceitação realiza o teste no software na visão do cliente, concluindo as etapas realizadas pelo usuário.
    
## O que o teste irá fazer ?

O objetivo do teste:
Realizar busca de uma matéria em um site.
Site:
Wikipedia
Objetivo principal:
Achar o artigo relacionado a testes em geral
Passos:
* Abrir o site.
* Colocar no campo de buscas o valor: “Testes”. 
* Pressionar o botão de pesquisa.
* Verificar os dados da página.

## Ferramenta

A ferramenta escolhida é a “Selenium IDE” que é uma ferramenta que funciona diretamente no Firefox na forma de plugin. Os motivos de escolha dessa ferramenta são:
* Facilidade de uso.
* Facilidade de exportar código de teste para outras linguagens.
* Opção de gravar o teste.
* Executado diretamente no navegador.

## Instalação

Para a instalação do Selenium IDE é necessário ter o Firefox instalado na máquina, se não já o tiver faça o download e instale-o pelo site: http://br.mozdev.org/firefox/download/

Após ter instalado o Firefox, é necessário instalar o plugin do Selenium IDE pelo site: 
https://addons.mozilla.org/en-US/firefox/addon/selenium-ide/

Clique no botão Add to Firefox


Após reiniciar o navegador pressione Ctrl + Alt  + S para iniciar o plugin Selenium IDE

A seguinte janela deverá aparecer:



## Realizando o caso de teste