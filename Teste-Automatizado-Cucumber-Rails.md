## Execução

Para iniciar os testes, deve-se criar o arquivo contendo os testes a serem realizados. O nome do arquivo deve ser NomeDaFuncionalidadeTestada.feature. Deve necessariamente terminar em “.feature”. Esse arquivo conterá os cenários de teste escritos, estruturando-se em:

__Feature__: (nome do arquivo. Exemplo do projeto: registration_member)

__Background__ (opcional): É uma forma de setup. De forma geral, o que estiver contido no background rodará antes de executar cada um dos outros testes, de forma a criar condições específicas.

__Scenario__: É o teste em si. Consiste de vários steps (passos) que indicam a ocorrência de algo no sistema. Se os passos são seguidos corretamente, o teste passa e a funcionalidade está de acordo com o escrito.

Como exemplo de um arquivo “.feature”, pode-se mostrar parte de um teste de aceitação do projeto Owla, chamado “registration_member.feature”:

          Feature: registration_member

 	  Scenario: a user should be able to registrate
    		Given I go to /
    		When I click "Register yourself"
    		Then I should be in "/members/new"
    		When I write "Gabriel Alves" on "member_name"
    		When I write "gabriel@gmail.com" on "member_email"
    		When I write "gabi" on "member_alias"
    		When I write "testtest" on "member_password"
    		When I write "testtest" on "member[password_confirmation]"
    		When I click button "Register"
    		Then I should be in "Gabriel Alves" homepage
    		And the object with attribute "name" and value "Gabriel Alves" of "member" klass was created

Nesse teste, não há a presença de um background. Porém, um _background_ seria a mesma coisa de um cenário, sem a presença da descrição presente na linha do _scenario_. Porém, apenas isso não é suficiente para que o teste rode sem problemas. Cada um dos _steps_ deve ser definido em outro arquivo, para que o sistema saiba que ações devem ser chamadas para cada passo. Deve-se criar um arquivo de definição de passos. No caso do projeto Owla, esse arquivo se chama web_steps.rb e está contido na pasta _step_definitions_. Seu conteúdo é o que se segue:

          Given(/^I go to (.+)$/) do |path|
           visit path
          end

          When(/^I click "(.+)"$/) do |link|
           click_link(link)
          end

          When(/^I click button "(.+)"$/) do |link|
            click_button(link)
          end

          Then(/^I should be in "(.+)"$/) do |page|
            assert current_path == page
          end

          Then(/^I should be in "(.+)" homepage$/) do |object|
            member = Member.find_by(name: object)
            assert current_path == "/members/#{member.id}/home"
          end

          Then(/^I should be in "(.+)" edit$/) do |object|
            member = Member.find_by(name: object)
            assert current_path == "/members/#{member.id}/home"
          end

          When(/^I write "(.+)" on "(.+)"$/) do |value, field|
            fill_in field, :with => value
          end

          Given(/^I have created "(.+)"$/) do |value|
            member = Member.create(name: "Victor Navarro", email: value, alias: "vivi",
            password: 'testtest', password_confirmation: 'testtest')
          end

          And(/^the object with attribute "(.+)" and value "(.+)" of "(.+)" klass was created$/) do |attribute, value, klass|
            object = klass.capitalize.constantize.find_by("#{attribute}": value)
            assert klass.capitalize.constantize.last.id == object.id
          end

Percebe-se que, nesse arquivo, contém “frases” com REGEX especiais que funcionam da seguinte forma: para cada step contido no arquivo de testes, o sistema procurará no arquivo de definição de steps um com a mesma “frase” de comando. Lá, ele encontrará a frase e o que dentro da frase é uma variável, que deve ser pega do arquivo de testes. Então, dentro do bloco de código presente na definição do step, ele implementará o que for especificado.
	É importante notar que há muitas funções referentes a clicar em botões, acessar links e páginas diferentes para auxiliar o desenvolvedor na hora de criar os testes. Apenas a pesquisa pode mostrar todas as funções, mas há sites que tentam fazer um resumo delas, como:
                        
                   https://gist.github.com/zhengjia/428105
