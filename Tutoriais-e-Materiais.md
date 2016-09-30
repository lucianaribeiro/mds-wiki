# Tutoriais
Esta parte é destinada para apresentação de tutoriais que auxiliem a disciplina.

##Aprendendo a usar o comando _alias_ no linux  
_Alias_ é um comando que vai facilitar muito a sua vida e ajudar na sua produtividade. O que ele faz é dar um apelido à uma linha de comando. Por exemplo, em vez de digitar ``$ cd user/user/Documents/Faculdade/MDS`` você pode apenas digitar ``$ MDS`` e você estará na pasta MDS.  

Para usá-lo basta digitar no terminal:  
``$ alias apelido='comando'``  
Por exemplo:
``$ alias MDS = cd user/user/Documents/Faculdade/MDS``  

Porém usando apenas este comando ao reiniciar sua máquina ele perderá o apelido. Para torná-lo permanente você deve seguir os seguintes passos:  

**1 -** Entrar no arquivo ~/.bashrc  
``$ nano ~/.bashrc``  

**2 -** Colocar no final do arquivo o apelido desejado  
``alias  apelido='comando'``  

**3 -** Salvar  
**4 -** Digitar no terminal   
``source ~/.bashrc``

E pronto! Você já pode usar seus comandos personalizados.

##Django Girls
O tutorial do [Django Girls](https://tutorial.djangogirls.org/pt/deploy/) é extremamente completo para quem deseja aprender a desenvolver em Python utilizando o Django como framework. O mesmo explica e ensina desde a instalação, passando por criação de projeto, URLs, implementação de models, views, templates, até estilização com CSS. Além disso, aborda formulários, administração e Querysets.

# Materiais
Esta parte é destinada para apresentação de materiais que auxiliem a disciplina.
## Tutorial Terminal 
> ### Codecademy 
> https://www.codecademy.com/pt/learn/learn-the-command-line
### Comunidade Ubuntu
> https://help.ubuntu.com/community/UsingTheTerminal

