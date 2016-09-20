## 1. Arquitetura de Software
“Uma arquitetura de software envolve a descrição de elementos arquiteturais dos quais os sistemas serão construídos, interações entre esses elementos, padrões que guiam suas composições e restrições sobre estes padrões”. GARLAN, 1998.
Exemplo de elementos arquiteturais: bancos de dados, servidores, clientes, componentes, entre outros.

## 2. Padrões Arquiteturais
* Padrões arquiteturais expressam formas de organizar a estrutura do sistema;
* Permitem a construção de uma arquitetura aderente a certas propriedades;
* A escolha do padrão arquitetural pode ser o primeiro passo para a solução de um projeto.

Padrões arquiteturais definem o conjunto de componentes do software, suar responsabilidades e as regras de relacionamentos entre eles.

Por que utilizar uma padrão arquitetural?
* Instrumento para lidar com a complexidade do software a ser construído;
* Ajuda na redução de tempo e custo de desenvolvimento;
* Melhora a manutenibilidade do software.

## 3. MVC

Um Padrão Arquitetural que separa estruturalmente o projeto do software em três parte:

* Model;
* View;
* Controller.

### 3.1. MVC - Model

Responsável por:
* Representar as classes de domínio;
* Leituras e escritas de dados (interface com o banco de dados).

### 3.2. MVC - Controller

Responsável por:
* Receber requisições dos usuários;
* Processar requisições;
* Controlar as models e vews a serem utilizadas.

### 3.3. MVC - View

Responsável por:
* Interação com o usuário;
* Exibição de dados (HTML).

### 3.4. MVC – Diálogo das camadas

View – Fala Controller ! O usuário acabou de pedir para acessar o Facebook ! Pega os dados de login dele ai.
Controller – Blz. Já te mando a resposta. Ai model, meu parceiro, toma esses dados de login e verifica se ele loga.
Model – Os dados são válidos. Mandando a resposta de login.
Controller – Blz. View, o usuário informou os dados corretos. Vou mandar pra vc os dados dele e você carrega a página de perfil.
View – Vlw. Mostrando ao usuário…

## 4. Arquitetura de Projetos Django

Segue o Padrão Arquitetural MVT, próprio do Django, aderente ao MVC.
De acordo como o Django Book, o Django segue o padrão MVC suficientemente para ser considerado um framework MVC.

### 4.1. Como Funciona o MVT
O MVT separa estruturalmente o projeto do software em três parte:
* Model;
* View;
* Template.

#### 4.1.1. Model
As Models do MVC e do MVT são equivalentes em responsabilidades.
O framework Django facilita na interface com o banco de dados.
Esta camada contém qualquer coisa e tudo sobre os dados: como acessá-lo , como validá-lo , quais comportamentos que tem, e as relações entre os dados.

#### 4.1.2. View
No MVT a View é responsável pela Lógica de negócios (Python), parte do trabalho da View do MVC ou em alguns casos da Controller.

#### 4.1.3. Template
No MVT a Template é responsável pela camada de interface com o usuário (HTML), parte do trabalho da View.

#### 4.1.3. Detalhes arquiteturais de projetos Django
* As resoluções de urls, responsabilidade dada as controllers no MVC, é feita pela própria estrutura do framework;
* O Django oferece uma interface com o banco de dados que perite ao desenvolvedor não se preocupar com a conexão entre suas classes de domínio e banco.   



