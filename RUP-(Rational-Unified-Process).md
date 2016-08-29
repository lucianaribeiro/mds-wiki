## O que é?

## Valores do RUP

## Disciplinas do RUP

### Seis Disciplinas de Engenharia de Software

#### Disciplina de Modelagem de Negócios

As organizações estão cada vez mais dependentes de sistemas de TI, tornando-se imperativo que os engenheiros de sistemas de informação saibam como as aplicações em desenvolvimento se inserem na organização. As empresas investem em TI, quando entendem a vantagem competitiva do valor acrescentado pela tecnologia. O objetivo de modelagem de negócios é, primeiramente, estabelecer uma melhor compreensão e canal de comunicação entre engenharia de negócios e engenharia de software. Compreender o negócio significa que os engenheiros de software devem compreender a estrutura e a dinâmica da empresa alvo (o cliente), os atuais problemas na organização e possíveis melhorias. Eles também devem garantir um entendimento comum da organização-alvo entre os clientes, usuários finais e desenvolvedores.

Modelagem de negócios, explica como descrever uma visão da organização na qual o sistema será implantado e como usar esta visão como uma base para descrever o processo, papéis e responsabilidades.

#### Disciplina de Requisitos

Esta disciplina explica como levantar pedidos das partes interessadas ("stakeholders") e transformá-los em um conjunto de requisitos que os produtos funcionam no âmbito do sistema a ser construído e fornecem requisitos detalhados para o que deve fazer o sistema.

#### Disciplina de Análise e Projeto("Design")

O objetivo da análise e projeto é mostrar como o sistema vai ser realizado. O objetivo é construir um sistema que:

* Execute, em um ambiente de execução específico, as tarefas e funções especificadas nas descrições de casos de uso;
* Cumpra todas as suas necessidades;
* Seja fácil de manter quando ocorrerem mudanças de requisitos funcionais;

Resultados de projeto em um modelo de análise e projeto tem, opcionalmente, um modelo de análise. O modelo de design serve como uma abstração do código-fonte, isto é, o projeto atua como um modelo de "gabarito" de como o código-fonte é estruturado e escrito. O modelo de projeto consiste em classes de design estruturado em pacotes e subsistemas com interfaces bem definidas, representando o que irá se tornar componentes da aplicação. Ele também contém descrições de como os objetos dessas classes colaboram para desempenhar casos de uso do projeto.

#### Disciplina de Implementação

Os efeitos da implementação são:

* Para definir a organização do código, em termos de subsistemas de implementação organizadas em camadas
* Para implementar classes e objetos em termos de componentes (arquivos-fonte, binários, executáveis e outros)
* Para testar os componentes desenvolvidos como unidades
* Integrar os resultados produzidos por implementadores individuais (ou equipes), em um sistema executável

Sistemas são realizados através da aplicação de componentes. O processo descreve como reutilizar componentes existentes ou implementar novos componentes com responsabilidades bem definidas, tornando o sistema mais fácil de manter e aumentar as possibilidades de reutilização.

#### Disciplina de Teste

As finalidades da disciplina de teste são:

* Verificar a interação entre objetos
* Verificar a integração adequada de todos os componentes do software
* Verificar se todos os requisitos foram corretamente implementados
* Identificar e garantir que os defeitos são abordados antes da implantação do software
* Garantir que todos os defeitos são corrigidos, reanalisados e fechados

O Rational Unified Process propõe uma abordagem iterativa, o que significa que deve-se testar todo o projeto. Isto permite encontrar defeitos tão cedo quanto possível, o que reduz radicalmente o custo de reparar o defeito. Os testes são realizados ao longo de quatro dimensões da qualidade:confiabilidade, funcionalidade, desempenho da aplicação, e o desempenho do sistema. Para cada uma destas dimensões da qualidade, o processo descreve como passar pelo teste do ciclo de planejamento, projeto, implementação, execução e avaliação.

#### Disciplina de Implantação

O objetivo da implantação é o de produzir com sucesso lançamentos de produtos e entregar o software para seus usuários finais. Ele cobre uma vasta gama de atividades, incluindo a produção de releases externos do software, a embalagem do software e aplicativos de negócios, distribuição do software, instalação do software e prestação de ajuda e assistência aos usuários. Embora as atividades de implantação estejam principalmente centradas em torno da fase de transição, muitas das atividades devem ser incluídas nas fases anteriores para se preparar para a implantação, no final da fase de construção. Os processos ("workflows") de "Implantação e Ambiente" do RUP contêm menos detalhes do que outros workflows.

### Três Disciplinas de Apoio/Suporte

#### Disciplina de Ambiente

O ambiente enfoca as atividades necessárias para configurar o processo para um projeto. Ele descreve as atividades necessárias para desenvolver as diretrizes de apoio a um projeto. A proposta das atividades de ambiente é prover à organização de desenvolvimento de software os processos e as ferramentas que darão suporte à equipe de desenvolvimento. Se os usuários do RUP não entendem que o RUP é um framework de processo, eles podem percebê-lo como um processo pesado e caro. No entanto, um conceito-chave dentro do RUP foi que o processo RUP pode e, muitas vezes, deve ser refinado. Este foi inicialmente feito manualmente, ou seja, por escrito, um documento de "caso de desenvolvimento" que especificou o processo refinado para ser utilizado. Posteriormente, o produto IBM Rational Method Composer foi criado para ajudar a tornar esta etapa mais simples, engenheiros de processos e gerentes de projeto poderiam mais facilmente personalizar o RUP para suas necessidades de projeto. Muitas das variações posteriores do RUP, incluindo OpenUP/Basic, a versão open-source e leve do RUP, são agora apresentados como processos distintos, por direito próprio, e atendem a diferentes tipos e tamanhos de projetos, tendências e tecnologias de desenvolvimento de software. Historicamente, como o RUP, muitas vezes é personalizado para cada projeto por um perito do processo RUP, o sucesso total do projeto pode ser um pouco dependente da capacidade desta pessoa.

#### Disciplina de Configuração e Gerência de Mudança

A disciplina de Gestão de Mudança em negócios com RUP abrange três gerenciamentos específicos: de configuração, de solicitações de mudança, e de status e medição.

* Gerenciamento de configuração: A gestão de configuração é responsável pela estruturação sistemática dos produtos. Artefatos, como documentos e modelos, precisam estar sob controle de versão e essas alterações devem ser visíveis. Ele também mantém o controle de dependências entre artefatos para que todos os artigos relacionados sejam atualizados quando são feitas alterações

* Gerenciamento de solicitações de mudança: Durante o processo de desenvolvimento de sistemas com muitos artefatos existem diversas versões. O CRM mantém o controle das propostas de mudança

* Gerenciamento de status e medição: Os pedidos de mudança têm os estados: novo, conectado, aprovado, cedido e completo. A solicitação de mudança também tem atributos como a causa raiz, ou a natureza (como o defeito e valorização), prioridade, etc. Esses estados e atributos são armazenados no banco de dados para produzir relatórios úteis sobre o andamento do projeto. A Rational também tem um produto para manter a solicitações de mudança chamado ClearQuest. Esta atividade têm procedimentos a serem seguidos

#### Disciplina de Gerência de Projeto

O planejamento de projeto no RUP ocorre em dois níveis. Há uma baixa granularidade ou planos de Fase que descreve todo o projeto, e uma série de alta granularidade ou planos de Iteração que descrevem os passos iterativos. Esta disciplina concentra-se principalmente sobre os aspectos importantes de um processo de desenvolvimento iterativo: Gestão de riscos; Planejamento de um projeto iterativo através do ciclo de vida e para uma iteração particular; E o processo de acompanhamento de um projeto iterativo, métricas. No entanto, esta disciplina do RUP não tenta cobrir todos os aspectos do gerenciamento de projetos.

Por exemplo, não abrange questões como:

* Gestão de Pessoas: contratação, treinamento, etc
* Orçamento Geral: definição, alocação, etc
* Gestão de Contratos: com fornecedores, clientes, etc

## Fases/Iterações do RUP

## Papéis

