### Histórico de Revisões

| Data       |  Descrição                      | Autor                          |
|:----------:|:-------------------------------:|:------------------------------:|
| 07/05/2017 | Introdução e Guia de Instalação | Felipe Hargreaves (15/0009313) |
| 30/05/2017 | Arquitetura MVVM                | Felipe Hargreaves (15/0009313) |

[Introdução](#introdução)  
[Configuração de Ambiente](#configuração-de-ambiente)

---

# Introdução

<p align="justify"> <b>Xamarin</b> é uma plataforma para desenvolvimento multi-plataforma de aplicações <i>mobile</i> mantida pela <i>Microsoft</i>. Através de uma base de código compartilhado em <i>C#</i>, é possível criar aplicativos com acesso à elementos nativos de interface e API tanto para <i>Android</i> quanto para <i>iOS</i>, proporcionando soluções de alto desempenho. 

# Configuração de Ambiente

<p align="justify"> Atualmente, o <i>Xamarin</i> encontra-se disponível para os sistemas operacionais <i>Windows</i> e <i>macOS</i>, fazendo uso, respectivamente das IDEs <i>Visual Studio</i> e <i>Xamarin Studio</i>. O processo de instalação e configuração da ferramenta é apresentado a seguir:

**Windows 10:**

**Passo 1**: Instalar o Visual Studio com o Xamarin:  
**1)** Fazer o download do instalador do [Visual Studio Community 2017](https://www.visualstudio.com/) ou a versão estável mais recente.  
**2)** No instalador, selecionar a opção **Desenvolvimento móvel com .NET**, na seção *Celular & Jogos*.  
**3)** Aguardar o download dos componentes necessários e a instalação da plataforma. O Visual Studio já será instalado com todas as ferramentas necessárias referentes ao Xamarin.

**Passo 2**: Instalando e configurando o Git para Windows:  
**1)** Fazer o download do [Git](https://git-scm.com/downloads).  
**2)** Prosseguir com a instalação, utilizando as opções padrão.  
**3)** Junto com o Git, é instalado um emulador de terminal com uma versão básica do *bash*. Dessa forma é possível o uso do Git através de linha de comando, com os mesmos comandos utilizados em outros sistemas.  
**4)** Dentro do Git Bash, configurar o usuário com os seguintes comandos, trocando as informações entre aspas:

    git config --global user.name "Nome do usuário"

    git config --global user.email "Email do usuário"


# Arquitetura - MVVM

<p align="justify"> O padrão arquitetural adotado no desenvolvimento de projetos em Xamarin é o <b>Model-View-ViewModel (MVVM)</b>, uma variação do MVC tradicional. Desenvolvida pela <i>Microsoft</i>, visa simplificar a programação em ambientes guiados a eventos, como é o caso de aplicações <i>mobile</i>. De forma geral, as atribuições de cada componente do MVVM são:

* <p align="justify"><b>Model</b>: Representa o modelo de domínio da aplicação, com a definição de seus objetos e provendo uma camada de acesso aos dados. 
* <p align="justify"><b>View</b>: Determina a estrutura dos elementos a serem exibidos na tela e a sua organização na mesma. É a camada que interage com o usuário.
* <p align="justify"><b>View Model</b>: Disponibiliza para a View uma lógica de apresentação, ao mesmo tempo em que não possui conhecimento sobre nenhum aspecto específico da View. Possui propriedades e comandos que servem para "popular" a View com dados e notificá-la de mudanças de estado. A conexão entre as duas é realizada através de um processo denominado <i>Data Binding</i>. 

![Exemplo MVVM](https://upload.wikimedia.org/wikipedia/commons/8/87/MVVMPattern.png)

Alguns pontos importantes e dicas para o cumprimento dos padrões de arquitetura no desenvolvimento de uma aplicação Xamarin:

* <p align="justify"> A ViewModel, em hipótese alguma, deve conter referências à View ou a elementos da mesma. Sua estruturação deve seguir a ideia de <i>POCO - Plain Old CLR Object</i>, isto é, não utilizar nenhum recurso ou dependência além dos componentes proporcionados pelo C#/.NET Framework. Além de diminuir o acoplamento entre as classes do sistema, isso torna a ViewModel uma estrutura 100% testável.
* <p align="justify"> De forma similar, Models não devem conter referências a elementos tanto das Views quanto das ViewModels. Sua única atribuição é a modelagem e acesso aos dados do sistema.
* <p align="justify"> Para manter a ideia de que a ViewModel não tem conhecimento sobre a View, elementos de navegação entre páginas ou envio de pop-ups não devem ser implementados diretamente na ViewModel. Devem ser criadas interfaces contendo os métodos de navegação do Xamarin, e o acesso realizado a partir destas. Desta forma, a ViewModel mantém sua propriedade de <i>POCO</i> e continua sendo testável, sendo necessário apenas realizar o <i>Mock</i> das interfaces implementadas.
* <p align="justify"> Cada View em Xamarin é composta por dois arquivos: um <i>.xaml</i>, que define os elementos de UI da página e um <i>.xaml.cs</i>, popularmente conhecido como <i>Code-Behind</i>, onde pode se instanciar a lógica da View e definir outros elementos. De forma geral, esses arquivos tem as mesmas capacidades - tudo que pode ser definido em XAML também pode ser escrito em C#. Na prática, entretanto, é recomendado que toda a declaração da interface seja feita através do XAML e que toda a lógica de apresentação seja delegada à ViewModel. Nessa situação, o <i>Code-Behind</i> se torna um arquivo praticamente vazio, contendo apenas a declaração do BindingContext daquela página. Em alguns casos não se pode alcançar esse cenário ideal, mas ainda assim deve se tentar manter o <i>Code-Behind</i> o mais "limpo" possível.
* <p align="justify"> As ViewModels devem implementar e utilizar em suas propriedades a interface INotifyPropertyChanged. Como o nome sugere, ela é responsável por notificar mudanças de estado em propriedades. Dessa forma, pode-se manter a apresentação da View sincronizada com as mudanças de estado que ocorrem na Model determinadas pela ViewModel.

### Referências adicionais sobre MVVM:
[Xamarin Guides - From Data Binding to MVVM](https://developer.xamarin.com/guides/xamarin-forms/xaml/xaml-basics/data_bindings_to_mvvm/)

[Xamarin Developers - Introduction to Data Binding](https://blog.xamarin.com/introduction-to-data-binding/)
