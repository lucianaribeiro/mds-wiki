# Tutoriais
Esta parte é destinada para apresentação de tutoriais que auxiliem a disciplina.

##Aprendendo a usar o camando alias no linux  
Alias é um comando que vai facilitar muito a sua vida e ajudar na sua produtividade. O que ele faz é dar um apelido a uma linha de comando. Por exemplo, em vez de digitar  
``$ cd user/user/Documents/Faculdade/MDS``  
você pode apenas digitar  
``$ MDS``
e você estará na pasta MDS.  
Para usá-lo basta digitar no terminal:  
``$ alias apelido='comando'``  
Por exemplo:
``$ alias MDS = cd user/user/Documents/Faculdade/MDS``  

Porém usando apenas este comando ao reiniciar sua máquina ele perderá o apelido. Para torná-lo permanente você deve  

1 - entrar no arquivo ~/.bashrc  
``$ nano ~/.bashrc``  
2 - colocar no final do arquivo o apelido desejado  
``alias  apelido='comando'``  
3 - salvar  
4 - no terminal digitar  
``source ~/.bashrc``

E pronto! Você já pode usar seus comandos personalizados.

# Materiais
Esta parte é destinada para apresentação de materiais que auxiliem a disciplina.
