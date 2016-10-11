# Framework XP

O XP é um método de desenvolvimento de software, leve, não é prescritivo, e procura fundamentar as suas práticas por um conjunto de valores. O XP, diferentemente do que muito pensam, também pode ser adotar por desenvolvedores médios e não apenas por desenvolvedores experientes. Sendo que seu objetivo principal é levar ao extremo um conjunto de práticas que são ditas como boas na engenharia de software. Entre elas podemos citar o teste, visto que procurar defeitos é perda de tempo, nós temos que constantemente testar. Mas o XP possui mais práticas do que apenas testar, entre as práticas, o XP diz que:

- Já que testar é bom, que todos testem o tempo todo;
- Já que revisão é bom, que se revise o tempo todo;
- Se projetar é bom, então refatorar o tempo todo;
- Se teste de integração é bom, então que se integre o tempo todo;
- Se simplicidade é bom, desenvolva uma solução não apenas que funcione, mas que seja a mais simples possível;
- Se iterações curtas é bom, então mantenha-as realmente curtas;

Como podemos notar todas as práticas boas são levadas ao extremo no XP.
Pode-se se dizer que é uma metodologia bastante volátil, mas no bom sentido. Portanto, implica que para conseguirmos se adaptar as mudanças frequentes, o XP preconiza ciclos curtos que nos dá previsibilidade e redução de incertezas/riscos, Simplicidade e melhorias constantes de código (refactoring) para facilitar a mudança e Testes Automatizados e Integração Contínua para aumentar a confiança.

O método XP preconiza que Codificação é a atividade central do projeto, que os Testes (que também são código) servem de especificação de requisitos, e a Comunicação oral entre desenvolvedores é fundamental, o que dá proximidade a equipe.

Isto não quer dizer que a equipe XP não constrói documentos e não faz modelagem, ela só não considera que um modelo é um documento. Modelos são feitos o tempo todo seja como quadro branco, sessões de design, etc, mas servem como um suporte para o concreto que realmente importa.

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

Pair programming 
https://courses.edx.org/courses/course-v1:BerkeleyX+CS169.1x+3T2015SP/

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