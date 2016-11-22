# Framework XP

<p align = "justify">O XP, ou _Extreme Programming_, é uma metodologia de desenvolvimento de software que tem como objetivo principal levar ao extremo um boas práticas de programação e boas práticas para o desenvolvimento de software no geral. O XP é uma metodologia baseada em valores, que definem uma maneira harmoniosa de trabalho na equipe de desenvolvimento.

<p align = "justify"> O XP define uma série de regras para que o desenvolvimento seja realizado da melhor maneira possível: 

#### Planejamento:

- As histórias de usuário são escritas
- Sâo feitas _releases_ pequenas e constantes.
- O projeto é dividido em iterações.
- As iterações são planejadas no momento em que vai se começar o trabalho.

#### Gerenciamento:

- O time deve ter um espaço aberto de trabalho.
- O desenvolvimento deve ter uma velocidade sustentável.
- Stand-up meetings iniciam o dia de trabalho.
- O velocity é sempre medido.
- O XP deve ser consertado caso não esteja funcionando.

#### Design

- Simplicidade.
- Crie soluções simples para explorar todas as soluções possíveis.
- Funcionalidades não devem ser adicionadas antes da hora.
- Refatore sempre que possível

#### Códificação

- O cliente precisa estar sempre disponível.
- O código precisa ser escrito utilizando padrões.
- O código é feito utilizando pareamento (_pair programming_).
- Apenas um par integra o código de cada vez.
- Toda a equipe deve participar da criação de todas as partes do código.

#### Testes

- Todo o código deve ter testes unitários.
- Todo o código deve passar os testes unitários antes da _release_.
- Se um bug existe, testes são criados.
- Os testes de aceitação rodam com frequência.


<p align = "justify">Como podemos notar todas as práticas boas são levadas ao extremo no XP.
Pode-se se dizer que é uma metodologia bastante volátil, mas no bom sentido. Portanto, implica que para conseguirmos se adaptar as mudanças frequentes, o XP preconiza ciclos curtos que nos dá previsibilidade e redução de incertezas/riscos, Simplicidade e melhorias constantes de código (refactoring) para facilitar a mudança e Testes Automatizados e Integração Contínua para aumentar a confiança.

<p align = "justify">O método XP preconiza que Codificação é a atividade central do projeto, que os Testes (que também são código) servem de especificação de requisitos, e a Comunicação oral entre desenvolvedores é fundamental, o que dá proximidade a equipe.

<p align = "justify">Isto não quer dizer que a equipe XP não constrói documentos e não faz modelagem, ela só não considera que um modelo é um documento. Modelos são feitos o tempo todo seja como quadro branco, sessões de design, etc, mas servem como um suporte para o concreto que realmente importa.

# Valores XP
* **Comunicação**
* **Coragem**
* **Feedback**
* **Respeito**
* **Simplicidade**          

# Funcionalidade Pronta XP

## Teste Unitário
<p align="justify">Este teste é utilizado para validar as classes básicas e os componentes do sistema que são considerados os menores elementos testáveis. Consiste em verificar se o fluxo de controle e dados estão corretos. Deve ser realizado no início da iteração.

* São escritos pelos desenvolvedores enquanto codificam o sistema.
* Devem ser feitos de modo que sejam fáceis de executar e e re-executar várias e várias vezes para validar o sistema.
* Devem ser criados para todas as classes do sistema.
* São implementados para todos os métodos do sistema.
* São escritos antes e ao decorrer da produção do sistema.
* Devem ser o mais simples possível.

## Programação Pareada
<p align = "justify">Sugere que todo e qualquer código produzido no projeto seja sempre implementado por duas pessoas juntas, diante do mesmo computador, revezando-se no teclado. Além de parecer ter poucos benefícios, temos a impressão de que ela irá consumir mais recursos ou irá elevar o tempo do desenvolvimento. 

###Porque parear com o coleguinha?
**1** - A programação em par é uma forma eficaz de reduzir a incidência de bugs em um sistema. Quando dois desenvolvedores estão programando em par, um deles está com as mãos no teclado e no mouse. O outro está sentado ao lado, olhando para a mesma tela e preocupado em resolver o mesmo problema. É importante que eles conversem o tempo todo e troquem idéias sobre a solução.

**2** - A programação em par também ajuda os desenvolvedores a criarem soluções mais simples, mais rápidas de implementar e mais fáceis de manter. Isso ocorre em grande parte devido à oportunidade de dialogar e trocar idéias sobre programas que estejam sendo desenvolvidos. Quando nos deparamos com um problema, buscamos uma solução usando todo e qualquer recurso que esteja a nossa disposição. E, assim que encontramos uma solução, encerramos a busca e a utilizamos.

**3** - Além do mais, a programação em par produz um efeito conhecido como "pressão do par" que faz com que os desenvolvedores tenham maior foco na atividade e faz com que isso se mantenha por mais tempo. Imagine que você esteja programando em par e, de repente, resolva olhar seus emails. Trata-se de uma situação embaraçosa, isso faz com que o foco seja mantido no desenvolvimento.

**4** - Uma das características mais marcantes da programação em par é a sua capacidade de disseminação de conhecimento, especialmente em projetos XP, nos quais os desenvolvedores sempre trocam de pares, fazendo com que haja maior compartilhamento de informações ao longo do projeto.

**5** - A programação em par também é uma forma de fazer com que o desenvolvedor tenha mais confiança no código que produz. Afinal, o código foi produzido por ele e mais outra pessoa que o ajudou a revisá-lo. Quando sabemos que mais uma pessoa, ou talvez várias, já olharam para o código no qual trabalhamos e estão de acordo sobre o mesmo, temos maior confiança de que ele realmente irá funcionar. Isso significa que a programação em par reduz o estresse do desenvolvedor.

**6** - Consequentemente, as características apresentadas acima fazem com que a programação em par acelere o desenvolvimento significativamente, embora à primeira vista pareça o contrário. Em função dos benefícios acima, uma atividade feita em par normalmente é encerrada mais rapidamente que outra feita por um programador solitário, aumentando a produtividade.

Pair programming 
https://courses.edx.org/courses/course-v1:BerkeleyX+CS169.1x+3T2015SP/

###Variações de Pares
**Expert-Expert** - Essa variação pode gerar um aumento enorme de produtividade e grandes resultados, entretanto nela pode haver uma falta de resolver problemas de novas formas, visto que dificilmente alguém da dupla questionará praticas já estabelecidas.

**Expert-Aprendiz** - Essa variação cria uma excelente oportunidade para o expert mentorear o aprendiz. Ela proporciona a criação de novas ideias, visto que o aprendiz deve buscar questionar e aprender práticas estabelecidas e o expert tem que usar os conhecimentos adquiridos com essas práticas para explicá-las e questioná-las também. É muito importante que o aprendiz não haja passivamente no processo e não hesite em participar.
 
**Aprendiz-Aprendiz** - Pode gerar ganhos de produtividade maior do que dois aprendizes trabalhando sozinhos, entretanto não é uma variação muito encorajada.

## Teste de aceitação
<p align="justify">Os Testes de Aceitação consistem no teste de uma possível aceitação por parte do cliente. Testes de aceitação estão intimamente ligados com as user stories.

<p align="justify">Testes de aceitação, visam testar o sistema do ponto de vista do usuário, de modo que são menos sucetíveis a alterações. Como o sistema é testado com todos os componentes interligados e configurados, inclusive bancos de dados e gerenciadores de filas, há garantias de que cada serviço oferecido esteja funcionando.

## Integração Contínua

<p align="justify">Integração contínua consiste em integrar o trabalho diversas vezes ao dia, ao invés de uma única vez, assegurando que a base de código permaneça consistente ao final de cada integração. O objetivo principal de utilizar a integração contínua é verificar se as alterações ou novas funcionalidades não criaram novos defeitos no projeto já existente.

<p align="justify">Esse conceito de integração contínua está atrelado à aplicação de controle de versionamento, geralmente feito com o uso de alguma ferramenta, como o github. O controle de versionamento permite restaurar versões anteriores do sistema, comparar códigos, gerenciar alterações, entre outros, e é utilizado por equipes de desenvolvimento que compartilham mesmo código e projeto. 

<p align="justify">O controle de versão funcionará de forma básica da seguinte forma:

* O desenvolvedor faz o seu código, efetua um build (compilar, preparar o executável, rodar os testes automatizados, etc) antes de integrar seu código com a base principal;
* Após realizar o build, o sistema deve ser integrado a base do sistema de controle de versão através de sincronização;

<p align="justify">Este processo deve ser feito frequentemente, evitando-se assim o acúmulo de codificação para a integração ao repositório. Algumas metodologias ditam que o desenvolvedor só pode considerar como pronto o trabalho quando o trabalho estiver sincronizado e então o desenvolvedor realizar um build na máquina de integração e após todos os testes serem executados com sucesso.

<p align="justify">Na integração contínua o processo de build integrado deve ser feito constantemente, sendo sincronizado sempre que possível, evitando o acúmulo de códigos e de testes. Isto por que é mais fácil encontrar erros em pequenas integrações do que em uma integração grande.

<p align="justify">Nesse contexto de código compartilhado e versionamento centralizado por uma ferramenta, a integração contínua, ou seja, a comunicação entre as partes que cada desenvolvedor construiu, permite que conflitos de versão sejam resolvidos mais rápido, desde que a integração ocorra continuamente.

<p align="justify">A chave para uma boa integração, como visto anteriormente, é um ambiente de controle de versão centralizado, builds e testes automatizados. Essa prática reduz erros e riscos cometidos pela equipe, pois como o sistema é integrado contínua e rapidamente, os erros também são detectados na mesma velocidade.

## Referências
* [Desenvolvimento Ágil](http://www.desenvolvimentoagil.com.br/xp/valores/)
* [Desenvolvimento XP](http://xp.edugraf.ufsc.br/bin/view/XP/TesteAceitacaoXtesteUnidade)
* [Integração Contínua](http://www.desenvolvimentoagil.com.br/xp/praticas/integracao)
* [Integração Contínua](http://www.devmedia.com.br/integracao-continua-uma-introducao-ao-assunto/28002)