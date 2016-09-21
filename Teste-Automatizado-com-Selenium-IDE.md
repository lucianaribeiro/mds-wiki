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

No campo “URL Base” digite: http://www.wikipedia.org
Selecione o comando open com alvo barra se já não estiver na tabela do teste.

Pressione com o botão direito na aba de test case o primeiro teste. Clique em propriedades. Troque o nome do caso de teste por : “Pesquisa no Wikipedia”.

Agora que já temos o comando open de abrir a página, precisamos colocar o que queremos pesquisar no campo de busca.
Para isso na aba de comandos do Selenium IDE selecione o do tipo type. Pressione o botão Select e com a página do Wikipedia aberta clique no campo de busca. Agora vamos colocar o valor que queremos procurar, Digite no campo valor: “TESTE”. 

Por fim precisamos pressionar o botão de pesquisa para pesquisar efetivamente. Em comando coloque clickAndWait, pressione Select no alvo e clique em cima do botão de pesquisa na página do wikipedia.

Após isso precisamos verificar se a página carregada corresponde a página que queremos, assim teremos certeza que o teste passou. Para isso coloque em comando assertText, em alvo clique em Select e pressione no Título da página, e no valor coloque Teste.

A página do Selenium IDE fica da seguinte forma:


Após isso é necessário apenas apertar “play” para todos os casos de teste.
A página irá ser preenchida automaticamente e o resultado será exibido e o teste será concluído.

## Código do teste

Código gerado no tutorial, para usa-lo basta clicar na aba “código fonte” e colar esse código lá.

`
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head profile="http://selenium-ide.openqa.org/profiles/test-case">
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<link rel="selenium.base" href="https://www.wikipedia.org/" />
<title>New Test</title>
</head>
<body>
<table cellpadding="1" cellspacing="1" border="1">
<thead>
<tr><td rowspan="1" colspan="3">New Test</td></tr>
</thead><tbody>
<tr>
    <td>open</td>
    <td>/</td>
    <td></td>
</tr>
<tr>
    <td>type</td>
    <td>id=searchInput</td>
    <td>teste</td>
</tr>
<tr>
    <td>clickAndWait</td>
    <td>css=button.pure-button.pure-button-primary-progressive</td>
    <td></td>
</tr>
<tr>
    <td>assertText</td>
    <td>id=firstHeading</td>
    <td>Teste</td>
</tr>

</tbody></table>
</body>
</html>
`