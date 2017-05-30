## Alunos
- Filipe Ribeiro - 12/0117738
- Gabriel Silva - 12/0118220
- Phelipe Wener - 12/0132893

## Sumário

- [1.0 Introdução](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#10-introdução)
- [2.0 Escopo](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#20-escopo)
- [3.0 Qualidade](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#30-qualidade)
- [4.0 Custos](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#40-custos)
- [5.0 Riscos](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#50-riscos)
- [6.0 Conclusão](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#60-conclusão)
- [7.0 Referências](https://github.com/fga-gpp-mds/00-Disciplina/wiki/Ágil-vs-Tradicional---Uma-abordagem-pragmática#70-referências)

## 1.0 Introdução

Nos dias atuais, a necessidade de automatização de processos se faz cada vez mais presente. Processos são essenciais dentro de qualquer organização em qualquer área de atuação, inclusive em uma das áreas mais recentes, que é a produção de software. A definição de processos de desenvolvimento de software vem com o objetivo de aumentar a produtividade e diminuir os riscos de um projeto(VIEIRA, 2003).

Com o grande crescimento da demanda na produção de software na atualidade os prazos estão cada vez mais curtos e cobrança relacionada a qualidade estão cada vez maiores. A qualidade de um produto de software está diretamente ligada a melhor forma de atender as necessidades do cliente, o que torna um produto totalmente dinâmico. Uma vez que a natureza do produto é dinâmica existem grandes dificuldades no gerenciamento do desenvolvimento, por exemplo: a essência volátil dos requisitos do cliente(TAVARES, 2008).

O produto de software também possui outra característica única, é totalmente desenvolvido por pessoas, o que gera outra gama de variáveis que podem causar risco e mudanças imprevisíveis no meio de processo de produção (SCHWABER, 2004).

Com base nessas dificuldades, vários processo durante a história da Engenharia de Software foram desenvolvidos, par amenizar esses problemas. Podemos citar destes processos, os processos cascata, interativo, espiral, incremental.

Considerando que para cada contexto de desenvolvimento, um processo pode ser melhor aplicado, foram analisadas e comparadas - nos quisitos de escopo, custo, qualidade e risco - uma versus a outra duas abordagens: Rational Unified Process(RUP) e metodologias ágeis(MA).

## 2.0 Escopo

Nessa sessão, visa-se mostrar a diferente abortagem e mentalidade entre a definição de escopo, ou seja, mostrar as diferenças em como é desenvolvido e gerenciado os requisito em abordagens tradicionais versus a abordagem em metodologias ágeis trazendo primeiro uma visão geral do que é requisito e seu gerênciamento.

### 2.1 Requisito

A elicitação, compreenção e manutenção de requisitos é um fator comum à todas as metodologias de desenvolvimento de software, uma vez que esse item (requisito) é o fundamento de qualquer produto de software.(Aurum; Wohlin, 2005)

O fato de que requitos são vitáis ao desenvolvimento de software deve-se principalmente às responsabilidades que um requisito desenpenha no produto, isto é, este identifica, modela, comunica e documenta o sistema, o ambiente de uso e quem o usará. (Paetsch; Eberlein; Maurer, 2003)

### 2.2 Processo genérico de Gerênciamento de Requisitos

O processo genérico consiste de cinco atividades fundamentais. São elas: Elicitação, Análise e Negociação, Documentação, Validação e Gerenciamento (Paetsch; Eberlein; Maurer, 2003). Cada abordagem tem a sua forma de executar cada uma das etapas como veremos na ultima sessão desse capítulo.

#### 2.2.1 Elicitação

Nessa atividade do processo genérico, tenta-se descobrir e definir o que faz e o que não faz parte do sistema com auxilio dos envolvidos no projeto (gerentes, desenvolvedores, cliente). Nessa etapa é fundamental o desenvolvimento correto do produto desejado, isto é, fundamental para fazer o software que resolve o problema do cliente.(Leffingwell, 2003)

#### 2.2.2 Análise e Negociação

Nessa etapa do processo a checagem dos requisisto é realizado. Verifica-se a consistência, a necessidade, a capacidade de realização e a completude. De forma geral, há uma verificação se é possivel fazer, se o que foi definido realmente é necessario para o sistema e se nada está em conflito ou incompleto. Essa é uma forma de melhorar a definição do produto. (Leffingwell, 2003)

#### 2.2.3 Documentação

Nessa etapa é documentado todos os requisitos definidos. Dessa forma é possivel uma visão do produto à ser realizado por todos os envolvidos. Assim como também servirá como insumo para as atividade de manutenção. (Leffingwell, 2003)

#### 2.2.4 Validação

Nessa etapa são validados os requisitos, ou seja, se estão descrevendo corretamente o produto. (Leffingwell, 2003)

#### 2.2.5 Gerenciamento de Requisitos

O objetivo do gerenciamento é capturar, armazenar, disseminar e gerenciar informação. Gerenciamento de requisitos inclui todas as atividades preocupadas com mudanças, controle de versão e rastreamento de requisitos. Rastreamento de requisitos provê relacionamento entre requisitos, projeto e implementação de um sistema a fim de gerenciar suas mudanças. (Leffingwell, 2003)

### 2.3 Aplicação nas abordagens

Na abordagem tradicional, a definição e gerênciamento de requisitos é realizada por uma equipe específica dentro do projeto. Por exemplo o papel de engenheiro de requistos é fundamental para essa abordagem. Nas metodologias ágeis toda a equipe é responsável pela elicitação e gerencimento de requisitos.

Um outro ponto que podemos levar em consideração são os padrões estabelecidos pelas abordagens tradicionais:

- Padrão IEEE 830 – Práticas Recomendadas para Especificação de Requisitos de Software (IEEE, 1998);
- Padrão IEEE 1233 – Guia para Desenvolvimento de Especificação de Requisitos de Sistemas (IEEE, 1998);
- Padrão IEEE 1362 – Guia para Tecnologia da Informação – Definição de Sistema – Documento de Conceito de Operações (IEEE, 1998)

Uma vez que a abordagem tradicional define um processo metódico, há a necessidade de definir diretrizes. Dessa forma toda a equipe deve ser guiada por essas diretrizes tornando o processo reproduzivel e bem definido.

Por outro lado, as metodológias ágeis não se baseiam nestes padrões para elicitação e gerenciamento de requisitos. Nessa abordagem, o processo é mais pragmático. E a equipe tem a autonomia de aprender no decorrer do processo o que melhor se adapta ao contexto dos envolvidos e do projeto (Aurum; Wohlin, 2005). Por exemplo: na abordagem tradicional há todo um processo bem definido de gerênciamento de mudança, com responsável e entrada e saída. Já a abordagem ágio lida com a mudança de forma diferente, o entendimento dessa aborgem é que variabilidade de requisitos é um problema constante em praticamente todos os projetos de software, portanto, o suporte a essas mudanças está incluso em seu processo como um ponto forte dando liberdade à cada equipe para definir como deve ser realizada (Tomayko JE, 2002).

Outro fator importante é que as metodologias ágeis não lidam com a mudança ou necessidade de forma futura. Foca-se nas necessidade pela quais agregam valor ao cliente. Assim, evita-se o desenvolvimento de uma arquitetura geral e robusta que requer um esforço grande. Busca-se incrementar o software modulo por modulo . Diferente da abordagem tradicional onde há a necessidade de uma definição de uma arquitetura robusta (Beck K, 1999).

O entendimento da natureza volátio de requisitos tem um grande impacto na capacidade das metodologias ágeis de serem _enxutos_. Em geral, uma arquitetura genérica e mais abrangente é esperada para suportar a variabilidade nos requisitos. Contudo, uma arquitetura mais complexa custa mais, não só para a equipe de desenvolvimento, mas também para a equipe de manutenção e correção de erros (Aurum; Wohlin, 2005).

## 3.0 Qualidade
## 4.0 Custos

A gerencia de custos do projeto tem como meta a inclusão dos processos
envolvidos por meio de estimativas, orçamentos e controle de custos de forma que 
o projeto possa ser executado dentro do orçamento inicialmente acordado entre os
envolvidos. A gerencia de custos tem como maior foco de atuação os custos de
recursos necessários para conclusão as atividades do projeto.
Dessa forma deve-se levar em consideração o efeito das decisões de projeto no
custo recorrente a subsequencia do uso, prestando a manutenção e o suporte do
produto, serviço ou qualquer produto do projeto. O  planejamento de
gerenciamento dos custos ocorre nas fases iniciais do projeto fornecendo a
estrutura para cada processo do gerenciamento dos custos para que seu
desempenho seja eficiente e coordenado.

### 4.1 Gerência de Custos em Metodologias Tradicionais

Metodologias de desenvolvimento de _software_ usam como base o PMBOK para
gerência de custos. o PMBOK propõe as seguintes atividades: 
* Planejar o Gerenciamento dos Custos: é o processo que visa o estabelecimento
das políticas, documentos, gestão e controle de custos;
* Estimar os Custos: processo de desenvolvimento visando estimações de recursos
monetários para terminar as atividades do projeto;
* Determinar o Orçamento:  é o processo de agregação  dos custos estimados de
atividades individuais ou pacotes de trabalho para estabelecer uma linha de
base dos custos autorizada;
* Controlar os Custos: processo de monitoramento do andamento do projeto para
atualização do seu orçamento e gerenciamento das mudanças feitas na linha de
base de custos.

### 4.2 Gerência de Custos em Metodologias Ágeis


## 5.0 Riscos
## 6.0 Conclusão
## 7.0 Refências

- VIEIRA, M. Gerenciamento de Projetos de Tecnologia da Informação. Rio Janeiro, Brasil. 2003;
- TAVARES, A. Gerência de Projetos com PMBOK e Scrum: um estudo de caso. Gravataí, Brasil. 2008;
- SCHWABER, K. Agile Project Management with Scrum. Microsoft Press. 2004;
- Aurum, Aybüke; Wohlin, Claes (Eds.) “Engineering and Managing Software Requirements” 2005.
- Paetsch F, Eberlein A, Maurer F (2003) Requirements engineering and Agile software development. In Proceedings of 8th International Workshop on Enterprise Security, Linz, Austria, 9-11 June.
- IEEE Standard 830 (1998) IEEE recommended practice for software requirements.
- IEEE Standard 1233 (1998) IEEE guide for developing system requirements specifications
- IEEE Standard 1362 (1998) IEEE guide for information technology: System definition, concept of operations document.
- Tomayko JE (2002) Engineering of unstable requirements using Agile methods. In: Proceedings of International Conference on Time-Constrained Requirements Engineering, Essen, Germany, 9-13 September.
- Beck K (1999) Extreme programming explained: Embrace change. Addison-Wesley, UK.
- Leffingwell, D., Widrig, D., Managing Software Requirements: A Use Case Approach, 2a. Edição, Addison-Wesley, 2003.
