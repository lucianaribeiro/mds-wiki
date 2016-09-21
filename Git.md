# Instalando e configurando o Git

Antes de utilizarmos o Git, é fundamental instalá-lo. Escolha a seguir o Sis-
tema Operacional apropriado e mãos à obra!

## Instalando no Windows

Acesse a seguinte URL, faça o download e instale a última versão dispo-
nível: http://msysgit.github.io/

A instalação é bastante simples. Escolha as opções padrão. Serão instalados alguns programas, sendo o mais importante o Git Bash, que permite que o Git seja executado pela linha de comando no Windows.
Dê duplo clique no ícone do Git Bash e será aberto um terminal, com o seguinte prompt na linha de comando:

``$``

Esse prompt será seu amigo a partir de agora. Não tenha medo! Sempre que falarmos de terminal, estaremos falando do Git Bash.

## Instalando no Mac

Baixe a última versão do instalador gráfico do Git para Mac OS X a partir do link: https://code.google.com/p/git-osx-installer/downloads

Abra um terminal e prepare-se para utilizar o Git!

## Instalando no Linux

Para instalar o Git no Ubuntu, ou em uma outra distribuição baseada em Debian, execute em um terminal:

``$ sudo apt-get install git``

No Fedora, utilize:

``$ sudo yum install git``

Para as demais distribuições do Linux, veja o comando em: http://git-scm.com/download/linux

## Configurações básicas

É importante nos identificarmos para o Git, informando nosso nome e e-mail. Em um terminal, execute os comandos a seguir:

``$ git config --global user.name "Fulano da Silva"``

``$ git config --global user.email fulanodasilva.git@gmail.com``

Claro, utilize seu nome e e-mail!

# Criar um repositório

O primeiro passo para trabalhar com Git é criar um repositório. Para isso, basta rodar o comando 

``$ git init NOME_DO_REPOSITORIO``

Exemplo:

``$ git init games`` cria a pasta chamada games, que é um repositório Git.

# Adicionar arquivos

Do ponto do vista do Git, existem quatro estados no qual um determinado arquivo pode estar.

*  Commited: O arquivo está sob controle de versão e não apresenta nenhuma modificação.

*  Commit candidate: Caso você crie um conjunto de modificações (commit), esses serão os arquivos incluídos.

*  Modified: Arquivos que foram modificados.

*  Untracked: Arquivos novos, que ainda não estão no controle de versão.

Para mudar um arquivo de untracked ou modified para Commit candidate, você usa o comando git add CAMINHO. O git add é inteligente, então se você passar um caminho parcial para ele, ele muda o estado de todos os arquivos que contém esse caminho parcial.

Exemplo:

* ``$ git add . `` mudaria o estado de todos os arquivos a partir do diretório atual.

* ``$ git add arquivo.txt `` mudaria o estado do arquivo arquivo.txt

* ``$ git add pasta `` mudaria o estado do arquivo pasta/arq1.txt e do pasta/arq2.txt, mas não mudaria do outra_pasta/arq1.txt

# Fazer Commits

Agora que você já sabe como selecionar as modificações que quer incluir em um pacote de modificações (um commit), chegou a hora de aprender como gerar esse pacote. 
O comando utilizado para criar um commit em git é *git commit*. Com esse comando, todos os arquivos que estiverem marcados como Commit candidate serão incluídos no commit. Se você também quiser incluir os arquivos que estão marcados como modified, você pode incluir a flag *-a*.

Uma coisa muito importante de qualquer commit é uma mensagem que explique o que significa aquele commit. Para isso, você pode passar a opção *-m "mensagem de commit" *. Caso você não passe, o git vai abrir um editor de texto para que você digite a mensagem.

Exemplo:

`` $ git commit -m "commit" `` cria um commit com todos os Commit candidate e a mensagem *commit*

`` $ git commit -a -m "segundo commit"`` cria um commit com os arquivos marcados como Commit candidate e os modified e junta com a mensagem *segundo commit*

Uma outra possibilidade para commit utiliza da flag ``-s``. Essa flag permite que o mesmo commit tenho vários autores, ou seja, você e outro desenvolvedor podem coolaborar para um mesmo fim e commitarem "juntos".  
  
É importante lembrar que esse tipo de commit leva em consideração o usuário configurado no git como principal e dá status de coolaborador para os demais.  
  
Para usar essa flag basta digitar, ``git commit -s``.   
Com Enter pressionado você será redirecioado para seu editor de texto padrão, visualizando algo semelhante:  

![Commit em grupo](https://raw.githubusercontent.com/wiki/fga-gpp-mds/00-Disciplina/img/commitGrupo.png) 

Na primeira linha insira um **Título** para o commit.  
Na segunda linha **descreva** um pouco melhor as alterações.  
Para adicionar os **coautores**, basta copiar a linha, ``Signed-off-by`` e colar na linha abiaxo mudando os dados necessários.  
    
Feito isso basta salvar o arquivo e seu commit será efetuado com sucesso.  

# Enviar commits para um repositório

Para enviar os commits feitos para o repositório desejado, utiliza-se o comando `push`. Este comando tem a seguinte assinatura: __`git push local_remote_name remote_branch_name`__, onde __`local_remote_name`__ indica o nome do repositório local em que o repositório git se encontra e __`remote_branch_name`__ indica o nome da branch em que deve ser enviado o conjunto de commits.

# Plataforma de Exemplo

Para exercitar e fixar os conhecimentos de Git, utilize a plataforma [Learn Git Branching](http://learngitbranching.js.org/)

# Referências

[Controlando versões com Git e GitHub - Casa do Código](https://github.com/brunoipjg/myEbooks/blob/master/Controlando%20vers%C3%B5es%20com%20Git%20e%20GitHub%20-%20Casa%20do%20Codigo.pdf)