[Configuração de Ambiente](#configuração-de-ambiente)

[DOJO de linguagem](#dojo-de-linguagem)

[DOJO de testes ](#dojo-de-testes)

[Repositórios educativos](#repositórios-educativos)

[Material didático produzido na disciplina ](#material-didático-produzido-na-disciplina)

-----
# Configuração de Ambiente
<p align = "justify">*Android* é o sistema operacional de código aberto desenvolvido pela *Google*, para ser utilizado majoritariamente em despositivos com tela touchscreen, como
smarthphones ou tablets. A criação de aplicativos para este sistema é feita em _Java_ utilizando-se de um kit de desenvolvimento (SDK)
 específico. Além disso, normalmente se utiliza uma IDE específica, o *Android Studio*. É de extrema **importância** que todos os integrantes da equipe tenham a mesma configuração de ambiente para que não haja incompatibilidade entre versões diferentes das ferramentas usadas, que podem comprometer o desenvolvimento do software.
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

##Observação Importante!

Ficar sempre atento às configurações do gradle tanto no seu app, quanto na sua IDE. Elas podem afetar significativamente os resultados de teste e deploy. Tente definir uma config padrão para todo o grupo o mais cedo possível.

# Arquitetura MVC Android 

# DOJO de linguagem 

**1)** Curso completo da plataforma [Udacity](https://www.udacity.com) sobre _Android_:

* **Tais cursos apresentados nesta plataforma são bastante completos e de alta qualidade, contudo bastante extensos. Logo, demanda-se uma quantia considerável de tempo para completá-los com eficácia e obter o resultado esperado.**

        https://www.udacity.com/courses/android

**2)** Sugestões de aprendizado direcionado na plataforma [Udacity](https://www.udacity.com):

* **Indicado para um desenvolvimento aceitável em _Android_:**
 
  Desenvolvimento intermediário de _Android_ (_Gradle, Layout, Intent,_ Banco de Dados, Testes e outros):

      https://br.udacity.com/course/developing-android-apps--ud853/

  Material _Design_ para _Android_:
    
      https://br.udacity.com/course/material-design-for-android-developers--ud862/

* **Indicado como um complemento, mas fortemente recomendado para um desenvolvimento aceitável em _Android_:**
 
  Desenvolvimento inicial de _Android_ (_XML_ e básico do _Framework_):

      https://br.udacity.com/course/android-development-for-beginners--ud837/

  _Login_ do _Google_ para _Android_:
    
      https://br.udacity.com/course/add-google-sign-in-to-your-android-apps--ud876-5/

* **Indicado para quem deseja aprofundar-se em _Android_:**
 
  Desenvolvimento avançado de _Android_ (_Libraries, localization,_ Material _Design_):

      https://www.udacity.com/course/advanced-android-app-development--ud855

  Outros tópicos (Sistemas de controle, menu, _layout_, entrada e saída):
    
      https://br.udacity.com/course/how-to-create-anything-in-android--ud802/

# DOJO de testes 
(material didático)

# Repositórios educativos


# Material didático produzido na disciplina 
(times, coaches, etc)