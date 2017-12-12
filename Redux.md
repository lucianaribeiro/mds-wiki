# Entendendo Redux

### O que é Redux?

<p align="justify">&emsp;&emsp;Redux é um padrão de arquitetura criado para simplificar a implementação do Flux do Facebook. Possui inspiração nos conceitos da linguagem funcional Elm e em bibliotecas de JavaScript. O Redux é sustentado por três pilares fundamentais que definem seu conceito: um único ponto de verdade, o estado é imutável e mudanças são feitas apenas por funções puras.</p>

#### Os princípios fundamentais

1. ##### Um único ponto de verdade

   <p align="justify">&emsp;&emsp;Todo e qualquer estado da aplicação é mantido em um único local, chamado de store. Os acessos a essa store são feitos somente por meio de referência a informação ali armazenada. Isso evita que exista dados duplicados, uma vez que qualquer mudança, feita em uma informação da store, será propagada para o restante da aplicação.</p>

2. ##### O estado é imutável

   <p align="justify">&emsp;&emsp;O estado da aplicação é inalterável. A única forma de alterá-lo é disparando uma action com a mudança</p>

3. ##### Mudanças são feitas apenas por funções puras

   <p align="justify">&emsp;&emsp;Para descrever a mudança que a action fará no estado é preciso criar reducers. Elas são responsáveis por receber as actions e aplicá-las ao estado, sempre retornando um novo state.</p>

   #### Conceitos importantes

   1. ##### State

      <p align="justify">&emsp;&emsp;State (estado) é o conjunto de dados guardados durante o momento em que sua aplicação está rodando.</p>

   2. ##### Actions

      <p align="justify">&emsp;&emsp;Actions (ações) são objetos que transmitem o que será enviado de cada iteração na aplicação para a store. As actions, obrigatoriamente, precisam possuir um tipo (type) que indica o tipo de iteração e o parâmetro.</p>

   3. ##### Reducers

      <p align="justify">&emsp;&emsp;Como explicado anteriormente, o papel da reducer é receber as actions e aplicar as modificações que elas trazem no state.</p>

   4. ##### Store

      <p align="justify">&emsp;&emsp;A store é responsável por manter o state da aplicação, permitindo a leitura do mesmo e que mudanças só sejam feitas através de reducers.</p>

   #### Conclusão

   <p align="justify">&emsp;&emsp;Com Redux é possível construir aplicações mais eficientes e ele facilita a implementação de funcionalidades mais complexas. Embora a curva de aprendizado seja maior, o ganho de produtividade no desenvolvimento de aplicativos será visível, uma vez que o seu entendimento seja alcançado.</p>


#### Bibliografia

GIL, Renan; Afina, o que é redux?; Disponível em: <http://geofusion.tech/afinal-o-que-e-o-redux/>;

IANAKIARA, Diogenes; 5 motivos para usar Redux; Disponível em: <https://blog.getty.io/5-motivos-para-aprender-redux-6ac730f3f1f2>;

DACAL, Vinícius; Conhecendo o básico de Redux; Disponível em <https://imasters.com.br/desenvolvimento/conhecendo-o-basico-do-redux/?trace=1519021197>;

SOSA, Henrique; Bem-vindo ao Redux; Disponível em : <https://tableless.com.br/bem-vindo-ao-redux/>;
