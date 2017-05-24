# Integração Contínua

## Introdução

## Controle de Versão

## Testes Automatizados

## Build Automatizado

## Vantagens da Integração Contínua

## Integração Contínua com o Travis

O seguinte tutorial objetiva exemplicar de maneira clara os passos necessários para implementar o Travis-CI em repositório com o intuito de realizar a integração contínua no mesmo.

1. Acessar travis-ci.org e fazer fazer cadastro autorizando a vinculação com o GitHub

2. No página de perfil do Travis acesse o '+' para habilitar o travis em um novo repositório

3. Habilite o travis no repositório desejado

4. Na raiz do seu repositório, crie o arquivo .travis.yml

Um exemplo do conteúdo do arquivo é:

```yml
  language: ruby
  services:
  - mysql
  before_script:
  - cp 2017.1-SIGS/SIGS/config/database.yml.travis 2017.1-SIGS/SIGS/config/database.yml
  - mysql -e 'create database myapp_test;' -uroot
  script:
  - cd 2017.1-SIGS3/SIGS
  - bundle install
  - bundle exec rake db:load_config
  - bundle exec rake db:create
  - bundle exec rake db:migrate
  - rake cucumber
  - bundle exec rspec
  - rubocop
  after_sucess:
  - coveralls push
  rvm:
  - 2.3.1
  notifications:
    email:
      recipients:
      - email@example.com
  branches:
    only:
    - master
    - /.*/
```

* **language:** linguagem do projeto<br>[Lista das lingagens aceitas pelo Travis](https://docs.travis-ci.com/user/languages)
* **services:** serviços que serão utilizados pelo Travis

* **before_script:** comandos que devem ser executados antes de rodar o script

* **script:** comandos para executar os testes

* **after_sucess:** comando a ser executado após a finalização dos testes

* **notifications:** configuração de notificações que podem ser associadas ao Travis.<br>[Lista de Notificações](https://docs.travis-ci.com/user/notifications/)

* **branchs:** definição das branchs em que serão rodado os testes
