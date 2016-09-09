
[1. O que é][about]  
[2. Valores do RUP][valores]  
[3. Disciplinas do RUP][disciplinas]  
[4. Fases/Iterações do RUP][fases]  
[5. Papéis][papeis]  

--
## O que é?
<p align = "justify" > O RUP <i>(Rational Unified Process)</i> é um processo de desenvolvimento de <i>software</i>. Ele engloba as ações necessárias para transformar um conjunto de requisitos do cliente em um sistema de <i>software</i> combinando os ciclos de vida iterativo, incremental e verificando a qualidade do mesmo de forma que cada entrega do <i>software</i> em um ciclo agrega mais valor ao produto em relação ao ciclo anterior.

## Valores do RUP

RUP é baseado em um conjunto de princípios de desenvolvimento de <i>software</i> e melhores práticas, por exemplo:

1. Desenvolvimento de <i>software</i> iterativo
2. Gerenciamento de requisitos
3. Uso de arquitetura baseada em componente
4. Modelagem visual de <i>software</i>
5. Verificação da qualidade do <i>software</i>
6. Controle de alteração no <i>software</i>

## Disciplinas do RUP

### Seis Disciplinas de Engenharia de <i>Software</i>

#### Disciplina de Modelagem de Negócios

<p align = "justify" >As organizações estão cada vez mais dependentes de sistemas de TI, tornando-se imperativo que os engenheiros de sistemas de informação saibam como as aplicações em desenvolvimento se inserem na organização. As empresas investem em TI, quando entendem a vantagem competitiva do valor acrescentado pela tecnologia. O objetivo de modelagem de negócios é, primeiramente, estabelecer uma melhor compreensão e canal de comunicação entre engenharia de negócios e engenharia de <i>software</i>. Compreender o negócio significa que os engenheiros de <i>software</i> devem compreender a estrutura e a dinâmica da empresa alvo (o cliente), os atuais problemas na organização e possíveis melhorias. Eles também devem garantir um entendimento comum da organização-alvo entre os clientes, usuários finais e desenvolvedores.

<p align = "justify" >Modelagem de negócios, explica como descrever uma visão da organização na qual o sistema será implantado e como usar esta visão como uma base para descrever o processo, papéis e responsabilidades.

#### Disciplina de Requisitos

<p align = "justify" >Esta disciplina explica como levantar pedidos das partes interessadas (<i>"stakeholders"</i>) e transformá-los em um conjunto de requisitos que os produtos funcionam no âmbito do sistema a ser construído e fornecem requisitos detalhados para o que deve fazer o sistema.

#### Disciplina de Análise e Projeto(<i>"Design"</i>)

<p align = "justify" >A Análise e Projeto busca mostrar como o sistema será realizado. O objetivo é construir um sistema que:

* Execute, em um ambiente de execução determinado, as tarefas e funções especificadas nas descrições de casos de uso;
* Cumpra todas as suas necessidades;
* Seja fácil de manter quando ocorrerem mudanças nos requisitos funcionais;

<p align = "justify" >Resultados de projeto em um modelo de análise e projeto têm, opcionalmente, um modelo de análise. O modelo de design serve como uma abstração do código-fonte, isto é, o projeto atua como uma espécie de "gabarito" de como o código-fonte será estruturado e escrito. O modelo de projeto consiste em classes de design estruturado em pacotes e subsistemas com interfaces bem definidas, representando o que irá se tornar componentes da aplicação. Ele também contém descrições de como os objetos dessas classes colaboram para desempenhar casos de uso do projeto.

#### Disciplina de Implementação

Os efeitos da Implementação são:

* Definir a organização do código em termos de subsistemas de implementação organizados em camadas
* Implementar classes e objetos em termos de componentes (arquivos-fonte, binários e executáveis, entre outros)
* Testar, como unidades, os componentes desenvolvidos
* Integrar os resultados produzidos por implementadores individuais (ou equipes) em um sistema executável

<p align = "justify" >Sistemas são criados através da aplicação de componentes. O processo descreve como reutilizar componentes existentes ou implementar novos componentes com responsabilidades bem definidas, tornando o sistema mais fácil de manter e aumentando as possibilidades de reutilização.

#### Disciplina de Teste

As finalidades da disciplina de Teste são:

* Verificar a interação entre objetos
* Verificar a integração adequada de todos os componentes do <i>software</i>
* Verificar se todos os requisitos foram corretamente implementados
* Identificar e garantir que os defeitos são abordados antes da implantação do <i>software</i>
* Garantir que todos os defeitos são corrigidos, reanalisados e fechados

<p align = "justify" >O <i>Rational Unified Process</i> propõe uma abordagem iterativa, o que significa que deve-se testar todo o projeto. Isto permite encontrar defeitos tão cedo quanto possível, o que reduz radicalmente o custo para reparar o defeito. Os testes são realizados ao longo de quatro dimensões da qualidade: confiabilidade, funcionalidade, desempenho da aplicação e desempenho do sistema. Para cada uma destas dimensões da qualidade, o processo descreve como passar pelo teste do ciclo de planejamento, projeto, implementação, execução e avaliação.

#### Disciplina de Implantação

<p align = "justify" >O objetivo da Implantação é o de produzir com sucesso lançamentos de produtos e entregar o <i>software</i> para seus usuários finais. Ela cobre uma vasta gama de atividades, incluindo a produção de <i>releases</i> externas do <i>software</i>, a embalagem do <i>software</i> e aplicativos de negócios, distribuição do <i>software</i>, instalação do <i>software</i> e s prestação de assistência aos usuários. Embora as atividades de implantação estejam principalmente centradas em torno da fase de transição, muitas delas devem ser incluídas nas fases anteriores para se preparar para a implantação, no final da fase de construção. Os processos ("<i>workflows</i>") de "Implantação e Ambiente" do RUP contêm menos detalhes do que outros <i>workflows</i>.

### Três Disciplinas de Apoio/Suporte

#### Disciplina de Ambiente

<p align = "justify" >O ambiente enfoca as atividades necessárias para configurar o processo para um projeto. Ele descreve as atividades necessárias para desenvolver as diretrizes de apoio a um projeto. A proposta das atividades de ambiente é prover à organização de desenvolvimento de <i>software</i> os processos e as ferramentas que darão suporte à equipe de desenvolvimento. Se os usuários do RUP não entendem que o RUP é um <i>framework</i> de processo, eles podem percebê-lo como um processo pesado e caro. No entanto, um conceito-chave dentro do RUP foi que o processo RUP pode e, muitas vezes, deve ser refinado. Este foi inicialmente feito manualmente, ou seja, por escrito, um documento de "caso de desenvolvimento" que especificou o processo refinado para ser utilizado. Posteriormente, o produto IBM <i>Rational Method Composer</i> foi criado para ajudar a tornar esta etapa mais simples, engenheiros de processos e gerentes de projeto poderiam mais facilmente personalizar o RUP para suas necessidades de projeto. Muitas das variações posteriores do RUP, incluindo <i>OpenUP/Basic</i>, a versão open-source e leve do RUP, são agora apresentados como processos distintos, por direito próprio, e atendem a diferentes tipos e tamanhos de projetos, tendências e tecnologias de desenvolvimento de <i>software</i>. Historicamente, como o RUP, muitas vezes é personalizado para cada projeto por um perito do processo RUP, o sucesso total do projeto pode ser um pouco dependente da capacidade desta pessoa.

#### Disciplina de Configuração e Gerência de Mudança

<p align = "justify" >A disciplina de Gestão de Mudança em negócios com RUP abrange três gerenciamentos específicos: de configuração, de solicitações de mudança, e de <i>status</i> e medição.

* <p align = "justify" >Gerenciamento de configuração: A gestão de configuração é responsável pela estruturação sistemática dos produtos. Artefatos, como documentos e modelos, precisam estar sob controle de versão e essas alterações devem ser visíveis. Ele também mantém o controle de dependências entre artefatos para que todos os artigos relacionados sejam atualizados quando são feitas alterações.

* <p align = "justify" >Gerenciamento de solicitações de mudança: Durante o processo de desenvolvimento de sistemas com muitos artefatos existem diversas versões. O CRM mantém o controle das propostas de mudança.

* <p align = "justify" >Gerenciamento de status e medição: Os pedidos de mudança têm os estados: novo, conectado, aprovado, cedido e completo. A solicitação de mudança também tem atributos como a causa raiz, ou a natureza (como o defeito e valorização), prioridade, etc. Esses estados e atributos são armazenados no banco de dados para produzir relatórios úteis sobre o andamento do projeto. A <i>Rational</i> também tem um produto para manter a solicitações de mudança chamado <i>ClearQuest</i>. Esta atividade têm procedimentos a serem seguidos.

#### Disciplina de Gerência de Projeto

<p align = "justify" >O planejamento de projeto no RUP ocorre em dois níveis. Há uma baixa granularidade ou planos de Fase que descreve todo o projeto, e uma série de alta granularidade ou planos de Iteração que descrevem os passos iterativos. Esta disciplina concentra-se principalmente sobre os aspectos importantes de um processo de desenvolvimento iterativo: Gestão de riscos; Planejamento de um projeto iterativo através do ciclo de vida e para uma iteração particular; E o processo de acompanhamento de um projeto iterativo, métricas. No entanto, esta disciplina do RUP não tenta cobrir todos os aspectos do gerenciamento de projetos.

Por exemplo, não abrange questões como:

* Gestão de Pessoas: contratação, treinamento, etc
* Orçamento Geral: definição, alocação, etc
* Gestão de Contratos: com fornecedores, clientes, etc

Fonte: [IBM Rational Unified Process](https://pt.wikipedia.org/wiki/IBM_Rational_Unified_Process)
## Fases/Iterações do RUP
<p align = "justify" >Para exemplificar as fases/iterações do RUP, o gráfico conhecido como "gráfico de baleias" é utilizado.Ele traz um panorama de como um projeto é executado no RUP, levando em consideração as disciplinas, iterações e fases. Observando as curvas do gráfico, é possível notar que em cada fase são abordadas todas as disciplinas.

!["Gráfico de Baleias"](https://upload.wikimedia.org/wikipedia/pt/0/07/Fases_do_RUP_-_portugues.jpg)

No RUP, o Engenheiro de Processo é responsável por adaptar o processo de desenvolvimento de <i>software</i> para atender o projeto. Para isso, este papel define o tamanho de cada iteração e quantas iterações existirão por cada fase. Nas matérias de GPP e MDS, a equipe de GPP de cada projeto ficou a cargo deste papel. Algumas equipes por exemplo, utilizaram iterações com extensão de duas semanas, com as fases de iniciação e elaboração sendo compostas apenas de uma iteração, enquanto a fase de construção constituída por mais iterações.

### Iniciação

Essa fase tem como objetivos preparar o ambiente de suporte, estabelecer o escopo do projeto, determinar os casos de uso, estimar o custo e prazo totais e identificar os riscos potenciais. O principal artefato dessa fase é o Documento de Visão.

<p align = "justify" >É uma fase muito importante para os esforços de desenvolvimento, é nela que se encontra grandes riscos de negócios e de requisitos que precisam de um cuidado especial a fim de que o projeto flua normalmente. A meta que almejada é que todos os envolvidos no projeto do software cheguem a um consenso e tenham conhecimento claro sobre o ciclo de vida do mesmo. 

<p align = "justify" >Para projetos iniciais esta é uma parte fundalmental que requer demasiada atenção. Para projetos que visam melhorias de sistemas esta fase já existe, contudo é uma fase de iniciação mais rápida.

<p align = "justify" >É nesta fase que estabelecem o escopo do projeto de software, os critérios de aceitação e se o projeto deve ou não ser aceito. Os casos de uso começam a ser levantados, verificar quais são os principais cenários que o sistema encontrará. Na iniciação deve se a tentar também a estimar os riscos em potencial, que todo projeto possui. Também nesta mesma fase deve-se prepara o ambiente de suporte para o projeto como a configuração de ambiente para e equipe.

**Marco: Objetivo do Ciclo de vida**
* O marco do objetivo do cilo de vida é o que avalia e diz sobre a viabilidade inicial do projeto.

### Elaboração

<p align = "justify" >A fase de elaboração tem como meta criar a baseline de arquitetura do sistema, cujo objetivo é forncer uma base estável para a construção. Priemeiramente é realizado um um exame dos requisistos mais significativos, ou seja, os que tem um maior impacto na arquitetura. Durante esta fase é realizado protótipos de arquitetura que servem para verificar a estabilidade da arquiteura escolhida.

<p align = "justify" >Deve se certificar nesta fase que a arquitetura que está sendo utilizada é estável o suficiente e que os riscos sejam minimizados, podendo assim determinar com uma segurança maior, o custo do sistema e quanto de programação será necessário. Além de se certificar da estabilidade da arquitetura é necessário demonstrar que a arquitetura escolhida para a baseline suportará o requisistos do sistema. O preço e o tempo de desenvolvimento devem ser levados em consideração na escolha da arquitetura.

**Marco: Arquitetura do ciclo de vida**
* O marco desta fase é a arquitetura do ciclo de vida que pode ser virificada através do documento de arquitetura. É durante está fase que se define uma baseline gerenciada para a arquitetura do software, através desta definição é que o escalonamento da equipe ocorre na fase seguinte de Construção.

### Construção

### Transição

## Papéis
<p align = "justify" >O RUP tem alguns papéis genéricos como os de analista, desenvolvedor, testador e gerente. Cada um desses papéis genéricos tem outros papéis mais detalhados, somente o papel de testador que a única atividade existente é a de testador. Abaixo temos os papéis genéricos e os detalhados de cada um.

**Analistas:**
* Analista de sistema
* Designer de negócios
* Revisor do modelo de negócios
* Analista do processo de negócios
* Revisor de requisitos
* Especificar de requisitos
* Analista de teste
* Designer de interface de usuário

**Desenvolvedores:**
* Designer de cápsula
* Revisor de código
* Designer de banco de dados
* Implementador
* Integrador
* Arquiteto de <i>software</i>
* Revisor de arquitetura
* Revisor de <i>desgin</i>
* Designer
* Designer de teste

**Testadores:**
* Testador

**Gerentes:**
* Engenheiro de processo
* Gerente de projeto
* Gerente de controle de mudança
* Gerente de configuração
* Gerente de implantação
* Revisor do projeto
* Gerente de testes

Fonte: [http://www.funpar.ufpr.br:8080/rup/process/workers/ovu_works.htm](http://www.funpar.ufpr.br:8080/rup/process/workers/ovu_works.htm)
Fonte: [http://www.funpar.ufpr.br:8080/rup/process/itrwkfls/iwf_iwfs.htm]
(http://www.funpar.ufpr.br:8080/rup/process/itrwkfls/iwf_iwfs.htm)

[about]: https://github.com/fga-gpp-mds/00-Disciplina/wiki/RUP-(Rational-Unified-Process)#o-que-%C3%A9
[valores]: https://github.com/fga-gpp-mds/00-Disciplina/wiki/RUP-(Rational-Unified-Process)#valores-do-rup
[disciplinas]: https://github.com/fga-gpp-mds/00-Disciplina/wiki/RUP-(Rational-Unified-Process)#disciplinas-do-rup
[fases]: https://github.com/fga-gpp-mds/00-Disciplina/wiki/RUP-(Rational-Unified-Process)#fasesitera%C3%A7%C3%B5es-do-rup
[papeis]: https://github.com/fga-gpp-mds/00-Disciplina/wiki/RUP-(Rational-Unified-Process)#pap%C3%A9is
