# Introdução
O teste de aceitação é uma parte fundamental para projetos ágeis. Nessa metodologia os testes são escritos em linguagem natural para alinhar as expectativas do cliente e da equipe de desenvolvimento. Os teste de aceitação eram necessariamente - e devem continuar sendo - feitos pelo cliente em um ambiente próximo do de produção, porém, a equipe de desenvolvimento pode implementar esse tipo de teste em código para ser reproduzível e capaz de medir os efeitos de mudanças solicitadas pelo cliente. Algumas ferramentas foram, portanto, desenvolvidas para automatizar a criação de suítes de teste de aceitação. O projeto aloe permite aos desenvolvedores utilizar linguagem natural para escrever testes que depois são traduzidos em comandos para o selenium. O Aloe permite que novos comandos - chamados steps - sejam criados para se adequar a especificidades do projeto em teste. O selenium, por sua vez, permite que diferentes browser sejam utilizados para se realizar os testes. 

O tutorial abaixo irá ensinar como configurar as ferramentas aloe e selenium para desenvolver testes de aceitação para projetos django. Iremos considerar que o usuário está utilizando um ambiente virtual para projetos python e a versão do python seja superior a 3.4. 

### Parte 1 - Criando e Instalando Dependências
1- Criar uma pasta para o projeto

2- Iniciar o ambiente virtual

3- Instalar o django no ambiente virtual

4- Criar um projeto

      django-admin startproject projectname

5- Instalar o selenium, dentro do projeto criado

      pip install selenium
6- Instalar o django_nose

      pip install django_nose
7- Instalar o aloe

      pip install aloe_django
8- Instalar o aloe web driver

      pip install aloe_webdriver
9- Editar o arquivo settings.py e acrescentar o django nose e o aloe django

      INSTALLED_APPS = [
			‘django_nose’
			‘aloe_django’
		       ]
10- Na pasta onde estão as configurações do projeto, criar uma pasta chamada "steps"
      
      mkdir steps
11- Entrar na pasta criada

      cd steps
12- Criar um arquivo chamado browser.py com o seguinte conteúdo

![12](https://raw.githubusercontent.com/wiki/fga-gpp-mds/00-Disciplina/img/selenium_12.png)

13- Para criar as suas próprias steps crie o arquivo steps.py que deve comecar da seguinte forma:

![13](https://raw.githubusercontent.com/wiki/fga-gpp-mds/00-Disciplina/img/selenium_13.png)
