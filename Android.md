# Configuração de Ambiente
*Android* é o sistema operacional de código aberto desenvolvido pela *Google*, para ser utilizado majoritariamente em despositivos com tela touchscreen, como
smarthphones ou tablets. A criação de aplicativos para este sistema é feita em _Java_ utilizando-se de um kit de desenvolvimento (SDK)
 específico. Além disso, normalmente se utiliza uma IDE específica, o *Android Studio*.

Configurar o ambiente do Android Studio requer alguns passos.

Linux (64-bits):

**Passo 1:** Instale o kit de desenvolvimento java:

**1)** Via terminal, adicione o repositório PPA com o seguinte comando:

    sudo add-apt-repository ppa:webupd8team/java

**2)** Atualize os pacotes disponíveis em seus repositórios:

    sudo apt-get update

**3)** Instale o kit de desenvolvimento:

    sudo apt-get install oracle-java8-installer

**4)** Defina o SDK da Oracle como o kit padrão a ser utilizado:

    sudo apt-get install oracle-java8-set-default

**5) Se o seu sistema for de 64 bits, instale as bibliotecas de 32 bits :**

    sudo apt-get install lib32z1 lib32ncurses5 lib32ncurses5-dev lib32stdc++6


**Passo 2:** Instale o ubuntu-make:

O ubuntu make é uma ferramenta de linha de comando a qual permite baixar e atualizar plataformas de desenvolvimento de software com mais facilidade.

**1)** Adicione o repositório PPA para instalar a última versão do ubuntu-make com o seguinte comando:

    sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make

**2)** Atualize os pacotes disponíveis em seus repositórios:

    sudo apt-get update

**3)** Instale o ubuntu-make

    sudo apt-get install ubuntu-make

**Passo 3:** Instalar o Android Studio

**1)** Com o ubuntu-make instalado, basta utilizar o seguinte comando:

    umake android

**2)** Após o termino do download, basta executar o programa Android Studio presente na máquina. Este irá realizar o download do kit de desenvolvimento
Android. Quando finalizado, o Android Studio estará pronto para ser utilizado.

# DOJO de linguagem (material didático)



# DOJO de testes (material didático)


# Repositórios educativos


# Material didático produzido na disciplina (times, coaches, etc)