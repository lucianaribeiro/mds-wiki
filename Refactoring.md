# **Responsável: Owla**

***

https://labs.spotify.com/2014/04/11/qualities-of-quality/

dividas técnicas:
https://www.youtube.com/watch?v=pqeJFYwnkjE

# Refatoração

A refatoração é um processo de reorganização da estrutura interna do software, sem alterar o seu comportamento externo. É um modo disciplinado de reorganizar código, facilitando a posterior depuração, eliminando código presumível de introduzir erros. De modo geral, quando se refabrica o código, melhora-se o desenho e a estruturação deste.

# Bad Smells in code (mal cheiro de código)

Bad smell é uma situação na qual a estrutura do programa pode ser melhorada com refatoração, como por exemplo: Duplicação de código e classe ou métodos longos.

# Identificando mal cheiro de código - métricas de código fonte

Existem vários indicativos de bad smells, abaixo deixo algumas definições desses bad smells bem como a refatoração sugerida:

* **Long Method/ God Method:** São métodos que centralizam a funcionalidade da classe e que, geralmente, são difíceis de entender e de manter.
Para melhorar esses métodos pode-se dividir o método em dois ou transformar o método em uma classe.

* **Feature Envy:** Acontece quando uma parte do código de uma classe "inveja" outra classe, por exemplo quando um método de uma classe usa atributos somente de outra classe.
Para refatorar pode-se mover os métodos e atributos entre classes ou juntar duas classes em uma.

* **Divergent Change:** Ocorre quando uma classe pode mudar frequentemente de diferentes formas e por razões distintas.
Como refatoração pode-se dividir a classe em duas.

* **Shotgun Surgery:** Oposto do Divergent Change acima, pois toda vez que uma classe for alterada, são necessárias várias pequenas mudanças em outras classes diferentes.
Como refatoração pode se mover métodos e atributos entre as classes e juntar duas classes em uma.

* **Refused Bequest:** Ocorre quando uma classe herda atributos e métodos de outra classe, mas não os usa.
Como refatoração propõe-se mover o método ou atributo da superclasse para a subclasse e substituir o relacionamento de herança por associação.

* **Comments:** Os comentários não são ruins, porém quando em excesso podem indicar que os nomes de métodos/atributos não estão suficientemente expressivos.
Pode-se quebrar um método em dois ou renomear.
## Ferramentas das métricas

# Tipos de Refatoração

# Treinamento

- Incluir descrição do treinamento/DOJO - passo a passo - etapas
- Registrar os detalhes da dinâmica
- Infraestrutura Necessária para a dinâmica
- Código referência no projeto da disciplina (00-Disciplina)
- Treinamento em, pelo menos 2 linguagens

# Referências

Engenharia de software Refactoring, disponível em: http://paginas.fe.up.pt/~ei02017/docs/relatorio_es.pdf

Ian Sommerville. Engenharia de Software, 9ª Edição. Pearson Education, 2011.