# BDD com o cucumber em JavaScript

## Objetivo

Este documento tem como objetivo principal criar um tutorial básico sobre o cucumberJS, ferramenta feita para desenvolvimento utilizando BDD (_Behaviour Driven Development_) em javascript.

## Introdução

Controlar se todos os critérios de aceitação de um sistema foram cumpridos nem sempre é uma tarefa fácil, e para simplificar esta tarefa, o BDD foi criado.
Neste tipo de teste o sistema é testado como um todo, sem considerar diferenças entre servidor e cliente, ou até mesmo banco de dados, garantindo assim que a funcionalidade como um todo funciona, porém nunca garantindo que ao encontrar um erro, torne mais fácil o _debug_.

## Objetivo do teste

O teste de exemplo para este tutorial será a funcionalidade do google de busca por um nome, sendo o caso de teste a busca da frase GPP/MDS e verificar se o github da disciplina é apresentado

## Instalação

### Pré requisitos:
- npm

### Preparação do teste

`npm init`

Serão apresentadas várias perguntas, aperte enter em todas =D.

`npm install --save-dev cucumber cucumberjs-chromedriver selenium-webdriver`

## Configuração dos testes

### Estrutura de arquivos

Os arquivos devem estar disponibilizados da seguinte forma

raiz<br>
|- tests<br>
_____|- features <br>
___________|-<files>.feature<br>
___________|-step_definitions<br>
____________________|-<file>_steps.js<br>
___________|-support<br>
____________________|-env.js<br>
____________________|-hook.js<br>
____________________|-world.js<br>
