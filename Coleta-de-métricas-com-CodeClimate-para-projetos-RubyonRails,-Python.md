
##CodeClimate

Ferramenta de análise estática de código bastante utilizada pelos desenvolvedores rubyonrails. O codeClimate analisa vários aspectos do projeto, e classifica o projeto segundo um indice. 
Dentre os recursos disponíveis destacam-se

* Análise de complexidade

* Branches

* Complexidade por método

* Duplicação de código

* Quantidade de modificações no arquivo

* Quantidade de linhas de código

* Checagem de segurança

* Possui integração com o Travis

A cada commit, o CodeClimate oferece um feedback a respeito da situação atual, informando se o indice subiu ou desceu.

Passo a Passo de como adicionar o CodeCLimate ao projeto.

__1 - Acessar o site https://codeclimate.com/__

__2 - Clicar na opção Get Started Free with GitHub__

__3 - Preencher a janela de login do github com sua conta__

__4 - Clicar na opção Add Open Source Repo__

__5 - Prencher formulário com o caminho/nome do projeto, Exemplo nicacioneto/colchonet__

Após seguir todos os passos o CodeClimate já estará funcionando e analisando o projeto, após a análise, será disponibilizado um índice de qualidade do projeto.

O CodeClimate oferece suporte as linguagens

* CSS
* Go
* JavaScript
* PHP
* Python
* Ruby

__6- Visualização dos resultados__

Para verificar o resultado das métricas coletadas, basta acessar o [site](http://codeclimate.com/) do Code Climate, realizar o _login_ com sua conta o _Github_ e adicionar o repositório desejado. A lista de repositórios adicionados aparecerá para o usuário. 

Clicando no repositório desejado, será mostrada um _feed_ com as últimas atualizações relacionadas as métricas do repositório (por exemplo, caso a cobertura de testes aumentem, a atualização será mostrada nesta tela). Nesta mesma tela, é possível visualizar o _score_ final da avaliação das métricas, indo de 0.0 a 4.0. 

Ao clicar na aba `code`, é possível visualizar todos os arquivos e suas respectivas informações relacionadas à quantidade de linhas de código, número de vezes que o arquivo foi modificado até a data da última coleta de métricas e o número de _issues_ do arquivo (estas _issues_ significam que existem blocos de código duplicados em mais de um arquivo, por exemplo). 

Ao clicar na aba `issues` é possível visualizar quais arquivos tem métodos ou blocos de código duplicados. Já na aba `trend` é possível visualizar novamente o _score_ final da avaliação das métricas e, mais importante, é possível visualizar o gráfico __churn vs. quality__, onde é mostrada a comparação entre a quantidade de vezes que o arquivo foi modificado e a qualidade de cada arquivo.

Para mais informações acesse a documentação oficial
https://docs.codeclimate.com
