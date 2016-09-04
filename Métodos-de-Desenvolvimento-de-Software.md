## Bem vindo a MDS
[ O que é Processo de Desenvolvimento de Software](#o-que-é-processo-de-desenvolvimento-de-software)

[ O que é modelo de processo de software](#o-que-é-modelo-de-processo-de-software)

[ Fases do ciclo de vida de software](#fases-do-ciclo-de-vida-de-software)

[ Estudo de caso da influencia do modelo de processo no sucesso de um projeto](#estudo-de-caso-da-influencia-do-modelo-de-processo-no-sucesso-de-um-projeto)

[ Referências ](#referências)

------
### O que é Processo de Desenvolvimento de Software
  Para Pressman um processo é um conjunto de atividades, ações e tarefas realizadas na 
criação de algum produto de trabalho (work product). Uma atividade esforça­se para atingir 
um objetivo amplo (por exemplo, comunicar­se com os interessados) e é utilizada independentemente do campo de aplicação, do tamanho do projeto, da complexidade de esforços ou do grau de rigor com que a engenharia de software será aplicada. 

Na engenharia de software, um processo não é uma prescrição rígida de como desenvolver um software, mas sim uma abordagem adaptável que possibilita às pessoas (a equipe de software) realizar o trabalho de selecionar e escolher o conjunto apropriado de ações e tarefas.

### O que é modelo de processo de software

É uma representação abstrata de um processo de software. Cada modelo representa um processo a partir de uma perspectiva particular.
Modelos de processo de software são utilizados para explicar diferentes abordagens do desenvolvimento de software. Definem a sequência em que as atividades do processo serão realizadas.
Não são descrições definitivas de processo de software, mas sim abstrações úteis, que podem ser usadas em diferentes abordagens.


### Fases do ciclo de vida de software

- **Levantamento de Requisitos:** Define as funcionalidades e as necessidades do produto, resultando no escopo e no documento de visão. Podemos separar os requisitos em três categoria:

    - **Funcionais:** São os requisitos relacionados às funcionalidades do software;
    - **Não Funcionais:** São os requisitos relacionados às necessidades do software;
    - **Inversos:** São os requisitos que definem o que o software não pode fazer.

       
       O objetivo de levantar requisitos é guiar o desenvolvimento para que o sistema correto seja feito. Para isso, é necessário descrever as condições e capacidades do sistema bem o suficiente,
de forma a ter um acordo entre cliente e os desenvolvedores do sistema, no quesito do que o sistema deve ou não fazer. O grande desafio dessa etapa é que o cliente, mesmo que não seja um especialista da área de computação, deve ser capaz de ler e entender os resultados da captura de requisitos. O resultado do levantamento de requisitos também ajuda o gestor do projeto a planejar o cronograma do projeto(JACOBSON,2007).
      

- **Design/Projeto:** A atividade de design compreende todo o esforço de concepção e modelagem que têm por objetivo descrever como o software será implementado. O design inclui:

    - **O design conceitual:** Que envolve a elaboração das ideias e conceitos básicos que determinam os elementos fundamentais do software em questão. O design conceitual têm influência na interface do usuário e na arquitetura do software.

    - **O design da interface do usuário:** Envolve a elaboração da maneira como o usuário pode interagir para realizar suas tarefas, a escolha dos objetos de interfaces , o layout de janelas e telas, etc. A interface deve garantir a boa usabilidade do software.

    - **O design da arquitetura do software:** Deve elaborar uma visão macroscópica do software em termos de componentes que interagem entre si.

    - **Design dos algoritmos e estruturas de dado:** Visa determinar, de maneira independente da linguagem de programação adotada, as soluções algorítmicas e as estruturas de dados associadas.

    A fase de Design ou Projeto, é a fase final do processo de planejamento e resulta no documento de arquitetura.

- **Implementação:** Envolve as atividades de codificação, compilação, integração e testes. A codificação visa traduzir o design em um programa, utilizando linguagens e ferramentas adequadas. A codificação deve refletir a estrutura e o comportamento descrito no design. Os componentes arquiteturais devem ser codificados de forma independente e depois integrados. Os testes podem ser iniciados durante a fase de implementação. A depuração de erros ocorre durante a programação utilizando algumas técnicas e ferramentas. É fundamental um controle e gerenciamento de versões para que se tenha um controle correto de tudo o que está sendo codificado.

- **Verificação e Validação:** Destinam-se a mostrar que o sistema está de acordo com a especificação e que ele atende às expectativas de clientes e usuários. A validação visa assegurar se o programa está fazendo aquilo que foi definido na sua especificação. A verificação visa verificar se o programa está correto, isto é, não possui erros de execução. Os testes são para correção, desempenho e confiabilidade, garantindo a qualidade do software.

- **Manutenção:** A parte de manutenção envolve melhorar o software a demanda do(s) cliente(s), seja por falhas do programa ou simplesmente por melhorias que o cliente precisa.


![](http://static.commentcamarche.net/pt.kioskea.net/faq/images/7kUwNTrgQL7rMNKd-s-.png)


#### Objetivos de cada fase do ciclo de vida de software

- **Levantamento de Requisitos** : Essa fase tem como objetivo unificar a visão do cliente e dos desenvolvedores. Para que isso aconteça, são analisados diversos fatores, como por exemplo as funcionalidades que o produto deve possuir, além do objetivo final do produto. Essas análises são feitas de maneira que os desenvolvedores tenham uma visão detalhada do que deve ser produzido.

- **Design Geral** : Essa fase consiste no detalhamento de como o software será desenvolvido, ou seja, a linguagem que será utilizada, assim como a arquitetura que o projeto deverá seguir. Feito isso, espera-se que todos os desenvolvedores tenham visões semelhantes do que deve ser produzido, assim como a maneira que essa produção deve ocorrer. Essa etapa é crucial, pois sem ela, é possível que o projeto inteiro falhe por divergências de visões entre os desenvolvedores.

### Estudo de caso da influencia do modelo de processo no sucesso de um projeto 

resumo do texto (e podem sugerir outros casos): 
[A partir do texto:  http://sloanreview.mit.edu/article/what-successful-project-managers-do/](A partir do texto:  http://sloanreview.mit.edu/article/what-successful-project-managers-do/)

##Referências

Jacobson, I., Booch, G., Rumbaugh, J., Rumbaugh, J., & Booch, G. **The unified software development process**. Reading: Addison-wesley, 2007.