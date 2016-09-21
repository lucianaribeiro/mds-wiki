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
![Add-to-firefox](http://postimg.org/image/7g6gxjjvj/)

Após reiniciar o navegador pressione: 
> Ctrl + Alt  + S 
Este comando irá iniciar o plugin Selenium IDE.

A seguinte janela deverá aparecer:
![Selenium-IDE-Interface.png](http://postimg.org/image/wvyczhvwh/)

## Realizando o caso de teste

No campo “URL Base” digite: http://www.wikipedia.org
Selecione o comando open com alvo barra se já não estiver na tabela do teste.

![Command-open.png](http://s9.postimg.org/tgd69adqn/Command_open.png)

Pressione com o botão direito na aba de test case o primeiro teste. Clique em propriedades. Troque o nome do caso de teste por : “Pesquisa no Wikipedia”.

Agora que já temos o comando open de abrir a página, precisamos colocar o que queremos pesquisar no campo de busca.
Para isso na aba de comandos do Selenium IDE selecione o do tipo type. Pressione o botão Select e com a página do Wikipedia aberta clique no campo de busca. Agora vamos colocar o valor que queremos procurar, Digite no campo valor: “TESTE”. 

Por fim precisamos pressionar o botão de pesquisa para pesquisar efetivamente. Em comando coloque clickAndWait, pressione Select no alvo e clique em cima do botão de pesquisa na página do wikipedia.

Após isso precisamos verificar se a página carregada corresponde a página que queremos, assim teremos certeza que o teste passou. Para isso coloque em comando assertText, em alvo clique em Select e pressione no Título da página, e no valor coloque Teste.

A página do Selenium IDE fica da seguinte forma:

![Selenium-IDE-Teste-Pronto.png](http://postimg.org/image/dz55bwm0d/)

Após isso é necessário apenas apertar “play” para todos os casos de teste.
A página irá ser preenchida automaticamente e o resultado será exibido e o teste será concluído.

## Código do teste

Código gerado no tutorial, para usa-lo basta clicar na aba “código fonte” e colar esse código lá.

> [Código do teste](http://textuploader.com/dsc25)