# **Responsáveis: SAAP+Observatório**

***


# Teste Unitário
http://www.extremeprogramming.org/rules/unittests.html

Este teste é utilizado para validar as classes básicas e os componentes do sistema que são considerados os menores elementos testáveis. Consiste em verificar se o fluxo de controle e dados estão corretos. Deve ser realizado no início da iteração.

* São escritos pelos desenvolvedores enquanto codificam o sistema.
* Devem ser feitos de modo que sejam fáceis de executar e e re-executar várias e várias vezes para validar o sistema.
* Devem ser criados para todas as classes do sistema.
* São implementados para todos os métodos do sistema.
* São escritos antes e ao decorrer da produção do sistema.
* Devem ser o mais simples possível.

Referência: [Desenvolvimento XP](http://xp.edugraf.ufsc.br/bin/view/XP/TesteAceitacaoXtesteUnidade)

# Teste Unitário Automatizado
# Stub

# Mock

# Boas práticas Testes Unitários

http://spring.io/blog/2007/01/15/unit-testing-with-stubs-and-mocks/

http://shipit.resultadosdigitais.com.br/blog/ruby-e-rspec-melhorando-a-legibilidade-de-seus-testes/

frameworks

# Desenvolvimento Orientado a Testes (TDD)

## Definição

_Test Driven Development_ (TDD), ou _Test-first development_, é um conjunto de técnicas de desenvolvimento orientado a testes associadas com _Extreme Programming_ (XP) e metodologia ágil. Com TDD temos um desenvolvimento incremental do código, iniciado pelos testes (Miller,2004). O programador deve ser capaz de escrever um código afim de satisfazer o teste escrito previamente. Dessa forma, possibilita-se a reflexão da modelagem antes de se escrever o código funcional. A consequência é um código fonte bem testado.  
TDD tornou-se uma das práticas mais populares entre os desenvolvedores de software.

## Ciclo de desenvolvimento orientado a Testes (TDD)

![Ciclo TDD](http://2.bp.blogspot.com/-O5F7OQeP6cY/VkYYHPNvd2I/AAAAAAAAAIw/eyuHiDRrzyM/s1600/TDD.png)

O ciclo do TDD é bem simples:

* Cria-se um teste.
* Executa-se o teste, que por sua vez irá falhar, pois a funcionalidade não foi implementada ainda.
* Codifica-se de modo a fazer o teste passar.
* Executa-se o teste novamente e, caso obtenha sucesso, prossiga para o próximo passo.
* Refatore o código.

## Pontos Positivos

###Qualidade do código
Um dos principais ensinamentos, senão o principal, do TDD é que se algo não é possível de ser testado então foi desenvolvido de forma errada. Parece um pouco drástico mas não é. Em pouco tempo utilizando testes o programador percebe mudanças relevantes em sua forma de programar. Em suma o uso de TDD ajuda o programador a elaborar um código com cada vez mais qualidade criando objetos concisos e com menos dependências.

###Raciocínio
Para que o código torne-se mais conciso, tenha menos acoplamentos e dependências o programador deve forçar seu raciocínio a níveis elevados. É muito difícil criar algo que realmente tenha um bom design. Utilizando TDD o programador praticamente obriga-se a olhar seu código de outra forma normalmente jamais vista antes. Aí é que está a parte legal da coisa toda.

###Segurança
Ponto importantíssimo para qualquer software nos dias de hoje. Mas não se engane, não estou falando de segurança da informação e sim de segurança ao desenvolver. Pense em uma situação em que o programador tenha um código que desenvolvera ha cerca de um ano. Como normalmente vivemos em um mundo com inúmeros softwares desenvolvidos ao longo de cada ano, torna-se muito difícil lembrar de tudo a respeito de um que merece nossa atenção em determinado momento. Normalmente deve-se realizar um trabalho bastante cauteloso para nova implementação em um software que encontra-se em produção. Toda e qualquer alteração deve ser minunciosamente testada e garantida que não afetará demais módulos do software. Fazer isto manualmente é realmente complicado pois até então não sabe-se (ou lembra-se) ao certo quem afeta quem no sistema. Com a prática de TDD cada pequeno passo do software está devidamente testado. Ou seja, com este cenário o programador pode realizar qualquer alteração sem medo e sem culpa.

Como cada pequeno passo tomado pelo sistema está testado ao qualquer módulo ou funcionalidade sofrer alteração, com poucos segundos descobre-se se houveram quebras e o melhor de tudo, onde foram essas quebras. Com isso em mãos a correção das quebras torna-se uma tarefa simples sem frustrar o cliente e o usuário.

###Trabalho em equipe
Por prover mais segurança o trabalho em equipe torna-se muito mais proveitoso eliminando discussões e dúvidas desnecessárias. Ao entrar no desenvolvimento do projeto o novo desenvolvedor tem apenas o trabalho de entender qual task deve ser realizada e ler os testes das features já desenvolvidas. Ao rodar os testes pela primeira vez o programador descobre se está no caminho de ter um entregável mais rapidamente e com segurança. Existem empresas em que um novo programador tem entregáveis logo no primeiro dia de trabalho. Sem testes normalmente haveria um período de adaptação para prévio entendimento do que há no sistema no momento de seu ingresso ao time de desenvolvimento.

###Documentação
Ao criar testes descritivos estes servem como uma excelente documentação para o software. Quando qualquer programador for rodar os testes, basta habilitar o modo verbose que uma “história” é contada eliminando o árduo trabalho de documentar um software onde nos meios tradicionais tende a defasar-se. O problema é que a documentação tradicional raramente segue o mesmo ritmo do desenvolvimento. Com os testes unitários a “documentação” é gerada antes mesmo da nova feature ser implementada e permanece fiel a qualquer alteração.

## Referências

[1] K. W. Miller,Test Driven Development on the Cheap:Text Files and Explicit Scaffolding. Disponível em http://www.ccsc.org/northwest/docarchive/2004/augustmailing2004final.doc  
[2] GASPARETO, Otávio. Test Driven Development. Universidade Federal do Rio Grande do Sul. Disponível em : http://www.inf.ufrgs.br/~cesantin/TDD-Otavio.pdf  
[3] TDD: fundamentos do desenvolvimento orientado a testes. Disponível em: http://www.devmedia.com.br/tdd-fundamentos-do-desenvolvimento-orientado-a-testes/28151. Acesso em: 10/11/2016.  
[4] Test-Driven Development. Disponível em: http://tdd.caelum.com.br/. Acesso em: 10/11/2016  


# Treinamento TDD

- Incluir descrição do treinamento/DOJO - passo a passo - etapas
- Registrar os detalhes da dinâmica
- Infraestrutura Necessária para a dinâmica
- Código referência no projeto da disciplina (00-Disciplina)
- Treinamento em, pelo menos 2 linguagens
