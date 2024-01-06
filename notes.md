#### 02/01/2024

Curso de Flutter: aplicando testes de unidade, de Widget e Mocks

```
flutter pub run build_runner build
dart run build_runner build
```

@01-Entendendo o projeto 

@@01
Apresentação

[00:00] Você quer aprender uma habilidade nova? E que tal uma habilidade que vai ser o diferencial para o mercado de trabalho?
[00:08] Pois é, você que quer ser desenvolvedor de Flutter ou desenvolvedora em Flutter e já está fazendo os nossos cursos há um tempo. Chegou a hora de nós elevarmos um pouco o nosso nível e aprender sobre testes.

[00:20] Nesse curso nós vamos aprender vários tipos de testes, entender para que servem os testes. Nós vamos usar esse projeto do Alura Bank para testar, onde ele tem uma API, tem os botões, algumas interações. Bem tranquilo.

[00:35] Nesse curso nós também vamos aprender o que são teste de unidades, o que são testes de widgets e explorar esses dois mundos incríveis para podermos produzir um projeto de qualidade.

[00:47] Então, se você quer ser mais profissional na sua área, o ideal é fazer projetos profissionais, e projetos profissionais precisam de testes.

@@02
Preparando o ambiente: Projeto inicial

Boas-vindas ao nosso curso de Flutter: Testes de Unidade, Widget e Mocks!
Para incrementar sua aprendizagem, vamos utilizar o projeto Alubank. Nesse app simples, vamos deixar de lado funcionalidades mais complexas para focar exclusivamente nos testes - uma habilidade importante para qualquer dev!

Caso queira, você pode baixar o projeto do curso.

https://github.com/alura-cursos/alura_flutter_curso_7/archive/refs/heads/master.zip

@@03
Compreendendo os testes

[00:00] Quer dizer que você já tem conhecimento suficiente para criar um grande aplicativo de celular? Ótimo, isso é perfeito, mas chegou a hora de nós elevarmos um pouco o nosso nível para podermos entrar no mercado de trabalho.
[00:13] E para poderem entrar no mercado de trabalho, serem programadores, desenvolvedores, desenvolvedoras ou programadoras de alta qualidade, nós temos que entender conceitos específicos e especiais.

[00:24] E um desses conceitos é o conceito de testes. O que são testes? Para que servem testes? É o que nós vamos ver agora. Então, só para nós não perdermos o costume, vamos dar uma organizada em como essa aula vai funcionar.

[00:35] Primeiro nós temos que entender por que utilizamos testes nos nossos projetos, qual é a grande importância? E depois nós vamos dar uma pincelada, uma introduzida, uma entendida melhor em quais são os tipos de teste em Flutter.

[00:50] Então, primeiramente, por que utilizar testes? Qual é a importância de testar? Para começar, eu quero fazer uma analogia, vamos contar uma história.

[01:00] Vamos supor agora que você é uma desenvolvedora ou um desenvolvedor Flutter em uma grande empresa e você ficou os últimos dois anos produzindo um grande aplicativo de celular.

[01:10] Um aplicativo de banco, ele é incrível, você tem certeza de que a qualidade do seu produto é imensa, sensacional.

[01:13] Então, todo mundo está na ansiedade e vocês lançam o produto, finalmente está lá na PlayStore para todo mundo baixar e começam a aparecer diversos bugs, erros, coisas que você não tinha controle sobre.

[01:32] "Como assim bugs que nós não conseguimos controlar?". Por exemplo, telas de tamanhos diferentes ou, as vezes, o usuário não tem espaço no celular. Enfim, muitas coisas que podem acontecer e nós não estávamos preparados para acontecer.

[01:45] O seu aplicativo que você demorou tanto tempo para fazer começou a dar problema com vários usuários e eles não perdoaram o seu aplicativo.

[01:43] As avaliações foram devastadoras, as pessoas não avaliaram nada bem o seu aplicativo e acabou que isso prejudicou muito a sua empresa.

[02:03] Meu deus, e agora? O que nós fazemos? Bom, qual que seria a grande solução? Como nós podemos impedir que isso aconteça com os nossos projetos? Com os nossos aplicativos?

[02:15] A solução é adicionar testes durante a produção de um projeto. O modo mais efetivo de nós fazermos com que os problemas não apareçam para os nossos clientes é ter certeza de que se eles aparecerem, eles vão aparecer enquanto nós estamos produzindo o nosso projeto.

[02:31] Conseguimos ter um ideia de que, quando nós estamos construindo grandes aplicações, o ideal é colocar testes para que o projetos tenha qualidades, mas não paramos por aí, nós precisamos entender um pouco quais são os tipos de testes que nós vamos trabalhar.

[02:47] Como é que funcionam os testes? O que, de fato, são testes na sua essência?

[02:52] Primeiro, eu quero que vocês entendam que teste não é uma coisa só do Flutter, só de aplicativo de celular. Não, testes são essenciais e eles existem em muitos tipos de projeto. Eles existem em projetos de celulares, mas também existem em projetos de desktop ou sites.

[03:10] De qualquer forma, independentemente do tipo de projeto ou de software que você criando, é importantíssimo que ele tenha um teste para que você tenha qualidade no que você está entregando. Existem vários tipos de testes que nós podemos usar, que nós podemos criar e isso não só no Flutter, isso é em todos os tipos de testes de software.

[03:28] Então, eu vou pedir agora para subir os créditos dos vários nomes de testes que existem por aí quando nós estamos testando projetos. Vocês devem estar vendo, no lado esquerdo da tela, que são muitos testes.

[03:40] Pois é, mas vamos agora falar do que interessa para nós, que são os testes em Flutter. Quando nós estamos falando de Flutter, especificamente, nós podemos dividir em alguns poucos tipos de teste e o primeiro deles é o teste de unidade, um teste mais simples.

[03:56] Então, eu vou só comentar o que são esses tipos de testes e depois nós vamos entendê-los com mais clareza.

[04:03] Nos testes de unidades nós estamos testando objetos pequenos, partes pequenas do nosso código, como uma classe ou uma função ou, como nós gostamos de nomear, um objeto específico.

[04:16] Como nós já sabemos os nosso objetos de Flutter, nós temos esses objetos bem pequenos que compõem todo um projeto. Se você não lembra exatamente o que é uma classe, o que é uma função, sugiro dar uma revisada lá no Dart.

[04:29] Mas nós também temos outros tipos de testes que são os testes de widgets. Lembram dos widgets lá dos nossos primeiros cursos de Flutter?

[04:36] Pois é, nós temos que testar os widgets também, até porque eles são componentes que aparecem na nossa tela e às vezes nós temos integrações ou ações com esses componentes.

[04:44] Então, nós temos que testar se o componente está no tamanho ideal para a tela, temos que testar se o botão está funcionando do jeito que nós queremos.

[04:52] E nós também temos alguns testes mais completos e complexos que são os testes de integração que eles entregam vários widgets, várias classes, vários comportamentos, métodos, ações.

[05:03] Então, é um teste mais completo, que é como nós gostamos de chamar, existem os testes de fluxo onde nós mudamos de tela. Temos também os testes de ponta a ponta onde nós testamos todo o aplicativo por completo.

[05:16] E esse teste, na verdade, é bem longo e bem complexo.

[01:19] Só para vocês não ficarem perdidos, nesse curso, especificamente, nós não vamos nos aprofundar em testes de integração, porque eles requerem um pouco mais de cuidado e de tempo. Agora nós vamos focar um pouco mais nos testes de widget e nos testes de unidade.

[05:36] Só para nós finalizarmos com chave de ouro. A gente criou uma tabela para comparação de confiança, comparação de vários detalhes em relação os testes.

[05:45] Olha só, quando nós não testamos o nosso projeto, ele não é confiável, pode até parecer bugs. O custo é zero, porque nós não precisamos fazer nada, a dependência, nenhuma, porque não dependemos de um teste e o nível de velocidade é rápido, ou seja, você produz muito rápido um projeto, mas ele não é confiável.

[06:05] Quando começamos colocar testes no nosso projeto, nós podemos usar testes de unidade que aumentam a confiança do nosso projeto um pouco. Então, deixa de ser ruim para ser só uma confiança baixa, o custo é barato, porque fazer os testes de unidade são mais simples, mais fáceis.

[06:22] E as dependências são bem poucos, porque os testes de unidade são meio que únicos. Então, eles não dependem muito entre si e a velocidade de execução ainda é rápida, apesar de mais lenta do que não fazer nenhum teste. Ela é ainda bem rápida.

[06:34] Conforme nós formos criando testes mais completos e complexos, a confiança aumenta, o custo aumenta, a dependência aumenta e a velocidade cai.

[06:43] Por exemplo, no teste de widget que nós vamos ver nesse curso também, a confiança no seu projeto já é média, o custo já médio, porque você demora mais para fazer. A dependência é moderada, porque alguns widgets dependem de outros widgets e a velocidade de execução desse projeto demora um pouco.

[07:01] Então você atrasa um pouco a execução desses testes, desse projeto, em geral. Isso só para vocês terem uma noção quando nós falamos de testes de integração a confiança é altíssima, porque é muito difícil de você deixar um bug passar.

[07:16] O custo também é muito alto, porque nós demoramos muito tempo para produzir os testes de integração. Então, custa dinheiro para fazer testes que demoram para serem feitos.

[07:29] A dependência é exagerada, é uma dependência muito grande, porque você está testando um código inteiro. Então, todo mundo depende de todo mundo.

[07:36] E a velocidade de execução é muito lenta. Então para você executar um teste gigantesco desse demora muito.

[07:42] A princípio era isso que eu queria passar para vocês em relação a testes. Nós vamos ficar revendo um pouco essas relações de confiança, custo, dependência e velocidade enquanto estivermos aprendendo sobre testes de unidades, sobre testes de widgets.

[07:56] Mas por enquanto era isso que eu queria passar. Vamos conferir o projeto que nós vamos trabalhar? Até daqui a pouco.

@@04
Conhecendo o projeto inicial

[00:00] Muito bem, agora chegou a hora de entendermos um pouco o nosso projeto. Dessa vez vamos fazer um pouquinho diferente. Nós vamos pegar um projeto pronto para depois testá-lo.
[00:13] Por que nós estamos fazendo isso? Porque se tivéssemos que produzir um aplicativo do zero e depois testar, nós íamos perder muito tempo de qualidade do que queremos aprender nesse curso, especificamente, que são testes.

[00:26] Então, nós vamos focar nos testes. Por isso nós já estamos dando um projeto pronto para vocês, para nós entendermos testes apenas.

[00:34] Então, para não ficar muito perdido, nesse vídeo nós vamos entender como funciona esse projeto, mas não precisa se preocupar, se você não pegou ou não entendeu alguma coisa, você pode pegar o projeto no GitHub e dar uma olhada passo-a-passo em como as coisas estão implementadas. Pode ir ao seu tempo, não precisa de pressa. Vamos?

[00:56] Aqui nós temos o nosso aplicativo. Você consegue ver que ele está em inglês, em cima nós temos available balance que é a quantidade de dinheiro que você tem, à direita nós temos o valor do dólar em relação ao real. Embaixo nós temos um componente de spent que é quantidade de dinheiro gasto.

[01:15] A direita nós temos o earned que é a quantidade de dinheiro obtido. Embaixo nós temos um limite de gasto. Nós temos embaixo um texto falando que esse mês você gastou uma porcentagem do seu dinheiro e o ideal é diminuir essa porcentagem.

[01:30] Embaixo nós temos alguns botões. Nós temos o botão de deposit e de transfer. No emulador do lado direito tem um botão desativado de scan, porque nós não vamos usar essa feature por enquanto e embaixo, se nós descêssemos um pouco o projeto, nós vemos account points que são os pontos da nossa conta.

[01:47] Toda vez que você depositar ou transferir, esses pontos vão ser atualizados. Você pode usar esses pontos para poder pedir comida, delivery custa 15 mil pontos, 1 mês de streaming que custa 30 mil pontos e assim vai.

[02:02] Como é que nós podemos interagir com esse nosso aplicativo? Nós temos esses nossos dois botões iniciais que é o deposit e o transfer. Eu quero depositar um dinheiro na nossa conta, esse aplicativo é bem simples, nós não fizemos um grandíssimo aplicativo, até porque não era esse o nosso objetivo, o objetivo é testar.

[02:21] Então, toda vez que eu clicar em depositar, a nossa conta bancaria vai ganhar 10 dólares. Eu vou clicar em deposit, você viu que ficou meio branquinho, só que nada mudou. Para alguma coisa mudar, eu tenho que clicar nos componentes que recebem esses valores.

[02:38] Por exemplo, aqui no nosso available balance, aqui na nossa conta bancária, se eu clicar, ele atualiza os dados para 10. Se eu clicar no card embaixo desse valor, ele vai atualizar o nosso valor de recebido para 10.

[02:52] Aqui em embaixo, nos nosso pontos, se eu clicar, ele vai atualizar para 10 também e assim vai. Se eu continuar clicando deposit eu vou clicar duas vezes a mais, três vezes. Então, vou clicar aqui em cada um dos nossos objetos e eles vão atualizar, earned foi para 40, account points foi para 40 também.

[03:11] E se eu transferir? Eu quero transferir 10 reais da minha conta. Então, se eu clicar em transfer eu transferi, portanto o meu valor, na minha conta diminui, vai para 30 e eu posso atualizar os nossos outros objetos.

[03:26] Por exemplo, aqui agora vai que eu gastei 10 reais e vai mudando aos poucos a nossa barra de progressos de gasto, do limite de gasto. Aqui embaixo no "nossos pontos", ele vai aumentar os pontos, porque independentemente de deposito ou transferência, você vai estar sempre ganhando pontos.

[03:44] E assim nós podemos ficar transferindo e depositando. Um detalhe importante para falar para vocês é que esse valor do dólar em relação ao real, ele é uma API. É uma informação que nós estamos pegando da internet.

[04:02] Então, eu vou mostrar para vocês como é que isso aqui está funcionando, em geral, no nosso projeto, no nosso código. Vamos lá.

[04:08] Então, aqui no nosso projeto nós temos várias pastas, eu não vou passar, exatamente, por tudo, eu vou passar pelas coisa importantes que nós precisamos visualizar no nosso projeto.

[04:19] Então, primeiramente aqui, no lado esquerdo da tela, nós temos a nossa pasta de componentes e ela tem vários arquivos e também tem uma pasta de seções.

[04:26] Por exemplo, nossa pasta de seções nós temos o actions.dart e o header.dart que vou abrir para gente dar uma olhada rapidinho. No actions, aqui é o nosso projeto que corresponde a account actions, que é onde nós temos o nosso depósito, nós temos o nosso transfer.

[04:41] E esse nosso deposito, esse nosso transfer, tem valor de um Inherited widget, que eu vou falar daqui a pouco para vocês, mas isso tudo está sendo modelado, gerenciado, os estados desses valores estão sendo gerenciados por um Inherited widget.

[04:55] Então, criamos um botão para cada uma dessas nossas ações que estão alterando o nosso Inherited widget. Beleza, aqui no actions, no header, por exemplo, aqui nós temos a nossa conta bancária e nela nós temos duas coisas importantes.

[05:11] O primeiro é que esse componente na parte superior do aplicativo, em roxo, ele é clicável, chamado de header, ele é totalmente clicável. Nós conseguimos visualizar isso com o nosso widget InkWell e ele é clicável, porque toda a vez que nós clicarmos nele, ele vai usar o setState para relodar, para rebuildar o valor que está aqui dentro.

[05:30] Então, sempre que eu mudar, por exemplo, cai deposit, eu só consigo visualizar essa mudança se eu clicar no header. Isso é muito importante. Aqui no nosso header nós temos a implementação da nossa API.

[05:42] Então, está recebendo valor da nossa API aqui embaixo em um FutureBuilder. Ele está construindo uma espera para receber os valores lá na internet sem problemas. Coisas que nós já vimos no passado em cursos passados.

[06:00] Beleza, então, tem muito mais outras coisas que nós queremos ver aqui. Não vou me estender aqui, nós temos os pontos que também estão recebendo esses valores e também estão recebendo um setState. Toda vez que nós clicarmos nele vai mudar de estado.

[06:16] Ele também está recebendo os valores do nosso Inherited widget, na linha 30, podemos ver que o texto é um filho do nosso BankInherited que vocês vão ver daqui a pouco, mas é um Inherited widget que manuseei nesse estado.

[06:29] Mesma coisa no status que é o retângulo no centro do nosso aplicativo que recebe o spent e o earned, a quantidade de dinheiro que nós ganhamos, que nós gastamos. Também é clicável, também é atualizável, também recebe informações do nosso Inherited widget. Mesmo esquema para todo mundo.

[06:50] Então, em relação a design, vocês vão ver muitas coisas aqui no nosso components, mas também temos outras pastas. Deixa eu fechar tudo para nós vermos isso com calma.

[06:59] Temos outras pastas que são as pastas de dados, onde nós temos a implementação da nossa API onde nós recebemos a informação a partir de um HTTP, nada que vocês não tenham visto antes.

[07:13] Nós temos também o nosso Inherited widget que foi criado onde nós recebemos e mantemos os dados, coisas que vocês também já viram no passado e mais alguns outros detalhes, por exemplo, em relação ao modelo de banco que é um modelo simples para nós podermos rever e armazenar.

[07:34] Para nós podermos modularizar, na verdade, os nossos valores de quantidade de dinheiro disponível, available, gasto, recebido, os nossos pontos. Além de alguns métodos que vão adicionar dinheiro ou vão adicionar pontos.

[07:52] Assim como um método de transferência. Então, esse aqui é o nosso projeto. Eu sei que eu passei muito rápido por muitas coisas. Sugiro, fortemente, que você dê uma olhada com calma no projeto, dê uma alterada se você quiser dar uma modificada para parecer mais a sua cara, fica à vontade.

[08:09] É um projeto bem simples, mas que vai dar muita margem para nós testarmos muitas coisas nesse nosso curso de testes.

[08:17] Era isso que eu queria passar para vocês, tem mais um detalhe que eu quero mostrar para vocês, mas eu vou mostrar já, que é em relação a esses estados todos mudando o tempo todo.

[08:28] Era isso que eu queria passar para vocês e eu os vejo daqui a pouco.

@@05
Qualidade ou velocidade?

No dia a dia de trabalho, você se verá em situações em que precisará aplicar conceitos teóricos e fazer escolhas. Vamos praticar um pouco?
Você é a(o) Tech Leader de um time de produção de aplicativos de celular e seus gestores solicitaram a produção de um aplicativo o mais rápido possível, sem comprometer a qualidade. Acontece que o aplicativo solicitado demora três meses para ser criado com testes. Se sua equipe não fizer nenhum teste, o aplicativo fica pronto em 1 mês.

Considerando o que vimos durante as videoaulas, qual a melhor alternativa para produzir o aplicativo como o cliente pediu?

Aceitar o pedido, preparar o time e fazer o aplicativo em um mês para impressionar o cliente, deixando os testes para outro momento.
 
Alternativa correta
Explicar ao cliente que o aplicativo vai demorar 3 meses e não há margem para negociar o prazo.
 
Alternativa correta
Explicar ao cliente que a qualidade do aplicativo depende dos testes e que eles podem poupar manutenção desnecessária no futuro. E, também, conversar com a equipe sobre o pedido do cliente e verificar se todos estão de acordo com a velocidade da produção.
 
Exatamente! Comunicação com o cliente e com o time é a chave para o sucesso!
Alternativa correta
Conversar com a equipe sobre manter a velocidade de produção do aplicativo com testes e não considerar o pedido do cliente de entregar rápido.

@@06
Lidando com estados

[00:00] Mas espera aí. Antes de começarmos a fazer testes nesse nosso projeto, tem uma coisa que eu quero perguntar para vocês. Vocês concordam com 100% do que está feito aqui? Vocês acham que a forma como o aplicativo está se desenvolvendo é legal?
[00:19] Por que eu pergunto isso? Olha só. Temos que clicar no botão deposit e depois que clicamos no botão deposit, nada muda na nossa tela. Para podermos mudar os valores na nossa tela, temos que clicar individualmente em cada um dos nosso widgets que tem esse valor.

[00:38] Por que isso está acontecendo? Mesma coisa para o transfer, eu posso clicar em transfer 20 vezes, cliquei várias vezes em transfer. Só vai mudar quando eu clicar no nosso objeto que precisamos mudar de valor.

[00:53] E por que isso tudo está acontecendo? Isso é algo muito importante e tem totalmente a ver com estados. Não é específico do curso de testes, mas isso é muito importante que vocês saibam porque também afetam os testes do nosso projeto.

[01:07] O que acontece? Esse projeto é um projeto extremamente simples. Nós temos poucos valores a serem alterados, são quatro valores, nós temos poucos widgets a serem recarregados, são três widgets e nós temos apenas dois botões que mudam os valores.

[01:26] Então, são poucas interações e nós testamos usando o Inherited widget para manusear, gerenciar um pouco esses estados. É uma forma bem inicial, bem simples, bem simplista de lidar com diversos estados e isso nos limita muito.

[01:47] O ideal mesmo, que seria um aplicativo bom mesmo, é clicarmos em deposit e todos os nossos widgets serem recarregados instantaneamente.

[01:57] Por que isso não acontece nesse nosso projeto? Só para vocês entenderem, nesse nosso projeto temos vários componentes separados. Nós temos o nosso components, no nosso projeto à esquerda e vou abrir o nosso sections.

[02:12] Por exemplo, eu vou abrir o header.dar, o header.dar é um projeto, é um documento, é um arquivo único, específico que lida só com o que está no header.dar. Então, ele receber essa informação do nosso Inherited widget é de boa, ele recebe a qualquer momento. Mas ele ser reconstruído já não é tão fácil, o Inherited widget não faz isso automaticamente por ele.

[02:38] Então nós temos que criar um mecanismo usando set state, ou seja, o nosso header tem que ser um state full widget, e nós temos que manualmente alterar o estado desse nosso objeto sempre que o valor do Inherited widget mudar.

[02:56] Isso vai acontecer com todo mundo, não só com o header. Vai acontecer com esse nosso widget central que é o status. Vai acontecer com esse nosso widget aqui embaixo que é o nosso points.

[03:08] Então, a mesma coisa acontece com todos eles, não é o ideal para um grande projeto. O ideal para um grande projeto é que isso tudo seja recarregado instantânea e automaticamente, porém o Inherited widget não tem tanto poder.

[03:21] O que isso interfere, especificamente, no nosso curso de testes? Nossos testes vão ser fáceis, vão ser tranquilos, até porque as coisas não estão dependendo tanto umas das outras. Os estados estão separados, nós mudamos os valores do nosso objeto manualmente, nada acontece automaticamente.

[03:44] Então, não vamos ter tantas dores de cabeça com testes que acontecem em vários lugares ao mesmo tempo. Ações que acontecem em vários locais, não precisamos nos preocupar com isso.

[03:56] O nosso teste vai ser um pouco mais simples, isso é importante para vocês que estão aprendendo agora a relação de testes.

[04:03] Está bom, Kako, entendi, estamos em um projeto mais fácil, mais simples, esse nosso projeto é simplista por conta dessa questão de estados mudando manualmente, mas como isso altera quando eu for fazer um projeto grande?

[04:19] Quando você for fazer um projeto grande, você vai ter que lidar com gerenciamentos de estados mais específicos, ou seja, você não vai usar só o Inherited widget.

[04:29] Eu sei que nesse ponto, provavelmente, você não sabe nenhum outro gerenciamento de estado específico, você só sabe lidar com o Inherited widget. Tudo bem, é por isso que nós estamos usando o Inherited widget nesse curso.

[04:42] Mas lá na frente você vai descobrir um mar de diversos tipos de gerenciamento de estado. Eu já dei uma pincelada sobre isso nos cursos sobre Controle e Navegação, mas não descobrimos nenhum gerenciamento de estado ainda.

[04:57] Quando vocês descobrirem, vocês vão ver que testes que levam em consideração gerenciamento de estados são um pouquinho diferentes, porque você tem que levar em consideração dependências, muitas dependências, na verdade.

[05:10] Era isso que eu queria passar para vocês em relação aos estados, também queria que vocês tivessem um olhar mais crítico em relação a aplicativos e algumas ações demais.

[05:20] O aplicativo do jeito que está aqui, eu não diria que é um aplicativo para ir ao mercado, ir para Play Store, ir para um usuário. Até porque tem trabalho demais para o usuário, ele ter que clicar para atualizar a tela não é tão legal. Mas eu quero que vocês relevem um pouco isso, até porque nós estamos aprendendo ainda.

[05:40] Falei o que eu queria falar sobre estados. Entendemos que os testes dependem da quantidade de dependência entre os estados e que a dependência dos estados nesse nosso projeto é bem baixa e por isso nosso curso vai ser mais leve, mais de boa.

[05:53] Não precisa se preocupar, depois vamos falar um pouco mais sobre testes mais complexos com estados, mas só depois quando a hora for certa.

[06:02] Agora estou mais aliviado de ter falado isso para vocês, vamos embora agora que eu quero codar uns testes para começarmos a aquecer.

@@07
Faça como eu fiz: explorando o projeto

Hora de colocar a mão na massa!
Para implementarmos a funcionalidade de testes no app, precisamos entender completamente o projeto.

Baixe o projeto inicial do AluraBank e explore cada um dos arquivos disponibilizados, conforme visto em vídeo.

Note como o InheritedWidget está conectado com o modelo de banco BankModel e também revise todas as formas de rebuildar a tela com setState
Vamos lá?

https://github.com/alura-cursos/alura_flutter_curso_7

O objetivo desta atividade é estimular você a compreender o projeto por conta própria!
Na moralzinha? Essa é uma tarefa tranquila, porém é comum ficarmos perdidos com um projeto que nunca vimos. Caso tenha alguma dúvida, chame a gente no fórum!

@@08
O que aprendemos?

Vamos relembrar o que aprendemos? Nessa aula exploramos os conceitos de Testes, conhecemos o nosso Projeto e vimos a importância de verificar o gerenciamento de estado para facilidade dos nossos testes.
Testes de Unidade:
Os testes de unidade são os testes mais simples de se produzir! Eles verificam objetos pequenos como: Classes, métodos, variáveis.

Testes de Widget:
Os testes de Widget são levemente mais complexos e testam elementos visíveis no nosso aplicativo que são construídos na tela.

Testes de Integração:
Os testes de integração são os testes mais completos e complexos, que verificam interação com diversos elementos e todo o fluxo do aplicativo, lembrando que esses testes de integração não serão vistos em completo nesse curso.

Projeto: AluraBank:
Um novo projeto de simulação de banco, com alguns dados de valores arrecadados e gastos, um aplicativo simples para aprender a testar de forma fácil.

Importância dos Estados para Testes:
Quando temos muitas informações que transformam nossa aplicação devemos ficar mais espertos, pois o gerenciamento dessas informações complica a produção de testes.

Finalizamos a Aula 1!

Mal começamos e já aprendemos muito! E aí, o que está achando? Conta pra gente lá no fórum ou no Discord da Alura!

Te vejo na próxima aula!

#### 03/01/2024

@02-Realizando testes de unidade

@@01
Projeto da aula anterior

Caso queira, você pode baixar o projeto do curso no ponto em que paramos na aula anterior.

@@02
Utilizando test()

[00:00] Agora nós podemos começar a trabalhar na produção de testes no Flutter, e por onde que nós começamos?
[00:09] Vamos lá, nós abrimos o nosso projeto e, à esquerda, como nós já conhecemos, temos os nosso diretórios do projeto inteiro. Nós temos aqui, por exemplo, a nossa pasta lib onde nós programamos o projeto em dart, criamos as nossas telas. Temos um main.dart.

[00:27] Eu vou fechar, eu vou minimizar a lib e, se você der uma olhada, duas pastas abaixo tem uma pasta chamada test e é nela que vamos trabalhar agora.

[00:36] Se você notar, essa pasta test tem uma seta laranja para esquerda junto com o uma seta verde para a direita. Vou abri-la, rapidinho, e dentro dela já temos um test. De onde que veio esse test?

[00:50] Bom, quando nós criamos o nosso projeto inicial, lembra aquele projeto do contado básico do Flutter? Pois é, já vem com teste específico para esse projeto. Então, já tem um teste experimentando os contadores, adicionar coisas.

[01:05] Mas nós não vamos ficar vendo esse teste aqui, não é o que nós queremos. Então, o que eu vou fazer aqui? Deletar esse arquivo, porque nós não vamos usar.

[01:15] Beleza, dento da pasta test é onde nós vamos trabalhar. Por onde nós começamos? Nós vamos testar uma coisa simples, como coisa básica primeiro.

[01:25] Vamos começar com testes de unidade e o que nós vamos testar nesse teste de unidade? Uma classe simples, que vai ser a classe bank model que nós vimos agora pouco, mas vamos dar uma recapitulada nela.

[01:38] Antes de começar a criar esse teste, nós temos que criar o arquivo. Então, para criar o eu vou clicar com o botão direito do mouse na pasta test, vamos no New e, em seguida, Dart file.

[01:49] Vou criar um novo arquivo Dart e vou chamar de bank_model_test. É muito essencial que os seus testes tenham nome bem tranquilo de entender.

[02:00] Beleza, nós já temos aqui o nosso arquivo de teste. Por onde que nós vamos? Primeiro vamos dar uma olhada no nosso bank model para ter certeza de como ele funciona?

[02:09] Vou aqui na lib, lado esquerdo da tela, e vou aqui no models, pasta models, e dentro dela nós temos o nosso bank.dart. O bank.dart nada mais é do que uma classe, uma classe que tem quatro componentes, quatro doubles aqui, available, spent, earned e points.

[02:27] Valores que começam em zero e nós temos dois métodos, o deposit e o transfer. O deposit adiciona valor no nosso available, earned e points e o transfer retira valor de available, adiciona valor em points e adiciona valor em spent.

[02:43] Só para vocês recapitularem, no nosso projeto, quando eu clico em deposit ele deposita, portanto o earned sobe, o available sobe, os pontos sobem.

[02:54] Se eu clicar em transfer o spent sobe, o available desce e o points sobe. Assim como está bem explicadinho nos nossos métodos.

[03:04] Beleza, nós já sabemos que isso aqui está funcionando, mas como que nós testamos isso aqui? Como é que nós garantimos que isso aqui vai estar sempre funcionando, independente, das modificações futuras?

[03:15] Primeiro, vamos voltar lá no nosso bank model e vamos começar como qualquer arquivo em dart. Nós precisamos de uma main, então, eu vou criar uma void main () {} parênteses e chaves.

[03:33] A nossa função padrão. Então, para começar a fazer os testes, primeiro nós temos que importar algumas funções de testes especificamente. Eu vou vir escrever im, ele já vai me habilitar para autopreenchimento, então, se eu clicar no botão "Tab", ele preenche para mim.

[03:50] Eu vou escrever flutter_test, underline test, ele já vai dizer para mim qual é o pacote que eu posso adicionar. Então, eu vou aqui e apertar o botão "Tab" e vai importar para mim todo esse pacote de testes.

[04:04] Beleza, nós já temos o nosso pacote importante, já temos a nossa void main, tranquilo. Se vocês estiverem tendo alguma dificuldade em algum ponto, vocês podem falar conosco no fórum.

[04:16] Por onde nós começamos? Tem uma função teste que já facilita os nossos testes simples. Eu vou dentro da main, na linha 3, e vou escrever test. É uma função básica que apertei o botão "Tab" para ele autopreencher e ela precisa de duas coisas, uma descrição e um body.

[04:36] Tem alguns outros detalhes, por exemplo, test on, type out, skip tags. Nós não vamos focar nelas, mas se você quiser dar uma explora, sinta-se à vontade.

[04:46] Inicialmente nós vamos só focar no body e na descrição. Quando nós estamos falando de descrição, significa que o nosso teste precisa, como se fosse uma mini documentação do próprio teste.

[04:56] Ele espera uma string e nessa string nós precisamos colocar informações sobre o nosso teste. Que tipo de informação esse nosso teste precisa?

[05:06] Quando nós estamos criando uma bela descrição nós precisamos de três coisa. Nós precisamos do nome do método que nós vamos testar, nós precisamos de cenário onde está sendo testado e nós precisamos do resultado, tudo isso no nome.

[05:19] Isso é uma convenção de nomenclatura de teste. A ordem específica que você vai colocar, eu não vou te obrigar, existem várias ordens de nomenclatura. Você não precisa se preocupar, a única coisa que você precisa se preocupar é que tem que ter essas três coisas. O local, o método e o resultado.

[05:39] Vamos lá, o que nós estamos testando? Nós estamos testando o nosso bank model. O que explicitamente nós queremos testar primeiro? Eu acho que eu vou testar, de todas essas coisas, eu quero testar o nosso deposit. Vou testar esse método deposit.

[05:54] E qual que seria o resultado? Vamos lá, eu quero testar esse deposit, eu vou testar uma quantidade de valor 10, vou colocar 10 de dinheiro nesse deposit e eu espero que os meus pontos subam para 10, pontos de 0 vão para 10 quando eu der o deposit.

[06:11] Vamos ver. Então, eu vou aqui em 'Bank model deposit should be 10'. Essa é a nossa descrição. Estou falando que o nosso modelo de banco, quando eu depositar, deve ter um valor de 10.

[06:30] E agora nós temos a nossa descrição e nós precisamos trabalhar no body desse teste, no corpo desse teste e o body desse teste nós precisamos de uma função anônima, uma função abre e fecha parênteses, abre e fecha colchetes, na linha 3.

[06:45] Só para nós não termos problemas, eu vou colocar ponto e vírgula no final da linha 3 e teste.

[06:49] Então, a princípio o nosso teste só tem descrição, não tem nenhum função sendo feita. O que nós precisamos? Nós precisamos, primeiramente, criar, instanciar o nosso banco.

[06:58] Eu vou criar um final e o nome dele vai ser final bank e o que ele vai ser? Ele vai ser um final bank = BankModel, um bank model. Pronto, criei um modelo de banco, um widget, um objeto.

[07:13] E o que eu quero fazer com esse bank? Eu quero vir no nosso bank e eu quero depositar. Vamos lá bank.deposit, eu vou acessar esse nosso método e esse nosso método espera um valor double de dinheiro para ser depositado.

[07:31] Então, eu vou colocar 10, porque nós estamos esperando 10. Beleza, até aí tranquilo, ponto e vírgula, na linha, 6 para finalizar.

[07:38] Então, até agora nós não tivemos nenhum problema no nosso teste. Nós criamos o modelo, nós estamos usando o deposit, mas como é que nós vamos saber que o valor foi depositado corretamente?

[07:51] Nós temos que visualizar se as nossas outras informações foram alteradas e para isso nós precisamos entender um pouco da função expect, que é o que nós vamos ver daqui a pouco.

@@03
Para saber mais: principais convenções de nomes

Acabamos de criar nosso primeiro teste! Uhull! Mas é o seguinte: vimos que a descrição é parte importante do teste, e que precisamos essencialmente de três informações nessa descrição:
Local;
Método;
Resultado.
Mas qual a ordem correta? Como posso me orientar melhor nesse assunto?
Para te ajudar mais nesse tema, separei um artigo do Macoratti que explica o quais as convenções de nomenclatura e o porque de todas elas!

Legal? 5 minutos de leitura apenas, acho que você vai curtir!

https://www.macoratti.net/20/12/net_unitconv1.htm

@@04
Utilizando expect()

[00:00] Agora nós já estamos criando os nossos testes, mas faltou um detalhe. Nós precisamos comparar os valores que estamos esperando com os valores que nós temos e se esses valores forem iguais, acabou.
[00:15] O que precisamos aqui? Precisamos usar uma nova função chamada expect, essa função também é do teste e ela precisa, primariamente, de duas coisas, ela precisa de um actual e de um matcher.

[00:29] O que vamos colocar aqui no nosso actual? Um valor atual, o que ele está buscando. Então, nós precisamos vir aqui no nosso bank, que nós criamos, que nada mais é do que um bank model. Buscando por bank., podemos acessar várias coisas. O points, o available, o earned, o spent.

[00:46] Vou verificar no points, porque ele é bem simples, ele sempre vai ser adicionado.

[00:50] Então, eu vou vir na linha 7, bank.points e precisamos adicionar um matcher. O que é esse matcher? Matcher é um valor que nós esperamos. Qual é o valor que estamos esperando nesse points? Estamos esperando 10, porque nós depositamos 10 dinheiros no nosso banco.

[01:07] Então, na linha 7, é o nosso matcher 10 e o que isso significa? Afinal, o que significa tudo isso? Nós criamos um modelo, nós usamos um método de adicionar 10 e nós estamos visualizando, verificando se os nossos pontos, realmente, estão valendo 10.

[01:27] Vamos ver se esse teste está passando? Para eu ver se o teste está passando, eu posso clicar aqui no nosso botão verde na parte superior à esquerda e clicar no botão Run, no botão verde à esquerda do número 4. Clicar no botão Run e ele vai verificar para mim se o teste é passável, ou seja, se o valor de pontos é realmente 10.

[01:48] Vamos ver se isso aqui está funcionado. Os primeiros testes são mais lentos, mas depois ele passa bem rápido.

[01:54] Olha só, deu a seta verde falando que o teste passou. Então é muito fácil, por enquanto está bem fácil. O que acontece, por exemplo, se eu vier aqui e trocar de 10 para 11 e tentar passar esse teste?

[02:09] O ideal é que não passe. Vamos ver se ele vai passar ou não? Não passou. O que acontece? O que ele fala para nós se o nosso teste não passar? Olha que maravilha que são os testes. Ele veio aqui e falou para nós Bank model deposit should be 10 e ele vem e fala aqui para nós que está esperando 11, mas achou apenas 10.

[02:33] Então, ele já dá uma noção para nós do que está errado. Eu vou voltar para o nosso 10 e se por algum acaso eu quiser testar outra coisa do nosso bank. No nosso bank, nós não temos só o nosso points, temos o available, nós temos spent, nós temos earned.

[02:51] Se eu tentar buscar esse valor no spent? Vamos verificar, de novo, no nosso bank model. Quando eu deposito, o valor de spent e não muda, só muda o valor de available, earned e points. Então, se eu tentar esperar um valor de spent igual a 10, o ideal é que o nosso teste não passe.

[03:18] Então, vamos tentar de novo, dessa vez eu cliquei aqui no nosso void main para testar todos os nossos testes de uma vez e também não vai passar, porque ele estava esperando 10 e o valor atual de gasto, de spent é 0.

[03:32] O ideal é que deixemos o nosso teste fixo. Então, é para nós visualizarmos apenas o nosso points, mas visualizando o que nós estamos esperando o nosso valor de points ser igual a 10, já dá para notar que a nossa descrição não está tão boa.

[03:55] O nosso Bank model deposit should be 10. Não é isso que queremos. Não é isso que estamos fazendo. Nós estamos verificando se o points é igual a 10.

[04:07] Então, Bank model deposit should turn points into 10, ou seja, nós estamos fazendo com que o nosso depósito do bank model transforme o valor de pontos em 10.

[04:28] Sim, descrições têm que ser longas, às vezes, é melhor você produzir nomes mais simples, mas se você não conseguir, podem ser nomes longos, não tem problema, o importante é que seja fácil de verificar.

[04:39] Então, o nosso teste está bem tranquilo, vou voltar aqui no nosso botão Run que vai visualizar todos os nossos mands e é simples assim? É simples assim, mas o poder do teste é muito maior do que simplesmente alterar os testes em si.

[04:56] O que acontece se eu alterar lá no bank? O que acontece se eu vier em bank.dart? Vamos supor que você está criando uma nova feature no seu projeto, no seu banco e dessa vez a quantidade de pontos em vez de ser só a quantidade de dinheiro que está entregada, vai ser "2 x money".

[05:23] Você adicionou 10, depositou 10 dinheiros, você vai ganhar 20 pontos. Você vez essa implementação, você mudou isso, significa que os testes que estão esperando um valor vão todos falhar e isso é ótimo, porque significa que quem está dependente desses pontos não vai ser pego de surpresa, porque o teste está esperto por nós.

[05:49] Então, estávamos esperando 10, mas virou 20, porque lá atrás nós decidimos mudar o nosso bank, sem lembrar que temos outras dependências em relação aos nossos pontos.

[06:01] Então, é bom ficarmos ligados no porquê de os testes fazerem tão bem para nós.

[06:05] Muito simples, muito tranquilo criar um teste básico com o nosso teste inicial unitário, mas não precisamos fazer só um teste, só testar uma coisa. Podemos testar várias coisas do nosso bank model, que é exatamente o que eu quero fazer com vocês na próxima aula.

@@05
Testando o BankModel

[00:00] Bom, agora nós já sabemos testar o depósito do nosso banco e nós precisamos um pouco mais de experiencia, de prática. Então, vamos testar outras coisas no nosso bank model
[00:13] Para isso eu vou diminuir o nosso resultado de testes. Nosso resultado de teste, agora, deve estar passando completamente, vamos só verificar se está tudo passando, porque arrumamos tudo na última aula, só não testamos de novo.

[00:30] Beleza, teste passou, 1 de 1. Vamos criar um outro teste. Depois do nosso teste final aqui na linha 8, eu vou criar um novo teste e dessa vez nós queremos testar a transferência, por exemplo.

[00:46] Então, 'Bank model transfer should turn points into 10', mesmo resultado, porque a transferência também adiciona pontos, vamos verificar. A transferência, nos pontos, adiciona o valor de money e nós queremos o valor de 10, porque foi uma convenção nossa, pode ser 100 aqui se nós quisermos.

[01:12] Vamos ter que mudar o valor do deposito, no nosso método deposit. Então, o mesmo esquema, nós temos a descrição, vamos para o body. Vou na linha 9 e criar a nossa função anônima, eu vou codar o ponto e vírgula para ele parar de marcar erro. Aqui dentro vamos criar, mais uma vez vamos instanciar o nosso bank model.

[01:34] "Por que temos que instanciar, de novo, o nosso bank model? Não faz sentido". Bom, ele não pode ser reutilizado de outro lugar, então, se eu decidir simplesmente vir aqui, vou comentar essa linha 10, só para vocês verem.

[01:50] Vou comentar essa linha 10, o bank foi criado, se eu quiser, simplesmente vir aqui bank.transfer, ele nem sabe o que fazer, porque ele não sabe o que é bank. Ele realmente não sabe o que é bank. Está até vermelho, na linha 11, nome indefinido, ele não vai pegar uma instancia que foi criar em outro teste.

[02:09] Então, importante esses detalhes de criação de instancias de variáveis ou de objetos.

[02:16] Beleza, nós temos aqui o nosso bank model, criado o nosso bank.transfer. Precisa de quê? Precisa de um valor, eu vou colocar o 10, porque é a nossa convenção. É a mesma coisa, agora nós precisamos verificar o nosso expect para ver se está funcionando direito.

[02:33] Então, vou na linha 12 no (actual), ele está procurando bank.points e o (matcher) tem que ser o quê? Tem que ser 10, obviamente, tem que ser 10. Vamos verificar se está dando certo?

[02:49] Vamos lá, apertei o botão Run, vamos ver se ele está realmente encontrando o nosso valor em 10. O teste passou, poxa, muito tranquilo e nós poderíamos ir testando várias e várias coisas do nosso bank model.

[03:04] O ideal é que você deixe o seu testes de bank model apenas nesse documento, nesse nosso arquivo .dart de model, apenas.

[03:13] "Poxa, Kako, mas eu quero rodar os dois testes ao mesmo tempo. Eu vou precisar rodar um de cada vez?". Bom, você pode vir aqui e rodar o main que roda todos os testes que estão dentro da função main e verificar se está tudo passando.

[03:29] "Que legal. Eu tenho outra dúvida", vocês são cheios de dúvidas, pode perguntar à vontade, inclusive, o fórum está lá para isso, pode perguntar. Então, temos mais uma dúvida e se nós tivermos um conjunto de testes que queremos testar separadamente?

[03:46] Por exemplo, eu vou criar mais alguns testes aqui. Acho que o teste a linha 4 está vermelho, porque não passou uma vez. Então, eu vou criar mais um teste, na linha 14, vou criar uns testes.

[04:01] Descrição desse teste, em vez do valor de points, eu quero verificar se o valor de available está correto. Eu vou aqui, 'Bank model deposit should turn available into 10', mais ou menos isso, tem que escrever direitinho.

[04:33] Então, vamos fazer de novo, a mesma coisa, o nosso body, ponto de virgula depois para ele não chorar e eu vou vir de novo e criar o nosso final bank. Agora aqui eu não preciso ir devagar, porque vocês já estão entendendo o que está acontecendo.

[04:49] Eu vou no deposito. Exatamente, eu já estava me atropelando aqui. Vamos lá, bank.deposit(10). Money, estou depositando 10 dinheiros e agora que eu tenho que esperar, expect, estamos esperando, agora sim eu vou colocar bank.available e o matcher tem que ser 10.

[05:24] Então, eu vou verificar o nosso bank, vamos ver se passa esse teste. O ideal é que passe, que nós sabemos que quando nós depositamos, o available sobre 10, mas agora eu quero testar todos os que estão em deposit ao mesmo tempo.

[05:38] Eu quero meio que agrupá-los, como é que eu os agrupo? Primeira coisa que nós temos que fazer é deixar os testes que nós queremos agrupar um em sequência do outro.

[05:46] Então, vou selecionar o nosso teste na linha 16 a linha 20, apertar os botões "Ctrl + X" para retirar e eu vou colocá-lo logo em seguida do nosso outro teste de deposito, onde está testando o deposito no points

[05:58] Testou os points aqui, estou testando o available ao mesmo tempo, mas eu quero que os dois rodem ao mesmo tempo sem testar o transfer. Tem como fazer isso?

[06:09] Tem como com uma função chamada group. Vou aqui antes do teste, do nosso primeiro teste na linha 5, e apertar o botão Enter. Agora eu vou na linha 6 group e ele já cria para nós uma descrição e um body, e dentro desse body nós vamos colocar os nossos testes.

[06:25] Então, deixa eu colocar um ponto e vírgula só para ele não chorar e no nosso description. Eu vou aqui falar 'Bank Model Deposit Tests'. Coloquei tudo em maiúscula e nem precisava. Então, eu vou vir aqui, 'Bank model deposit tests'.

[06:43] Dentro desse grupo eu posso colocar vários testes que têm a ver com o nosso depósito. Então, eu vou na linha 9 até a linha 18 e selecionar o nosso teste de pontos e o nosso teste de available. Vou apertar os botões "Ctrl + X", deixar apenas o nosso teste de transferência lá fora, e dentro do group, na nossa linha 7, eu vou apertar os botões "Ctrl + V" e colocar todos os testes ao mesmo tempo.

[07:05] Então, só para vocês terem certeza de que tudo está dando certo. Nós temos, na linha 6, um grupo com duas setas, o significa que nós vamos testar vários testes de uma vez.

[07:17] Então, se eu clicar nele para dar um Run, nós vamos ver que ele vai passar dois testes. Opa, mas nós temos três testes e nós podemos só ter certeza de que temos todos os testes funcionando, se nós rodarmos o nosso void main que vai testar o grupo e ainda o teste que está lá fora. Então, serão três testes.

[07:36] Legal, nós podemos brincar com isso. Tem muitas coisas que o nosso bank model que podemos testar, fiquem à vontade. O ideal mesmo é, em grandes projetos, você testar absolutamente tudo.

[07:48] Então, você tem que testar o spent, tem que estar o available do transfer, tem que testar o earned do deposit. Teste tudo que os métodos estão fazendo para ter certeza.

[07:59] Porque se no futuro alguém vier e alterar o seu método, os testes vão acusar e isso é qualidade de projeto, porque você não vai ter dor de cabeça para descobrir o que deu errado, o teste te fala o que deu errado, olha que maravilha.

[08:15] Era isso que eu queria passar para vocês nesse vídeo, muito obrigo e vejo vocês daqui a pouco.

@@06
Função expect()

Aprendemos a produzir um teste e vimos que ele precisa de uma descrição e de um corpo, no qual temos os métodos que desejamos testar, porém precisamos usar uma função chamada expect() que espera por um resultado.
A função expect() precisa de um actual e de um matcher. Qual a responsabilidade de cada um respectivamente?

O actual é um objeto genérico disponibilizado pelo pacote test e o matcher é o objeto do nosso projeto.
 
Alternativa correta
O actual é o valor da variável atual e o matcher é o valor esperado dessa variável.
 
Corretíssimo! No primeiro, devemos colocar a variável que desejamos comparar e, no segundo, indicamos o valor que esperamos dessa variável após a utilização dos métodos. Assim, garantimos que nosso projeto está seguindo nossos desejos a todo instante.
Alternativa correta
O actual é sempre uma String e o matcher é sempre um int.
 
Alternativa correta
O actual é o valor da variável no passado, enquanto o matcher é o novo valor dessa variável.

@@07
Faça como eu fiz: testando 1, 2, 3

Chegou a hora de testar seu conhecimento!
Vamos criar um novo teste para seu aplicativo, para isso siga nosso passo a passo:

Crie um novo arquivo na pasta test;
Produza um teste com uma boa descrição;
Teste o máximo que conseguir da Classe que escolheu testar;
(lembre-se não existem testes demais);
Faça grupos de testes!
Vamos lá?

O objetivo desta atividade é estimular você a produzir vários testes no seu aplicativo.
Um exemplo de código que poderia ser testado é o caso do “Spent” quando usamos o método transfer():

test('Bank model transfer should turn Spent into 10', (){
  final bank = BankModel();
  bank.transfer(10);
  expect(bank.spent, 10);
});COPIAR CÓDIGO
Com muitos testes, você vai notar que: muitas classes e métodos estão conectados, e fazer alterações no seu projeto vai ser um trabalho menos exaustivo, pois os testes vão te guiar nas dependências entre objetos.
Caso tenha alguma dúvida, chame a gente no fórum!

@@08
O que aprendemos?

E aí? Pronta(o) para revisar?! Acabamos de ver alguns novos conceitos úteis para produzir aplicativos com qualidade no Flutter:
Pasta Test:
Existe uma pasta, em nosso projeto, destinada apenas aos testes que faremos em nosso aplicativo. Essa pasta já possui um teste padrão que vem junto com o projeto inicial. É imprescindível que os testes sejam criados nela.

test():
Função herdada do pacote de testes do Flutter, que permite a iniciação de um teste simples de unidade. Ele pede por uma descrição (que precisa ser bem estruturada) e por um body (que é responsável pelas ações do teste).

expect():
Método usado dentro do test() para comparar o valor da variável e o valor esperado por essa variável. Para isso, precisamos usar o actual e o matcher.

group():
Método que agrupa diversos testes, para facilitar quando precisamos rodar diversos testes juntos, facilitando a produção.

Finalizamos a Aula 2!

Estamos evoluindo bem no conteúdo de testes no Flutter! E aí, o que está achando? Conta pra gente lá no fórum ou no Discord da Alura!

Te vejo logo, logo!

#### 04/01/2024

@03-Realizando testes de Widget

@@01
Projeto da aula anterior

Caso queira, você pode baixar o projeto do curso no ponto em que paramos na aula anterior.

@@02
Diferenciando teste manual e automatizado

[00:00] Agora já sabemos fazer os nossos testes de unidade. Lembrando que o nome correto é teste de unidade e não testes unitários. Só para desencargo de consciência.
[00:14] Já sabemos fazer teste de unidade, tanto que testamos uma classe que é o nosso bank model. Mas agora precisamos adentrar um pouco mais em testes mais difíceis. Vamos começar a explorar um pouco os testes de widget.

[00:29] Porém, antes de já chegar de cara nos testes de widget, eu quero conversar um pouco com vocês sobre a grande diferença entre testes automatizados e testes manuais. Qual que é a grande diferença?

[00:42] Vamos criar uma história, vamos criar um momento nosso. Vamos supor que eu quero mudar a cor lilás do nosso aplicativo, a cor lilás que é um degradê que está em cima do nosso aplicativo, de um azul mais escuro e vai ficando mais roxo.

[01:01] Eu quero mudar essas cor. Então, eu vou no header, na parte esquerda, onde está esse código, header está dentro do components, dentro da seção sections e na linha 27, dentro desse header, temos as nossas três cores que compõem esse degradê.

[01:14] Eu não quero mais esse degradê. Vamos mudar a cor, eu não quero mais que seja azul, eu quero seja completamente vermelho. Vamos ver aqui, zero no azul, zero no verde e agora um vermelho. Vou colocar 255 para ficar super vermelho.

[01:34] Eu quero seja essa cor e mudei o nosso código. O que é natural fazer? O natural de nós, desenvolvedores, fazermos é apertar o botão Hot Reload e visualizarmos se o nosso código corresponde ao que nós queremos visualmente. Então, vamos ver.

[01:50] Apertando o botão Hot Reload e ficou bem chocante. Mudou e nós visualizamos que mudou. Então, acabamos de fazer um teste manual para verificar se a cor que nós colocamos no código está aparecendo, de fato, no nosso projeto.

[02:09] Agora imagina o seguinte, imagina que temos várias páginas, dez páginas para verificar. Teríamos que verificar todas as páginas uma a uma para ter certeza de que todas pegaram essa nova cor vermelha e demoraria um pouco mais de empo.

[02:27] Assim os testes manuais começam a ser um pouco mais custosos porque demoramos um tempo para fazer, mas e se automatizássemos? E se tivéssemos um robô que fizesse isso por nós? Que verificasse se essa cor está correta em todas as outras páginas?

[02:43] É isso que compõe o teste automatizado. Nós criamos um código, um robô, que testa todos os locais em que programamos esse robô. Então, ele vai testar todas as supostas dez páginas para verificar se as cores estão corretas.

[03:02] Demoraríamos alguns segundos para fazer, enquanto o robô, que é bem rápido, faria isso em menos de um segundo. Então dá para perceber que testes automatizados são muito mais velozes do que testes manuais nesse nosso contexto que acabamos de criar.

[03:18] Só para não ficar muito confuso, eu vou voltar as nossas cores para não termos problemas, eu vou apertar o botão Hot Reload para verificar. Voltou. Mas lembrem-se, se nós, humanos, fossemos testar, visualizar e observar pessoalmente cada um dos detalhes que mudamos no nosso código.

[03:38] Sempre que mudássemos alguma coisa, iriamos demorar muito tempo, enquanto, se deixarmos esse trabalho para um robô, ele faz isso em segundo, às vezes, menos e essa é a ideia do teste automatizado.

[03:51] Então, agora nós vamos começar a criar o nosso teste de widget automatizado que vai testar cada um desses nosso componentes que nós criamos individualmente de uma forma muito mais veloz do que nós poderíamos fazer fisicamente. Vejo você daqui a pouco.

@@03
Utilizando pump()

[00:00] Agora vamos começar a produzir um teste de widget. Por onde nós começamos?
[00:12] Nós temos que criar o nosso documento em dart. Então, vamos na nossa pasta test, criar um Novo Dart File, como nós já sabemos e o nome desse dart file vai ser home_test. Sabe por quê?

[00:24] Porque nós vamos testar o widget home. "Mas, Kako, que widget é esse?". Vamos conferir no nosso main.dart. Se nós olharmos o nosso main.dart que é o nosso principal documento inicial.

[00:37] Ele tem o Home aqui dentro que é filho de nosso BankInherited que é filho de MaterialApp que, por fim, é o nosso MyApp que é o aplicativo inteiro.

[00:49] Então, o Home ele é, na verdade, nada mais, nada menos, do que a nossa tela. Então, tudo o que está desenhado na nossa tela está dentro do Home.

[00:59] Então, vamos verificar no lado esquerdo da tela, dentro de screens, a nossa pasta screens, nós temos apenas uma tela que é o Home. Se eu clicar aqui nós abrimos o Home e dentro nós temos vários outros componentes que compõem toda essa tela que nós estamos vendo no nosso projeto.

[01:13] Nós vamos fazer um teste widget com widget mais completo do nosso projeto. Você poderia fazer, caso você quisesse, um teste com widget menor. No meu caso eu quero colocar teste no Home justamente, porque ele é um widget completo e ele vai conseguir entender melhor essas questões de testes widget usando um widget completo.

[01:35] Estamos testando o Home, esse é o nosso teste e como é que nós fazemos para testar esse nosso widget? Primeiramente, como normalmente nós fazemos, precisamos criar um void main que é a nossa função principal, nós precisamos também importar o nosso Flutter teste que nós vamos utilizar.

[02:00] E agora nós temos que começar os testes. Como é que nós começamos o teste da última vez? Nós começamos com uma função chamada test, mas aquilo lá era para o nosso teste de unidade, agora nós vamos testar um widget.

[02:12] Para começar a testar um widget, nós vamos usar uma função levemente diferente que é o testWidgets, vou apertar o botão "Tab" e ele vai escrever para mim. O testeWidgets é levemente diferente, ele tem um description e ele tem, em vez de uma função, que ele espera uma função no teste de unidade.

[02:33] Agora nós temos um call back e esse call back usa um widgetTester. Esse widgetTester é o nosso robô que eu falei lá atrás. Lembra que nós podemos fazer os nossos testes manualmente? Nós podemos criar um robô que testa por nós? Esse aqui é a personificação do nosso robô.

[02:51] Inclusive vou até mudar o nome dele aqui para (tester), é o nome do nosso robô. Então, é o tester quem vai olhar e verificar cada um dos pontos que estamos buscando nos testes que vamos fazer.

[03:02] Beleza, vamos mudar nossa descrição. O que eu quero testar especificamente nesse teste de widget inicial? Não vou testar tudo, não vou chegar aqui agora com vocês e testar tudo o que está nessa tela. Vou testar um elemento por vez.

[03:19] Eu quero ver se esse spent, no projeto, que em português significa gasto. Eu quero verificar se esse spent está, de fato, aparecendo na dela.

[03:30] Então, eu vou colocar uma descrição aqui escrito 'My widget has a text "Spent" ', vou até colocar entre parênteses esse "Spent" só para ficar mais claro. Temos a descrição, temos o nosso call back e agora eu vou colocar um ponto e vírgula, na linha 3, só para não ter esse problema e vou mudar de seta para chaves.

[04:03] Para nós podermos entender o que está acontecendo. Agora nós temos os nossos testes de widgets e como é que nós construímos o nosso teste de widgets?

[04:14] Inicialmente, primeira coisa que eu vou fazer é dizer que esse call back aqui tem que ser assíncrono. Logo explicarei para vocês por que ele tem que ser assíncrono, mas basicamente nós temos que esperar algumas coisas acontecerem.

[04:27] Segunda coisa que nós temos que fazer é, nós temos que desenhar uma tela, nós temos que construir uma tela, temos que buildar uma tela, porque é um widget e um widget é um componente visual.

[04:40] Então, nosso robô, o nosso tester, ele tem que criar essa tela e verificar se os objetos estão, de fato, dentro dessa tela.

[04:49] Então, como é que nós construímos essa tela? Primeiramente nós vamos ter que chamar um await, porque essa função demora para acontecer. E eu vou falar que o nosso tester, ou seja, o nosso robô, ele tem que fazer uma nova funcionalidade, ele tem que fazer uma nova coisa.

[05:03] O que ele tem que fazer? Ele tem que pumpWidget. O que significa pumpWidget? Ele tem que criar, ou seja, buildar, como você desejar. Ele tem que criar, desenhar esse widget na tela para ele verificar. Primeira coisa que ele tem que fazer é desenhar o widget na tela.

[05:22] Que widget é esse que nós queremos desenhar? É o nosso Home. Eu posso vir aqui e apertar os botões "Alt + Enter" para ele achar para nós o Home, deixar eu colocar um ponto e vírgula aqui para não ter problema e ele vai pedir para importar o nosso Home.

[05:42] Mas se eu apenas pedir para ele importar o nosso Home para ele desenhar apenas o Home, vamos ter um problema. Sabe por quê? Vamos voltar lá no nosso main.dart, só para vocês entenderem um detalhe, e aqui que começa a brincadeira.

[05:59] O Home é filho de um BankInherited que é filho de um MaterialApp. Então, a partir do momento que o Home é dependente de outros widgets, nós temos que saber isso na hora do teste.

[06:14] Porque se eu tentar testar apenas um Home vai dar problema, porque o Home precisa de informações que estão dentro do nosso BankInherited, assim como ele também precisa de informações que estão dentro do nosso MaterialApp.

[06:32] Então, lembra lá atrás quando nós falamos, na tabela, de que testes de unidade tem pouquíssimas dependências e testes de widget já tem um pouco mais de dependências. É aqui que começamos a ver esse detalhe, o Home depende de outros widgets para funcionar perfeitamente.

[06:48] Então, nós não podemos chegar aqui e simplesmente chamar um Home para desenhar. Nós precisamos chamar a partir do MaterialApp, o BankInherited e o Home, para poder desenhar na nossa tela.

[07:03] Então, vamos fazer isso? Sabendo tudo isso, vamos lá no nosso Home teste e vamos alterar para não ser apenas o Home. Vamos deletar Home() e eu vou criar o MaterialApp e esse MaterialApp tem um Home.

[07:22] Esse nosso MaterialApp, um dos parâmetros dele é home: e o home desse MaterialApp vai o nosso BankInherited, vai ser um widget que precisa de um child e o child vai ser o nosso Home.

[07:37] Vou apertar os botões "Ctrl + Alt + L" só para ficar bonito aqui e colocar uma virgula ficar tudo certo. Agora sim nós estamos criando, desenhando a nossa tela inteira para o tester poder procurar o nosso texto Spent.

[07:55] Mas, opa, espera aí, nós acabamos de desenhar na tela com o função pumpWidget. Como é que nós procuramos widget que está aqui dentro? A informação que está aqui dentro?

[08:08] Para isso nós precisamos de uma função que procura, que encontra e é isso que nós vamos ver daqui a pouco.

@@04
Utilizando Finders

[00:00] Nesse instante nós acabamos de construir a nossa tela para o tester poder testar as coisas. Ele está desenhado na tela do nosso teste. Só que nós precisamos procurar algum objeto dentro dessa nossa tela. No caso, o objeto que nós estamos procurando é o texto Spent, ou seja, gasto, em português.
[00:23] Como que nós fazemos para procurar alguma coisa no nosso teste? Para isso nós precisamos do finder. Para isso eu vou criar aqui um final e eu vou chamar esse final de spentFinder é um finder é alguém que procura, está procurando alguma coisa

[00:40] E esse finder vai ser um find, é um comando de procurar e ele vai procurar um texto dentro desse nosso teste, dentro dessa tela que foi desenhada.

[00:55] Que texto é esse? O texto é 'Spent'. Lembrando que tem que ser exatamente igual ao que nós estamos procurando, se for com um espaço ou com um S minúsculo, ele não vai achar da forma como nós estamos procurando.

[01:10] Então, certifique-se de que o texto está certo. Nós estamos procurando um texto e usamos uma função find para procurar o texto no nosso home.

[01:23] Legal, ele procurou o find e agora? Agora ele tem que comparar para ver se realmente esse find está lá dentro. Como é que nós fizemos isso das últimas vezes? Nós usamos a função expect, exato, então, nós pegamos uma informação que estamos buscando e compara para ver se a informação é a que nós queremos mesmo.

[01:44] Então, eu vou pegar e dizer que o actual é spentFinder que essa informação é que está sendo buscado e o matcher que é aquilo que nós estamos querendo comparar vai ser findsOneWidget. "Como assim findsOneWidget, Kako? Não era para ser spent? Não era para ser só um texto?"

[02:09] Não, porque agora nós estamos testando widgets e ele vai apenas procurar se esse widget existe ou não, se existem vários widgets, quantas vezes esse widget existe.

[02:19] Calma, daqui a pouco nós vamos ver outros tipos de matchers, mas por enquanto nós vamos ter que procurar, vai ter que comparar isso com findsOneWidget.

[02:28] Até porque só existe um widget que tem o texto chamado Spent na nossa tela, no nosso home. Então só recapitulando. Nós acabamos de desenhar a tela, criamos um procurador, um finder que procura o nosso texto e nós comparamos com o nosso expect, se esse texto que foi procurado existe apenas um widget nessa construção inteira, nesse teste todo.

[02:57] Tudo isso para ver se o nosso teste, se a nossa tela tem Spent dentro. Então, eu vou clicar no Run, vamos ver se o teste passa. Passou.

[03:10] Legal, aqui eu nem vou ficar brincando de ficar mudando o nome de *Spent. Vocês podem testar à vontade se quiserem, porque eu quero falar de outros tipos de finders antes de terminar essa aula.

[03:20] Existem vários tipos de procurados, nós não precisamos procurar apenas textos, nós podemos procurar widgets específicos.

[03:28] Então, é isso que eu quero fazer agora. Para facilitar a nossa vida, já vou criar aqui mais um teste widget, depois de outro teste de widget, linha 16, testWidgets e eu vou procurar um outro widget. O widget que eu quero procurar dessa vez é essa barra de progresso linear bem no centro do nosso aplicativo, que ela vai crescendo de acordo com o quanto que gastamos, só para vocês lembrarem.

[03:52] Vou colocar vários depósitos e alguns transfers, vou atualizar, está vendo? Ele vai subindo e vai descendo. Então, vou colocar aqui na nossa descrição que é 'find a LinearProgressIndicator', que é o nome desse widget e podemos fazer da mesma forma como nós fizemos lá atrás.

[04:16] Nós desenhamos o nosso home baseado no bank inherited e no MaterialApp, tem que ser assíncrono. Vamos deixar tudo bonito, bem alinhado.

[04:34] Então, aqui dentro, primeira coisa que nós temos que fazer é desenhar a tela. Então, vou copiar da linha 8 até a linha 12 o nosso pumpWidget que vai desenhar na tela para a nós. pumpWidget, o nosso home, eu não quero ficar repetindo.

[04:47] Mas lembrando que só porque foi feito aqui no nosso teste de spent, não quer dizer que não tem que ser feito aqui embaixo em outro teste. São testes diferentes. Então, nós temos que inicializar de novo, mesmo esquema que vimos nos testes de unidade quando nós precisávamos instanciar um objeto.

[05:06] Então, agora nós queremos procurar outra coisa, não estamos procurando o finder, estamos procurando o LinearProgressIndicator, especificamente ele.

[05:15] Então, como é que nós procuramos um widget que nem tem texto? Eu nem preciso criar um final, se eu quiser. No caso eu vou até alterar aqui para não ficar igual, já vou direto no expect.

[05:33] E aqui no actual aqui eu posso criar um finder diretamente. Então, eu posso escrever find, só que existem vários tipos de find, existe find.byText, byElement, byWidget. No caso, nesse instante eu vou usar o find.byType e eu vou procurar qual é tipo de widget que eu estou procurando.

[05:52] No caso é o nosso LinearProgressIndicator, não é o widget, é o tipo de widget. Isso aqui é a classe do widget, não o widget, em si.

[06:02] Então, o LinearProgressIndicator e o matcher que eu estou procurando. Quantos LinearProgressIndicators existem? No caso existe só um. Então, findsOneWidget. Vamos verificar se isso está dando certo? Vamos lá, vou rodar e o ideal é que ele passe.

[06:23] Teste passou, ele encontrou o nosso LinearProgressIndicator e antes de terminar, eu quero passar mais um tipo de finder. Lembrando que existem vários tipos de finders. Vocês podem clicar aqui no find. , ponto e procurar vários tipos de finders

[06:37] O último tipo de finder é o finder bykey. Então, nós vamos procurar um widget baseado na key daquele widget, a chave especifica daquele widget.

[06:46] Primeiro nós temos que verificar qual é a key, onde que tem uma key e nós não temos nenhuma key. Vamos criar uma key agora em um widget específico.

[06:56] Então, primeiro ponto. Vamos colocar uma key em algum widget dentro do nosso home. Todos esses componentes, essas seções estão dentro do nosso home.

[07:04] Então, eu vou no nosso recent_activities.dart, lado esquerdo da tela, e vou entrar nele. Todos esses componentes aqui estão dentro do home e eu posso colocar uma chave em qualquer um deles, porque eles vão estar dentro da tela que vamos desenhar no nosso teste.

[07:19] Então, dentro do recent_activities, eu vou abri-lo aqui, que é um dos widgets que eu escolhi e eu vou procurar um widget específico dentro para colocar uma chave nele.

[07:28] Por exemplo, nós temos na linha 13 um Box Card e esse Box Card recebe um Account Status. Esse Account Status eu quero colocar uma chave nele, eu quero nomear uma chave para que esse widget seja único por chave.

[07:42] Então, eu vou no nosso Account Status já vou falar key e ele pede uma key que é um objeto, um widget key e esse widget key, deixa eu botá-lo como widget. Ele precisa de um texto dentro que vai ser especificamente essa chave de acesso única apenas para o Account Status.

[08:06] Qual vai ser o nome dessa chave? Eu vou escrever uma chave bem simples que é 'testKey', deixa eu apertar os botões "Ctrl + Alt + L" para visualizar com facilidade.

[08:13] Então, acabamos de adicionar uma chave no nosso Account Status. Você pode fazer isso com qualquer widget. O ideal é que a sua chave seja única mesmo, não uma palavra específica. Assim você consegue procurar vários widgets em projetos gigantescos.

[08:27] Acabamos de adicionar uma key no Account Status e temos que verificar se esse widget, por chave, pode ser encontrado no nosso teste. Vamos testar?

[08:39] Vamos lá no home_test.dart, vamos criar mais um teste widget, de fato, eu vou até copiar da linha 16 até a linha 23, porque é quase igual, quase a mesma coisa. Vou apertar os botões "Ctrl + C" em tudo, apertar o botão Enter e apertar os botões "Ctrl + V" e temos um outro teste.

[08:54] Só que agora nós não estamos procurando um LinearProgressIndicator, estamos procurando o nosso Account Status, especificamente.

[09:01] Então, eu vou escrever 'finds a LinearProgressIndicator' na linha 4. Vou deletar e escrever no lugar 'finds a AccountStatus' e nós temos que mudar apenas uma coisa que é o nosso expect.

[09:23] Então, em vez de ser find.byType, eu vou deletar o find.byType, e escrever find., ponto. Lembrando que nós temos todos esse tipo de forma de procurar widgets, fiquem à vontade, mas eu vou o key só para mostrar para vocês que essa é uma das formas mais legais de procurar um widget específico.

[09:42] E agora ele vai, simplesmente, perguntar para nós qual vai ser a chave que ele está procurando. Então, tem que ser um widget key como valor que é a nossa string 'testkey' e mais uma vez isso tem que estar escrito exatamente igual a nossa chave lá no nosso Account Status.

[10:00] Se tiver um pouco diferente ele não vai encontrar. Então, agora é só testar o nosso teste widgets. Gente, às vezes essa seta, do lado direto, na linha 24, ela some, normal, as vezes dá uma bugada. É só você refazer o teste que ele volta, você pode testar com facilidade.

[10:18] Caso você não consiga achar, você pode vir aqui em cima, parte superior esquerda, onde, normalmente, temos o nosso main.dart. Tem todos os testes aqui embaixo com o nome bonito e você pode procurar o teste que você quer e fazer rodar normalmente como se fosse um aplicativo.

[10:32] Mas eu vou clicar na linha 24. O jeito padrão que nós temos, clicando na esquerda, e verificar se nosso teste vai passar. Ele vai procurar o widget que tenha a chave e passou, olha que legal.

[10:42] Agora acabamos de ver várias formas de procurar widgets, foi um vídeo um pouquinho maior, mas foi bom que deu para passar tudo o que eu queria passar para vocês e caso vocês tenham vontade de experimentar outros tipos de find fiquem à vontade. Qualquer coisa só usar o fórum que nós ajudamos.

@@05
Para saber mais: documentação CommonFinders

Existem diversos tipos de Finders disponíveis para facilitar sua busca por um Widget específico.
Para quem tem mais curiosidade, separei uma pagina da documentação oficial do Flutter que fala sobre todos os métodos do tipo find:

CommonFinders
Aproveite para conferir e incrementar seus estudos!

https://api.flutter.dev/flutter/flutter_test/CommonFinders-class.html

@@06
Entendendo os Matchers

[00:00] Agora nós já começamos a entender a questão de testar um widget. Nós primeiro temos que criar a tela e dentro dessa tela simulada nós procuramos por um widget específico, pode ser com chave, pode ser tipo, pode ser por texto, pode ser por várias coisas e depois nós comparamos com o valor de retorno que, no caso, é o findsOneWidget.
[00:25] "Espera, valor de retorno? Calma lá, Kako, você não falou nada disso". Está bom, vamos falar um pouco mais sobre o matcher. Aqui no nosso expect, nós temos o actual que é onde tem o find.byKey e nós temos o matcher que, nesse caso, nós temos o findsOneWidget.

[00:43] Se você colocar o mouse em cima do findsOneWidget, ele vai te falar que existem outros tipos de matchers que pode ser o findsNothing que não encontra nada, o findsWidgets que descobre se existem widgets, um ou mais, mas não define o valor. Existe também o findsNWidgets que procura o número específico de widgets.

[01:05] Então, esse que é o matcher, ele é aquele com o qual vai ser comparado o valor do que estamos buscando.

[01:12] Então, para nós podermos ter uma visão um pouco melhor de como esse matcher funciona, eu quero usar o findsNWidgets, e para isso nós precisamos procurar um widget que aparece várias vezes no nosso projeto.

[01:25] Que widget que está aparecendo? O que está aparecendo aqui várias vezes no nosso projeto? Vamos dar uma olhada?

[01:31] Então, no nosso projeto inteiro, emulador, nós temos os headers, nós temos esse bloco que é o nosso status, nós temos esses três botões, esses três blocos que são as nossa ações, aqui embaixo nós temos esse grande bloco que são os nosso pontos.

[01:49] Então, fica um pouco difícil de visualizar o que está sendo repetido aqui, mas eu falei uma palavra várias vezes e exatamente essa palavra que está sendo repetida várias vezes no nosso projeto.

[02:01] Bloco, nós temos um bloco no status, é uma margem, é como se tivesse uma cor diferente, cinza claro. Nós temos esse mesmo formato no botão deposit, o mesmo formato no botão transfer, no scan também e assim como aqui embaixo em Account Points. Isso é um widget.

[02:18] Vamos verificar no nosso código? Vamos dar uma olhada aqui nos nossos diretórios. Opa, eu não quero que fique aparecendo isso aqui, então, eu vou clicar.

[02:30] Aqui nos nossos componentes, lado esquerdo da tela, nós temos vários de tipos de componentes e em vez de section, só dentro de componentes mesmo, nós temos um widget chamado box_card.dart, vamos neles.

[02:41] O Box Card é um widget específico, vou até deixar aqui o home teste para a esquerda para ficar organizado. O Box Card é um widget que forma essa decoração inteira, essa decoração específica em quesito de formato, de cores, de temas.

[02:59] Então, o Box Card está aparecendo várias vezes no nosso projeto. Vamos dar uma olhada em quantas vezes ele aparece no nosso projeto?

[03:05] O primeiro lugar que ele está aparecendo é nosso recent_activities.dart, na linha 13, quando nós estamos criando o nosso AccountStatus. Lembra do AccountStatus? Acabamos de criar uma chave para ele. Agora pouco criamos uma chave para ele.

[03:21] O AccountStatus nada mais é do que o status dessa informação dentro nosso projeto onde possui o spent, onde possui o earned, possui o nosso LinearProgressIndicator. Isso aqui tudo está dentro de um Box Card.

[03:38] Beleza, já achamos um Box Card faltam mais, já dei spoiler aqui, mas faltam mais.

[03:45] Então, qual é o próximo que nós temos que olhar? Aqui nós temos os points_exchange.dart e o points_exchange.dart tem aqui o nosso Account Points e o Account Points está dentro do Box Card, linha 20. Opa, tem mais um Box Card que denomina todo esse espaço em volta do nosso Account Points.

[04:04] Beleza, já achamos os dois. O que mais nós precisamos procurar? O nosso actions.dart, na linha 51, também possui Box Cards, um deles para cada botão.

[04:21] Então, vamos verificar, eu vou voltar aqui em cima, na linha 29, nós temos o Box Card do deposit. Então, nós temos toda uma atividade que compõem o deposit está dentro de um Box Card.

[04:33] A mesma coisa aqui embaixo, na linha 40, para o transfer também é um Box Card e a mesma coisa aqui no scan, linha 51, que é outro Box Card. Caramba, achamos cinco Box Cards dentro do nosso projeto.

[04:45] Então, quando nós formos fazer um teste que procurar um Box Card, nós estamos procurando por cinco widgets especificamente dentro desse nosso teste específico, dentro do home_test.dart.

[04:56] Então, vamos criar isso. Como que nós fazemos isso? Para isso vamos criar um novo teste e nós vamos até aprender a usar um novo finder, mas vamos uma coisa de cada vez.

[05:07] Novo teste, testWidgets, mesma coisa que nós fizemos, a descrição vai ser 'finds a BoxCard'. No caso, não vai ser a Box Card, vai ser find 5 BoxCards para nós já termos certeza, quando o teste passar, se está dando certo na descrição.

[05:27] O nosso tester, vou mudar WidgetTester só para tester para ficar padronizado. Vou trocar de seta para chave, linha 32, pôr um ponto e vírgula. Lembrando que isso aqui tem que ser assíncrono, porque nós estamos desenhando a tela. Então, eu vou no nosso async.

[05:46] E vamos lá, agora nós temos que colocar o nosso dentro do nosso teste. Nós temos que mandar um await, porque temos que esperar, espera o quê? Esperar para a nossa tela ser construída.

[06:01] Nossa tela vai ser construída pelo tester o nosso robô e o nosso tester precisa usar o pumpWidget para construir os widgets que estão aqui dentro com calma.

[06:13] Então, quais vão ser os widgets? Mais uma vez nós já fizemos isso antes, vou, inclusive, para facilitar a nossa vida, copiar o MaterialApp, BankInherited e o Home(), vou apertar os botões "Ctrl + C" da linha 25 até a linha 29. Acho que eu copiei do jeito errado.

[06:32] Então, eu tenho que vir da linha 29 a 25, mas eu não preciso copiar o ultimo parentes e o último ponto e vírgula, porque já está aqui.

[06:43] Era exatamente isso, vou apertar os botões "Ctrl + Alt + L" para ficar indentado. Já desenhamos a nossa tela, agora o que nós precisamos? Precisamos do finder, precisa do expect, precisa do matcher.

[06:55] Eu já vou colocar isso tudo junto. Vou criar, na linha 38, um expect e precisa de um actual e precisa de um matcher. Poxa e esse actual? Como é que vai ser?

[07:05] O nosso actual nós vamos usar o find. só que dessa vez não vai ser byKey, não vai ser byType, vai ser finds.byWidgetPredicate. O que isso aqui significa? Significa que nós vamos verificar um widget e nós vamos procurar se esse widget bate com o nosso Box Card.

[07:31] Nós vamos comparar vários tipos de widget, predicado dos widgets, se ele tem uma estrutura igual, na verdade. Ele vai comparar as classes que criamos do Box Card.

[07:44] Como é que nós fazemos isso aqui? Nós vamos ter que fazer uma nova comparação. Eu vou vir aqui, ele pede o widget, ele está pedindo um widget e uma função call back

[07:54] Aqui dentro do nosso widget, eu vou com uma condição if que vai perguntar se o widget que nós estamos comparando, ou seja, ele vai olhar cada um dos widgets dentro da nossa tela, ele vai olhar cada um deles e vai perguntar se esse widget.

[08:10] Vou aqui, linha 39, se o widget é um Box Card. Se for um Box Card, eu vou codar um if é uma condição, se for um Box Card, retorne true. Caso não seja um Box Card, então, else para ficar bonito, caso não seja retorne false.

[08:37] Então, o que ele está fazendo aqui? Esse nosso find.byWidgetPredicate está olhando cada um dos widgets e está comparando se esse widget é um Box Card, se for, verdadeiro, se não for, falso.

[08:49] E agora só falta o nosso matcher. Deixa eu dar um ponto e vírgula na linha 46 só para ele não dar erro. Agora falta o nosso matcher que é comparando quantos widgets foram encontrados.

[08:58] Então, findsNWidgets, eu vou descer aqui para codar findNWidgets, linha 46, e esse findNWidgets é um método, uma função que pede uma quantidade.

[09:11] Então, primeira coisa, respira fundo, eu sei que é muita coisa. Toma uma água, se hidrata. No meu caso estou tomando um chá para dar uma acalmada. Pode ser café, pode ser água, mas o importante é você se hidratar.

[09:25] Vamos lá, o nosso findsNWidgets é uma função que requer uma quantidade de widgets que estamos procurando. Então, no caso, eu vou colocar o valor de '5'. Pronto, acabamos o nosso teste um pouco mais complexo, porque o nosso finder agora está procurando por predicado em cada um dos nossos Box Cards.

[09:47] Vamos ver se nosso teste está passando? Esperando e passou, quer dizer que ele encontrou todos os cinco Box Cards dentro da nossa tela.

[10:01] Lembrando que você pode testar, se você colocar 4, vê se passa, você mudar o tipo de widget e ver se ele encontra. Fica à vontade para testar e brinca um pouco.

[10:12] Até daqui a pouco.

@@07
Para saber mais: documentação Additional Matchers

Existem diversos tipos de Matchers disponíveis para relacionar a quantidade de Widgets encontrados.
Para você aprofundar os estudos, separei uma página da documentação oficial do Flutter que mostra os diferentes Matchers disponíveis.

Matchers Adicionais
Recomendo dar uma olhadinha!

https://docs.flutter.dev/cookbook/testing/widget/introduction#additional-matchers

@@08
Procurando Widget

Vimos diversas formas de procurar um Widget nessa última aula, chegamos a utilizar algumas delas
Quais são, na ordem correta, os finders para: encontrar por chave, por predicado, por tipo e por texto?

byWidgetKey ; byWidgetPredicate ; byWidgetType ; byWidgetText
 
Alternativa correta
Key ; WidgetPredicate ; Type ; text
 
Alternativa correta
byKey ; byPredicate ; byType ; byText
 
Não, o by não é obrigatório como nome dos métodos Find.
Alternativa correta
byKey ; byWidgetPredicate ; byType ; text
 
Isso ai! Nem todos eles tem o mesmo formato/padrão de nomenclatura.

@@09
Faça como eu fiz: cadê o Widget?

Testou? Vamos aplicar o que foi visto durante as videoaulas, então!
Vamos criar um novo teste de Widget para seu aplicativo, e lembre-se de:

Verificar as dependências necessárias para dar pump no Widget;
Produzir um teste com uma boa descrição;
Procurar vários Widgets com diferentes Finders;
Utilize diferentes Matchers para quantidades distintas de Widgets.
Também testamos a ação do nosso botão de depósito (deposit), agora é a sua vez de testar as seguintes ações que ocorrem no projeto Alurabank:

Botão transfer:
Seção Available balance;
Seção Spent.
Vamos lá?

O objetivo desta atividade é estimular você a produzir vários testes no seu aplicativo.
Um exemplo de código que poderia ser testado é o caso do “Deposit”:

testWidgets('My widget has a text "Deposit" ', (tester) async {
    await tester.pumpWidget(MaterialApp(
      home: BankInherited(
        child: Home(),
      ),
    ));
    final spentFinder = find.text('Deposit');
    expect(spentFinder, findsOneWidget);
  });COPIAR CÓDIGO
Existem diferentes tipos de Finder e diferentes Matchers, e existem tantos justamente para facilitar sua vida ao procurar Widgets diferenciados!
Caso tenha alguma dúvida, chame a gente no fórum!

@@10
Testando ações

[00:00] Nós acabamos de aprender a fazer os nossos testes de widget que são um pouco mais dependentes.
[00:09] O nosso tester, nosso robô automatizado, ele está apenas olhando para a tela e verificando se os elementos estão lá.

[00:16] Só que o nosso projeto não é uma tela estática que não se move, não muda, ela é uma tela de dinâmica, é um aplicativo, nós mudamos, nós temos ações para fazer nesse aplicativo.

[00:26] O ideal é que nós possamos testar ações no nosso aplicativo. "Como assim ações, Kako?" Quais são as ações do nosso projeto?". Vamos dar uma olhada?

[00:36] Nós temos botões funcionais, que é o deposit e o transfer. Se nós clicarmos em deposit, ele vai mudar o valor de algumas variáveis como o earned, o available balance ou o points.

[00:48] Só que para podermos visualizar essas alterações, nós temos que clicar no elemento que é o nosso status, por exemplo, e ele atualiza o valor de earned.

[00:59] Se nós clicarmos no elemento que é o header aqui em cima ele atualiza o valor, se nós clicarmos lá embaixo no elemento que corresponde aos pontos, ele atualiza esse valor e a tela muda.

[01:10] Então, isso são ações que nós temos que fazer. Nesse instante, nós estamos testando manualmente se essa ação é funcional, mas nós queremos programar o nosso robô, o nosso tester, para testar isso automaticamente sozinho, para ter certeza de que nada vai parar de funcionar.

[01:27] Então, vamos começar a fazer esses testes que envolvem ações do nosso tester? Vamos lá. Primeira coisa que temos que fazer, vamos voltar aqui para o nosso home_test.dart, embaixo do nosso teste widgets, no caso, está na linha 47 e eu vou começar um novo teste de widget.

[01:44] testWidgets, como nós já sabemos, precisamos de uma descrição, de um call back, o call back eu vou mudar o nome para tester e vou deixar o nosso call back na forma de chaves em vez de seta, ponto e vírgula para deixar tudo certo, apertei os botões "Ctrl + Alt + L" para deixar indentado.

[02:02] E a descrição nós precisamos descrever o que esse teste vai fazer. No caso desse instante, eu quero testar o botão deposit para verificar se quando eu aperto em deposit, o valor de earned sobe em 10 dinheiros, 10 pontos, 10 reais, 10 dólares, o que você quiser.

[02:18] Então, vamos colocar uma descrição aqui, 'When tap Deposit should upload earned in 10 points', acho que points não combina tanto upload earned in 10. Fica mais fácil de entender que quando nós apertamos em deposit o valor que está em earned vai subir em 10.

[02:52] Vamos lá, apertar os botões "Ctrl + Alt + L", para dar uma indentada e vamos começar o nosso teste. Assim como nós fizemos em todos os testes, ele tem que ser assíncrono, porque nós estamos colocando o nosso tester pump para desenhar na tela toda essa nossa screen home.

[03:13] Então, para facilitar a nossa vida, isso aqui nós já vimos, mas se você tiver com alguma dúvida, pode me acionar no fórum.

[03:20] Vou apertar os botões "Ctrl + C" no nosso tester.pumpWidget, da linha 34 a 38, para nós podermos printar a tela e vou colocar aqui o nosso novo teste de widgets, na linha 48.

[03:30] Temos o nosso desenho de tela e agora nós precisamos fazer algumas ações e como nós fazemos ações?

[03:40] Para fazer ações nós usamos uma nova função que também depende do tester, nós vamos pedir para o tester que é o nosso robô para ele fazer uma ação de tap.

[03:50] Existem vários tipos de ação. Tem tap, tem drag que é arrastar, tem o scroll until que é um que você vai rolando a tela até encontrar. Existem vários tipos de ações, mas nessa aula nós vamos ver apenas o tap.

[04:09] Então, inicialmente, eu vou falar "tester. eu quero que você dê um tap em alguma coisa". Que coisa? Bom, essa coisa nós precisamos encontrar, esse objeto, esse lugar onde tem uma ação.

[04:24] Eu vou aqui e falar, "Eu quero que você procure um widget que tem o valor de deposit". Então, qual vai ser o finder que nós temos que colocar aqui? O que nós estamos procurando?

[04:36] Nós estamos buscando o nosso botão de deposit e como é que nós podemos encontrá-lo? Tem várias formas, nós podemos usar o Box Card específico com uma key ou um tipo específico do widget que tenha esse ícone.

[04:50] Ou de um jeito mais simples, vamos usar o jeito mais simples, por enquanto, que é o find.text e o text que nós queremos só tem em um lugar é o deposit. "Se tivesse dois lugares escrito deposit, Kako?" Quer dizer que ele ia clicar, procurar esses dois lugares e clicar nos dois.

[05:10] Então, nós pedimos para o nosso tester clicar no nosso deposit. Vou adicionar aqui o await, para que nós possamos esperar o nosso robô, o nosso tester clicar em deposit antes de fazer a próxima ação.

[05:25] Então nosso tester clicou em deposit o que ele precisa fazer depois? Bom, ele vai precisar clicar no local correspondente que tem o earned e o valor de 10 que é o nosso status. Como que nós podemos fazer isso?

[05:41] Então, vamos fazer mais um tester await tester.tap para ele poder dar um tap, um clique e o mesmo tipo de find porque é mais fácil, no momento, para nós, find.text e vamos buscar em todo essa nossa tela, o nome earned, porque só existe no nosso widget clicado. Então, mais fácil de encontrar.

[06:08] Então, 'Earned', ele vai procurar o texto earned e vai clicar nele. Depois que ele clicar nele, ele vai procurar para ver se existe o valor de 10 no nosso novo widget.

[06:23] Não só 10, ele quer procurar, especificamente, aqui em cima. Para facilitar, eu vou até clicar no deposit e depois no status, que é onde tem o earned, por exemplo, e ele atualizou para cifrão 10, 10 dólares.

[06:38] Então, nós vamos buscar por essa informação aqui, cifrão 10 dólares. Vamos lá, nesse caso nós estamos esperando. Então, nós estamos esperando expect o quê? Nós esperando um finder que é o find.text.

[06:56] Qual que é esse text? É um text que vai ter barra para esquerda cifrão, que nós sabemos que é o cifrão mesmo '\$10.0'. É isso que ele está procurando e o matcher que nós vamos buscar é ter certeza de que só existe um widget.

[07:14] Então, findOneWidget. Recapitulando, vamos verificar se está tudo certo. Nós estamos criando o nosso teste de widget, temos a descrição, ele desenhou toda a tela, ele vem aqui e clicou no nosso botão que tem escrito deposit.

[07:32] Depois ele foi e clicou no lugar onde está escrito earned e depois ele esperou encontrar o texto $10.0 e encontrou apenas um widget. Vamos ver se esse teste funciona?

[07:45] Vou clicar no botão Run. Será que funciona? Não funcionou. Por que não funcionou? Bom, eu deixei esse erro falhar de proposito, porque tem uma coisa importante que nós esquecemos.

[08:02] Normalmente nós esquecemos quando não estamos muito atentos que é o seguinte. Quando nós estamos usando o pumpWidget, o que nós estamos fazendo? Nós estamos desenhando na tela.

[08:15] Então, essa simulação de tela está sendo desenhada. Uma vez que nós apertamos um tap, ele está mudando os valores, porque estamos clicando no botão deposit. Depois que nós clicamos, usamos o tap no earned.

[08:30] Nós estamos atualizando a nossa tela, emulador, porém nós precisamos avisar para o tester. Nós precisamos avisar para o teste que ele tem que reatualizar essa nossa tela, precisa recarregar essa tela.

[08:42] Não é só porque a função que está dentro do nosso widget clicável, altera automaticamente o valor com Set State que o tester também vai mudar.

[08:54] Toda vez que a sua tela mudar de forma, você precisa avisar para o tester que ele tem que dar um novo pump. O que é um pump, é como se ele estivesse fazendo os micro serviços, os pequenos serviços que fazem com que a tela mude.

[09:11] E existem vários serviços. Então, nós vamos ter que vir aqui, logo depois do nosso tap, no earned e pedir para o nosso tester dar um novo pump na tela e esperar.

[09:24] Então, nós podemos vir aqui e usar o await tester, existem vários tipos de pump, tem pump puro, tem o pumpWidget, tem o pumpAndSettle, o pumpBenchmark, o pumpFrames.

[09:37] São vários tipos de pump que são como se fosse esperar micro serviços, micro atividades que o nosso projeto faz quando nós estamos atualizando a tela e ele espera esses serviços terminarem.

[09:50] No caso nós vamos usar o pumpAndSettle, porque ele vai esperar todos os micro processos acabarem para depois continuar. Se nós usarmos só o pump, ele vai esperar um micro serviço terminar e continuar e assim vai.

[10:05] Então, vamos usar um pumpAndSettle. Vou usar o pumpAndSettle e agora sim o nosso tester vai clicar em deposit, depois ele vai clicar em earned, depois ele vai esperar todos os micro processos que alteram a tela acabarem e ele vai procurar pelo valor de 10 dólares. Vamos ver?

[10:26] Vou aqui e clicar para rodar o nosso teste. Agora ele deve passar. Passou. Olha que legal. Bacana.

[10:36] Acabamos de criar uma ação no nosso tester, ensinar o nosso robô a fazer ações, esperar o resultado dessas ações.

[10:45] Nós não precisamos testar só o deposit, dá para testar o transfer e vários outros botões. Nós não precisamos testar só o earned, podemos testar o que tem o spent, o available balance ou o points. Fica ao seu critério.

[10:59] Mas a princípio aprendemos a fazer um novo teste. Eu te desafio a fazer o teste para todas as áreas de ações nesse nosso projeto aqui.

[11:09] Vejo você daqui a pouco.

@@11
Para saber mais: outras ações

Vimos que podemos simular ações no nosso teste, mas tap() não é a única ação disponível para o nosso tester. Para ajudar você a explorar novas ações, separei algumas outras ações que você pode simular, tais como arrastar, inserir texto ou até scrollar a tela.
Bons estudos!

https://docs.flutter.dev/cookbook/testing/widget/tap-drag

https://docs.flutter.dev/cookbook/testing/widget/scrolling

@@12
O que aprendemos?

Chegou a hora de sentar e revisar o que vimos! Nessa aula, metemos a mão no código e construímos testes de widgets, exploramos vários Finders, aprendemos criar um Matcher e ainda vimos a diferença entre teste automatizado e teste manual:
Teste Automatizado Vs Teste Manual:
Comparamos a eficiência de um teste Manual (que é feito pelo desenvolvedor, ao alterar o código e verificar se de fato o projeto seguiu o desejado ) e o teste automatizado (que é feito pelo framework e é extremamente veloz e eficiente).

Testes de Widgets:
Aprendemos que testes de Widgets requerem um pouco mais de cuidado, pois precisam ser renderizados em uma tela emulada para a verificação de elementos desenhados, além de possuir mais possibilidades de dependências entre outros widgets.

pump():
Método capaz de esperar pelos microprocessos necessários para buildar/renderizar/desenhar na tela os elementos dos Widgets. Lembre-se de que existem diversos tipos de pump() que podem se adaptar melhor a diversos testes e Widgets específicos.

Finders:
Nome dado aos métodos capazes de buscar, na tela renderizada, os Widgets desejados, utilizando diversas abordagens de procura, como tipo de Widget, qual sua chave, entre outros.

Matcher:
Compreendemos que, ao encontrar um Widget na tela, precisamos ter algum grau de controle quanto a ele. Assim, podemos verificar quantos Widgets existem na tela e quais os parâmetros que confirmam que de fato aquele Widget é o procurado. Os Matchers são responsáveis por essa comparação.

Testar ações no código:
Quando testamos nosso aplicativos, nos deparamos com ações de interação com botões, caixas de texto, scrollables entre outros. As ações são instruções que damos ao nosso tester para interagir com certos Widgets a fim de verificar sua usabilidade.

Finalizamos a Aula 3!

Já passamos da metade! E aí, o que está achando? Conta pra gente lá no fórum ou no Discord da Alura!

Vejo você na próxima aula!

#### 05/01/2024

@04-Aplicando Dublês

@@01
Projeto da aula anterior
PRÓXIMA ATIVIDADE

Caso queira, você pode baixar o projeto do curso no ponto em que paramos na aula anterior.

https://github.com/alura-cursos/alura_flutter_curso_7/archive/refs/heads/Aula_3.zip

@@02
Aplicando Dublês

[00:00] Então, quer dizer agora que nós já sabemos fazer os nosso testes de widget e os nosso testes de unidade e está tudo dar certo, então, já estamos muito bem, não é?
[00:15] Pois é, não estamos tão bem assim, porque nem tudo está dando certo. Inclusive, todos os testes que nós fizemos uma coisinha não estava muito certa.

[00:25] Qualquer teste que nós formos olhar agora com calma, vocês vão ver a mesma mensagem. Vou mostrar para vocês qual é o problema que está dando e que eu não falei para vocês até agora.

[00:35] Vou rodar o nosso último teste que foi o teste do deposit, para vocês terem certeza de que esse erro está em todos os lugares, mas vocês podem fazer com outros testes também.

[00:46] Se eu rodar aqui, vocês vão ver que o teste passa, porém se nós dermos uma lida no teste, existe uma mensagem escrita, "Não foi possível se conectar com a API: 400".

[00:58] O que é isso aqui? Opa, espera aí, como assim? Como não foi possível se conectar com a API: 400? O que está acontecendo?

[01:05] Vamos dar uma olhada aqui no nosso HTTP, como nós fazemos essa implementação nesse projeto, para nós entendermos que mensagem é essa. Vamos aqui no nosso projeto, a esquerda, e vamos acessar data e vamos acessar o documento bank_http.dart.

[01:22] Nesse nosso documento bank_http.dart, nós temos a conexão com o site economia.awesomeapi que nos diz qual é o valor em relação ao dólar e o real naquele instante.

[01:36] Então, essa é a nossa API, nós estamos pegando informação em relação ao dólar e real, nós podemos ver essa informação no nosso aplicativo, à direita e em cima, e esse valor muda de acordo como valor do dólar e do real no momento.

[01:50] Nós estamos pegando essa informação em tempo real. Então, se nós tivermos uma conectividade, uma conexão boa, nós vamos ter uma resposta de 200 e ele manda essa informação para nós.

[02:03] Caso tenha algum problema, caso o statusCode, a conexão não seja 200, significa que não foi possível se conectar com a API, ele vai mandar essa informação para nós no nosso console e vai dizer qual é o statusCode, 400, no caso.

[02:20] Então, isso está acontecendo em todos os nosso testes. Por que isso está acontecendo? Bom, isso está acontecendo, porque quando nós estamos testando alguma coisa, quando nós estamos fazendo testes no Flutter, ele não vai testar conexão de fora, conexões externas.

[02:37] "Kako, por que não testa essas conexões externas?". Vamos supor o seguinte, vamos imaginar que o nosso teste testa, inclusive, as conexões com essa nossa API do dólar e por um instante de segundo, em um momento no dia, esse site ficar fora do ar, por um segundo, as vezes um pouco mais, mas esse site está fora do ar.

[03:00] E nesse incrível momento que você está testando a sua aplicação e o site está fora do ar, o teste não passa e se o teste não passa, bom, você vai achar que tem algo errado. Só que não é culpa do seu projeto, não é culpa do Flutter, é só uma conexão com algo externo que está fora do ar, ou seja, nós criamos um teste não confiável quando nós adicionamos uma API a esse teste.

[03:27] Nós chamamos, inclusive, de Fake test, um teste não-confiável. Ele pode estar passando agora e daqui a dois segundos não passar, porque o site sob o qual não temos controle nenhum, saiu do ar.

[03:39] Então, não é legal nós termos um teste que testa toda a nossa aplicação e não depende só de nós, ou seja, nós temos um teste não muito confiável. Como é que nós podemos lidar com isso aqui?

[03:51] Para entender como lidar com a conexão API, ou conexões de fora que não dependem só do nosso projeto, nós usamos um termo chamado de dublês. Existem vários tipos de dublê. Eu vou mostrar para vocês como eles funcionam, mais ou menos.

[04:06] Vamos imaginar o seguinte, imagine que o nosso projeto é um quebra-cabeça. Existem vários pedaços do nosso quebra-cabeça. Como vocês podem ver agora, nós temos um quebra-cabeça com peças cinzas, uma peça verde e algumas peças amarelas.

[04:21] As peças cinzas são peças que nós não temos muito interesse, a peça amarela é a peça, o objeto, o local onde nós estamos fazendo o nosso teste e as peças amarelas são as peças que se encaixam perfeitamente na nossa peça verde, ou seja, são as nossas dependências daquele objeto ou widget.

[04:42] Ou seja, se eu quiser testar a peça verde, eu vou ter de levar em consideração as peças amarelas, só que olha só, as peças amarelas estão conectas em algumas peças cinzas e fica difícil de testar peça verde se nós não acabarmos testando tudo.

[04:55] Então, como é que nós podemos resolver esse problema? Para resolver esse problema, nós usamos alguns dublês. Então, agora vocês devem estar vendo a imagem, no canto esquerdo, um pouco atualizada, onde nós temos a peça verde no centro e algumas peças amarelas que são apenas resquícios da antigas amarelas.

[05:13] Elas são só encaixes para encaixar na nossa peça verde, são objetos que estão simulando ações ou algumas dependências apenas para a peça verde poder funcionar sem problemas.

[05:25] Não são peças verdadeiras que funcionam no nosso projeto. São apenas peças de encaixes para nós podemos testar sem ter problemas.

[05:32] Esses são os nosso dublês e nós precisamos de dublês de teste toda vez que tivermos algum teste com uma dependência que não depende muito da nós que é o caso da API.

[05:42] Então, como é que nós fazemos para implementar isso no Flutter? Existem vários tipos de dublê. Existe mock, existe stub, existe spy, existe dummy, existe fake.

[05:55] Nesse curso, especificamente, nós vamos ver o mock e os stubs, mas uma coisa de cada vez.

[06:01] Para nós começarmos com pé direito nesses nossos dublês, já vou mostrar para vocês como é que nós implementamos um mock no nosso projeto. Vem comigo, vamos ali no nosso site do Flutter.

[06:14] Estamos aqui no site do Flutter que vocês já conhecem bastante, flutter.dev. Aqui à direita em cima, eu vou clicar no nosso menu e vou clicar no get started e nós vamos para a nossa famosa documentação do Flutter.

[06:29] Aqui à esquerda embaixo do nosso menu, eu vou procurar por texting. Então, vamos descer aqui e existe Texting & Debugging, vou abrir e eu vou buscar pelo tópico de texting.

[06:42] Na página nós temos uma documentação extensa e muito bem-feita sobre testes. Vocês podem vir aqui e olhar bastante coisa sobre teste de unidade, teste de widget, mais especificamente nós estamos procurando mock, dependências com mock e aqui embaixo, descendo um pouco, no tópico de Recipes.

[06:58] Vocês vão ver que tem um tópico escrito Mock dependencies using Mockito. Vamos clicar e agora nós estamos na nossa documentação. Se vocês quiserem parar um pouco, dar uma lida com calma para entender como é que isso tudo funciona, vocês podem, mas vocês também podem usar só essa aula para seguir no nosso curso.

[07:15] Nós temos aqui várias coisas de como funciona para adicionar um mock no nosso Flutter. Eu estou aqui só para mostrar como é que a documentação funciona em relação ao Mockito.

[07:27] Mockito é um pacote que nós podemos usar para adicionar a nossa funcionalidade no nosso projeto, eu vou clicar nesse link escrito Mockito package que vai nos levar para o Pubdev do Mockito que é o pacote que nos ajuda a adicionar um mock, um dublê no nosso projeto.

[07:47] Existem muitas coisas para você ler aqui. Se você quiser ler com calma, mas agora eu vou só ensinar para vocês como nós criamos um mock, um dublê da nossa API que já está no nosso projeto, de um jeito bem mais simples, mas vocês podem vir aqui para entender tudo.

[08:03] Ele está explicando para nós aqui que nós temos que colocar um generate mock no nosso arquivo que precisa ter um dublê. Então, qual é o nosso arquivo que precisa ter um dublê? Vamos voltar no nosso projeto. Aqui no nosso projeto, nós temos o BankHttp e ele precisa de um dublê, porque nós não queremos que o nosso teste fique dependendo dele toda hora.

[08:23] Então, eu vou vir aqui e vou escrever @GenerateMocks e ele precisa da classe, a classe que nós estamos buscando é o BankHttp. Vou colocar na linha cinco BankHttp e agora nós já acionamos uma forma de criar um novo mock, mas não é só isso, nós temos que dizer para o Flutter, "cria um dublê dessa classe para mim, por favor", "Beleza, vamos criar sim, mas isso nós vamos ver daqui a pouco".

@@03
Gerando um Mock

[00:00] Então, nós estamos criando, um mock, um dublê, e para isso nós usamos, escrevemos esse comando diferenciado @GenerateMocks. Mas isso aqui não é o suficiente para gerarmos o nosso dublê do BankHttp.
[00:19] Para nós gerarmos o nosso dublê, vamos dar uma olhadinha na documentação, só para não nos perdermos. A documentação está no pub.dev/packages/mockito. Nós estamos usando o pacote do Mockito que é um pacote que facilita a criação de dublês, especificamente, mocks para o Flutter.

[00:42] Escrevemos o @GenerateMocks e colocamos o nosso tipo de classe que queremos gerar no nosso mock, no caso, é o nosso BankHttp.

[00:56] Nós precisamos fazer umas coisas, como colocar no nosso pubspec.yaml o pacote do Mockito e um outro pacote que a documentação está explicando para nós aqui que é o build_runner.

[01:06] Eu não vou ler a documentação para vocês. Como eu já sei, exatamente, o que a temos que fazer, eu vou fazer passo-a-passo para nós. Caso vocês queiram, você pode parar o vídeo um pouco e dar uma lida em toda essa documentação aqui como já vimos lá atrás como nós lidamos com pacotes.

[01:24] Então deixar a documentação para caso vocês queiram olhar e vou direto, agora, para o nosso projeto.

[01:30] Então, voltando aqui para o nosso projeto, deixa eu abaixar a aba. Voltando aqui para o nosso projeto, o que vamos precisar fazer primeiramente? Vamos lá na aba pubspec.yaml e no pubspec.yaml nós vamos procurar o local onde podemos adicionar uma dependência.

[01:46] Então, temos na linha 29 dependencies e embaixo do http, na linha 37, que é um pacote que já veio no nosso projeto. Eu vou colocar o pacote do mockito. O mockito que estamos usando nessa versão do curso é o 5.3.0, e eu aconselho fortemente que você use a mesma versão.

[02:07] Mais uma coisa que nós precisamos adicionar, é um outro pacote, mas é um pacote levemente diferente, é um pacote de desenvolvimento, ou seja, é um pacote que ele vai estar habilitado para os desenvolvedores.

[02:18] Para adicionarmos um pacote de desenvolvimento, temos que vir aqui um pouco mais embaixo na aba de dev dependencies. Um pouco mais para baixo, logo depois do flutter_lints, na linha 49, nós vamos adicionar um novo pacote e isso está na documentação.

[02:33] E nós vamos adicionar aqui o build_runner, o build_runner que nós estamos usando nessa versão é 2.2.0. Mesmo esquema, sugiro que você use a mesma versão.

[02:46] Então, nós já colocamos aqui os nossos pacotes que vamos precisar. Vou dar um pub get para ele poder atualizar o nosso projeto e uma vez rodado, já está finished. Vamos continuar o nosso pub expect já está finalizado.

[03:04] O nosso BankHttp, o nosso @GenerateMocks não sabe que código é esse. Então, nós precisamos importar um pacote para ele começar a entender que código é esse.

[03:17] Então, eu vou aqui e clicar no próprio @GenerateMocks, apertar os botões "Alt + Enter" e ele vai dizer para mim, pode importar o pacote mockito/notations e esse código vai ser inteligível.

[03:29] Agora já importamos e o @GenerateMocks já está funcional. Só isso que a precisamos? Não, agora vamos usar o pacote build_runner que ele basicamente cria um código em dart para nós, automaticamente. Ele vai criar esse dublê, vai codar para nós. Bem bacana.

[03:48] Então, vou aqui, para podermos utilizar esse build runner, no terminal aqui embaixo. Então, embaixo, aqui no nosso Android Studio vocês vão ver que tem um terminal e no próprio terminal conseguimos ver que estamos no Alubank.

[04:06] Então, eu vou aqui e digitar o código para rodar a criação desse nosso mock. Então, vamos lá. O código está na nossa documentação.

[04:19] O código é flutter pub run build_runner build, pronto, só isso e ele vai começar a criar o nosso novo arquivo de mocks. Esperamos um pouquinho, ele começa a fazer várias ações e no final ele vai falar assim, Succeeded depois de alguns segundo com um output, esse output significa a nossa saída, o nosso novo arquivo.

[04:57] Normalmente o Android Studio demora um pouco para criar. Vocês viram agora que ele apareceu. Normalmente o Android Studio demora um pouco para mostrar que esse arquivo foi criado. Às vezes o Android Studio dá algum problema, então se deu sucesso e ele não apareceu, pode reiniciar o seu Android Studio, que vai aparecer, ou você pode verificar nas pastas físicas mesmo e ver se BankHttp.mocks.dart está criado.

[05:26] Vamos abri-lo para ver o que foi criado? Não se assustem, isso aqui nós não precisamos entender 100% do que está acontecendo, mas é importante que vocês entendam que esse aqui é o nosso dublê do nosso BankHttp.

[05:41] Então, ele basicamente está pegando tudo que o nosso BankHttp faz e criando um fingimento, um dublê, um mock de tudo o que fazemos.

[05:51] Pronto, temos aqui agora o nosso BankHttp mockado. Que legal. Só para termos certeza de que está funcionando, nós podemos testar com no nosso próprio arquivo do BankHttp. Vou aqui, linha 21, depois que acaba o BankHttp, eu vou criar uma void main só para vermos que o nosso mock http existe.

[06:18] Então, criei uma void main aqui e eu vou criar um final vou chamar de httpMockado e ele vai ser equivalente a um Mock, aparecem vários tipos de mock aqui, MockSpec, MockClient e apareceu agora o nosso MockBankHttp.

[06:37] Então, vou em MockBankHttp. Em vez de usar o BankHttp quando nós precisamos nos testes, vamos usar o MockBankHttp, já existe o nosso hpptMockado, "dublezado". "Dublezado" é uma palavra estranha.

[06:57] Nós já sabemos que existe, está tudo funcionando. O que nós precisamos fazer agora? Primeira coisa, eu já vou deletar esse void main, na linha 23, que eu usei só para mostrar para vocês que o MockBankHttp existe e é uma classe, está usável, está aqui no lado esquerdo.

[07:11] Vou fechar. E o que nós precisamos? Nós precisamos entender onde que o nosso BankHttp está sendo usado.

[07:19] Então, vamos aqui, bank_http.dart, ele foi criado aqui, mas onde que nós o usamos? Está sendo usado lá em cima. Se nós olharmos, no nosso projeto, em cima, à direita, nós temos o nosso dólar para reais.

[07:37] Então, vamos no nosso "components > sections" e procurar pelo header.dart. Vamos acessar header.dart e um dos elementos dentro dele, vamos procurar aqui descendo um pouco.

[07:56] Aqui, a partir da linha 61 nós temos um FutureBuilder que está procurando o BankHttp e está usando o método dólar para real que é esse método da nossa classe, linha 9, dolarToReal. Esse método que está fazendo toda a conexão http.

[08:17] Então, é lá no header que nós estamos usando o BankHttp para poder acessar essa informação toda. É um FutureBuilder, então, caso essa informação não exista, ele vai deixar um círculo de progresso CircularProgressIndicator. Caso existe ele vai vir aqui embaixo e printar na nossa coluna os valores que é o que nós estamos vendo na nossa tela do nosso projeto.

[08:38] Poxa, legal, é aqui que está sendo usado o nosso BankHttp. Então, no caso, quando eu fizer o nosso teste, eu posso, em vez de usar o BankHttp, usar o MockBankHttp. Seria isso? Não sei, vamos ver isso daqui a pouco.

@@04
Aplicando o Mock

[00:00] Então, nós entendemos que nosso BankHttp está sendo usado no header e nós já criamos o nosso dublê. Só que nós não podemos, simplesmente, vir aqui e adicionar o nosso dublê no nosso header. "Por quê, Kako?".
[00:16] Porque aqui é onde está o nosso projeto verdadeiro, nós não queremos um dublê no projeto verdadeiro. Nós queremos um dublê apenas no nosso teste.

[00:25] Então, o dublê não é para estar dentro do projeto, é para estar dentro do teste e como nós podemos fazer para isso funcionar?

[00:31] Vamos voltar no nosso teste? Então, eu vou aqui nosso home_test.dart e o nosso home_test.dart, se nós dermos uma olhada, a primeira coisa que nós fazemos no nosso testes de widget é buildar, desenhar, a tela e desenhar essa tela nós precisamos do home.

[00:47] Vamos dar uma olhada rápida no home só para nós recapitularmos. O nosso home, quando nós abrimos aqui ele é um Stateless widget e tem quatro children. Um desses children é quem? É o Header e dentro do Header nós já sabemos, tem o nosso BankHttp.

[01:03] Ok, então, nós sabemos que o home é o pai do nosso header e o header é onde está sendo usado o nosso BankHttp. Como é que nós fazemos para avisar no nosso teste, deixa eu vir aqui para o nosso home_test.dart, o que nós fazemos aqui?

[01:21] Teste é o seguinte, eu quero Home que você avise, eu vou até deixar aqui um comentário (/*Avisar que isso é um teste lá para o header*/). Como é que nós fazemos para o home que é o nosso widget que estamos usando no teste.

[01:45] Como é que nós fazemos para o home avisar para o header que isso aqui é um teste? Nós criamos algumas dependências e é isso que nós vamos fazer agora.

[01:55] Vamos lá, eu vou deixar esse comentário aqui assim, por enquanto, para nós não esquecermos e vamos voltar no header.

[02:02] Aqui no nosso header, na linha 62, nós estamos usando o BankHttp e eu não quero mais usar esse BankHttp aqui nesse instante. O que eu quero? Eu quero receber a informação. Se isso aqui vai ser o BankHttp ou se esse aqui vai ser o dublê.

[02:19] Como é que nós fazemos isso? Vamos subir lá para o início onde nós construímos o nosso StatefulWidget, linha 5, e quero criar um final. Qual é o tipo desse final?

[02:33] Esse final é Future<String>. "Kako, por que é um future string esse final que você criou?". Já vou explicar. Vou nomear como API. Por que é um Future String? Vamos dar uma olhada lá no nosso BankHttp.

[02:48] O BankHttp, nós estamos usando um método chamado dolarToReal que ele é o quê? Future String, ele está enviando para nós uma String que demora um tempo, porque é uma conexão API.

[03:02] Então, vamos voltar lá no nosso header e nós estamos esperando essa API. Agora que nós temos esse final, nós precisamos avisar toda vez que nós instanciarmos um header, ele precisa receber essa API.

[03:15] Então, eu vou no nosso construtor, linha 6, e vou falar required this.api. Então, toda a vez que nós formos iniciar o nosso header, ele vai receber esse Future API.

[03:30] Só isso? Não, nós precisamos alterar aqui embaixo. Deixa eu descer um pouco, na nossa linha 63, no nosso Future, e em vez de usar aqui o BankHttp, eu vou falar precisamos da API this.api. No caso é widget.api. Todo mundo erra, eventualmente, acontece.

[03:55] widget.api, pronto, agora nós estamos esperando a nossa API e nós podemos escolher entre ser o mock e ser verdadeiro no nosso header

[04:05] Então, quem é que está com erro agora? Nosso home. Lá no home, quando nós instanciamos o header, ele pede por essa API.

[04:14] Ele está precisando de uma API que é required. Nós podemos vir aqui e falar que é o BankHttp ou MockBankHttp? Não, é aqui que nós vamos alterar. Nós temos que enviar essa informação para o nosso home, que precisa receber essa informação.

[04:29] Então, nós temos que fazer exatamente a mesma coisa no home. Aqui na linha 8 do nosso Home, que é StatelessWidget dessa vez. Eu vou falar home você precisa de um final e esse final vai ser um Future<String> e o nome dele vai ser api também.

[04:51] E como nós fizemos agora a pouco no header, nós precisamos que você receba esse API required this.api e coloque um valor nessa API para nós.

[05:02] E o que nós precisamos agora? Falar que o nosso header vai receber a informação do nosso home. Então, o nosso API agora precisa de um this.api.

[05:13] "Mas, Kako, está vermelho na linha 19, tem um problema". Esse é um problema padrão. Nós falamos anteriormente, no nosso projeto, que isso seria constante, e não é mais constante.

[05:26] Você está recebendo uma informação variável. Então vou tirar o const da linha 18 e ele vai parar de brigar conosco e todos agora vão ficar pedindo para ser constantes.

[05:37] Isso é uma boa prática que o próprio Android Studio faz para nós, não tem problema, mas tranquilo, apertei os botões "Ctrl + Alt + L", só para indentar e o nosso header está recebendo a informação da API do nosso home.

[05:51] Quem é que cria o home? Vamos lá no main? Agora o main está com erro, linha 19, porque o Home precisa receber API.

[05:58] Nós estamos trazendo de cima mesmo essa decisão se vai ser mock ou não. Estamos criando muita dependência aqui, inclusive.

[06:07] A primeira coisa que eu vou fazer é tirar esse const daqui que nós temos na nossa linha 19, antes do Home e agora o nosso Home está pedindo por uma API do tipo Future<String>. Qual vai ser essa API? No caso aqui, na nossa main, eu estou colocando o BankHttp verdadeiro.

[06:31] BankHttp().dolarToReal() que é um Future String. Agora sim esse BankHttp().dolarToReal() vai descer do home para o header, linha 18, do header vai descer até o nosso future builder na linha 63 e vai ser usado.

[06:55] No final das contas não mudamos nada, mas e o nosso teste? Vamos conferir nosso teste? Como é que nós fazemos essa alteração no nosso teste? Deixa eu abrir home_test.dart, aqui que nós acabamos de deixar um comentário na linha 50, o nosso teste de widget de deposit.

[07:18] O home agora está com erro. Ele está falando, "Nós precisamos de uma API". Todos os homes que nós já escrevermos até agora vão ficar falando, "Nós precisamos de uma API" e que API é essa?

[07:27] Vamos vir aqui, (api) e vou colocar o nosso (api: MockBankHttp().dolarToReal()). Agora sim ele está recebendo o nosso objeto dublê, o nosso objeto mockado e ele não vai ter tanto erro em relação a comunicação http ou a nossa API. Que bacana.

[07:52] Então, antes da nós terminarmos essa aula, o que nós precisamos fazer? Os nossos testes todos estão em vermelho, porque o home precisa de uma API. No caso, o nosso mock.

[08:04] Então, vamos copiar na linha 51 uma api: MockBankHttp().dolarToReal() e vou colocar em todos os nossos outros testes de widget.

[08:17] Aqui dentro do nosso teste de BoxCard, dentro do nosso teste de AccountStatus, dentro do nosso teste de LinearProgresseIndicator e dentro do nosso teste do texto Spent. Coloquei em todos eles. Que legal.

[08:31] Será que agora, então, os nosso testes passam? Vamos testar? Vou aperar o botão Run, na linha 8, e vamos ver se os nossos testes passam.

[08:40] Pela minha cara deu para ver que não ia passar. Pois é, os testes não vão passar, porque tem mais uma coisa crucial que nós precisamos fazer quando estamos mockando testes e essa crucial se chama stubs e nós vamos ver a seguir.

@@05
Criando Stubs

[00:00] Nós acabamos de fazer o nosso mock e implementamos ele nos nossos testes, porém todos os testes falharam. Por que isso aconteceu? Vamos dar uma olhada no nosso console? Que ele explica um pouco do porquê que os testes falharam.
[00:18] Vamos dar uma olhada aqui, os nossos testes dizem, No stub was found, ele está dizendo que não existe um stub para o método que nó chamamos. Qual método? dolarToReal. O que isso significa? Vamos conferir lá no nosso dolarToReal.

[00:35] Então, vamos voltar no nosso documento bank_http.dart e aqui no nosso método dolarToReal, ele faz várias coisas para chamar o http, conectar e ele busca um valor. Quando ele encontra esse valor, ele retorna um valor que é uma string, no caso essa string demora um pouco, por isso Future<String>.

[00:56] Então, ele retorna essa string. Opa, então, ele retorna um valor, precisamos desse valor para quê? Esse valor é necessário para construir na nossa tela a relação entre o dólar e o real.

[01:09] Aqui a direita em cima, no nosso projeto, vocês conseguem ver que está aqui, R$ 5,2192, que é o valor que foi pego pela nossa API.

[01:18] Então, ele retorna um valor e esse valor é necessário para construir a tela. Então, no nosso teste a falta desse valor fez falta, esse valor fez falta.

[01:29] Então, nós precisamos dizer que quando usarmos esse método do dolarToReal, vamos retornar um valor.

[01:39] Então, vou criar aqui com vocês para nós entendermos com facilidade o que é o stub. Vou criar um novo teste, vai ser um teste de widget, porque nós vamos construir essa nossa tela, então, vai ser um teste que nós vamos testar o nosso mock

[01:54] Então, vai ser 'Testing MockHttp dolarToReal', linha 61, uma descrição simples. Vou mudar o nome do nosso tester para tester padrão. Vou tirar o nosso arrow type para uma chaves, linha 62.

[02:17] Vamos ver aqui, deixar ele assíncrono, coisa que nós já fizemos aqui e já entendemos como funciona. Um ponto e vírgula, linha 62.

[02:26] Normalmente a primeira coisa que nós fazemos é o quê? Nós chamamos um await tester.pumpWidget para construir a nossa tela.

[02:34] Antes disso nós vamos criar um stub. Então, vou explicar essa construção do stub e eu mostro para vocês exatamente o que é o stub.

[02:43] Primeiramente, para construir um stub, nós vamos precisar de uma nova função. Função when, a função when fica de olho em um método que vai ser chamado durante o nosso teste. Que método que nós estamos buscando? Esse método é o nosso MockBankHttp().dolarToReal().

[03:04] Quando esse método for ativado, for usado no nosso teste, eu preciso enviar e retornar alguma coisa. Como é que eu digo que eu preciso retornar alguma coisa?

[03:16] Para isso nós vamos usar mais uma função que é a thenAnswer e para isso é só você apertar no ponto e vai abrir para você algumas opções de toString e temos aqui thenAnswer e thenReturn, thenThrow.

[03:31] Enfim, tem vários tipos e em alguns momentos nós usamos o thenReturn, em outros os thenAnswer. Para o nosso caso ser do tipo Future e do tipo assíncrono, o ideal é usar o thenAnswer que é o que nós vamos usar agora.

[03:44] Mas isso também está muito bem explicado na documentação do Mockito, só vocês darem uma olhada e se tiverem dúvida pode falar comigo no fórum.

[03:53] Então, thenAnswer e ele vai falar o seguinte, uma vez que nós usamos o nosso método dolarToReal, ele vai nos enviar um valor.

[04:05] Então, para facilitar a nossa a vida eu vou deletar esse nome realInvocation, isso aqui é um call back, realInvocation vai ser só um nome privado, com um underline, vai ser do tipo assíncrono, porque vai demorar para esse valor vir e ele vai nos dar um valor simples de '5'.

[04:29] O que significa? Significa que no nosso teste, quando o MockHttp que é o nosso dublê que não faz nada, de fato, ele for chamado, o nosso teste vai dizer, "Quando esse método for chamado você vai responder com 5". O que significa que no nosso teste o valor a ser lido pelo robô seria 5 aqui em cima do dolarToReal.

[04:55] Isso aqui é um stub que é basicamente um dublê que recebe uma resposta. Então, um dublê está ali aparecendo para se encaixar na dependência e a resposta desse dublê é dada pelo stub, isso é um stub.

[05:12] Então, agora nós vamos continuar o nosso teste de widgets. Qual é o próximo passo padrão que fazemos? Nós fazemos o pumpWidget para nós construirmos a nossa tela.

[05:23] Então, eu vou aqui da linha 51 a 55, copiar esse texto inteiro do pumpWidget, que nós fizemos várias vezes. Então, eu não quero perder muito tempo. Vou vir aqui no pumpWidget.

[05:36] Agora o que nós precisamos fazer é verificar se, de fato, durante todo esse pumpWidget, esse teste, se o nosso MockBankHttp().dolarToReal()foi chamado mesmo.

[05:50] Para verificar é muito simples, tem uma função chamada verify que vamos verificar qual é a função que foi chamada. Mesma coisa MockBankHttp().dolarToReal() e ele está verificando se ela foi chamada.

[06:06] Porém, nós precisamos comparar, ter um matcher ali. Quantas vezes essa função foi chamada? E para isso podemos vir aqui e apertar o ponto e ele vai abrir para mais algumas opções e a opção que nós vamos usar é a called.

[06:22] E ele vai perguntar, ele vai comparar quantas vezes essa função foi chamada. Então, vai perguntar no nosso matcher, "Quantas vezes foi chamada essa função?"

[06:31] No nosso caso essa função foi chamada apenas uma vez, em todo o nosso projeto nós só a usamos em um lugar. Então só vai ser chamada uma vez. "Terminamos, professor".

[06:44] Não, não terminamos. Tem um detalhe importante que nós esquecemos. Eu deixei esse erro de proposito para nós não perdemos o costume, o hábito de ficar sempre de olho no dart.

[06:56] O que está acontecendo no nosso teste? Olha só, nós usamos o when e no when nós criamos uma instancia aqui do MockBankHttp. No nosso tester.pumpWidget, nós criamos de novo esse MockBankHttp e no verify nós criamos, de novo, esse nosso MockBankHttp.

[07:19] Cada um desses três é uma instancia. Então funciona como se fossem indivíduos diferentes. O when nunca vai conseguir encontrar o mesmo objeto, o mesmo indivíduo que foi criado no nosso pumpWidget ou foi verificado, não vai conseguir verificar o mesmo indivíduo.

[07:42] Eles são iguais? São a mesma classe, mas não são os mesmos indivíduos. Como é que nós podemos fazer para resolver isso? Para isso nós podemos criar uma instancia única.

[07:52] Eu subir e vou no nosso void main. Vou criar, linha 11, um final MockBankHttp e vou chamá-lo de httpMock, e ele vai ser igual a nosso instancia única MockHttpBank.

[08:12] Então, tudo o que eu fiz foi instanciar em um único indivíduo chamado httpMock e agora eu posso ir lá embaixo, de volta ao nosso teste, e em vez de usar MockBankHttp, linha 65, em todos eles, eu vou, simplesmente, chamar o nosso indivíduo que é o httpMock que nós nomeamos lá em cima.

[08:33] Então, eu vou mudar para todo mundo e assim todo mundo vai analisar e verificar e criando o mesmo indivíduo.

[08:44] Agora nós podemos verificar se esse teste está passando. Vamos ver se passa? Vou clicar no número da linha 64 e esperar.

[08:54] Passou, quer dizer, então, que o nosso objeto foi criado, foi verificado e não tivemos o problema da API.

[09:05] Então, parabéns, você conseguiu entender como está funcionando, só que os outros testes ainda estão com o MockBankHttp, eles não estão com os stubs.

[09:15] Então, eu sugiro, eu desafio, na verdade, vocês a virem aqui nos outros testes de widget e começarem a colocar os stubs em cada um deles e usar o mesmo indivíduo para todos eles que seria o nosso httpMock.

[09:30] E assim todos os testes vão passar totalmente mockados com dublês sem problema nenhum de comunicação com a API. Que bom que vocês gostaram. Vejo vocês daqui a pouco. Tchau.

@@06
Faça como eu fiz: Mockito - eu escolho você!
PRÓXIMA ATIVIDADE

Tá na hora de você contratar seu Dublê! Brincadeiras à parte, é importante agora praticar as implementações que fizemos ao longo desta aula.
Vamos aplicar o que aprendemos para produzir um Mock:

Adicionar o pacote do mockito (5.3.0) e o build_runner (2.2.0);
Usar o código de gerar Mock na classe que deseja um dublê;
Rodar o código do build_runner no terminal e esperar o arquivo .mock ser criado;
Alterar as dependências para poder relatar ao teste se há um dublê ou não;
Adicionar um Stub caso seu método mockado tenha retorno (desafio que eu mencionei no vídeo!).
Partiu?

Nessa atividade, a intenção é que você consiga produzir um Mock por conta própria.
Assim, caso queira ver a implementação, acesse o repositório do projeto no Github.

Ao gerar um Mock com o build_runner você deve ter cuidado e calma, pois nem sempre o Android Studio acompanha quando o arquivo é criado, fique de olho na pasta para garantir que seu código foi gerado.
Sobre o desafio com os stubs, você pode consultar a explicação disso no próximo vídeo!

Dúvida? Chame a gente no fórum!

https://github.com/alura-cursos/alura_flutter_curso_7/archive/refs/heads/Aula_5.zip

@@07
Finalizando os testes

[00:00] Na última aula eu joguei um desafio para vocês, mas eu quero deixar um gabarito para não termos muita confusão em relação ao nosso stub e todos os outros testes.
[00:11] Afinal, o nosso último teste passou, mas os outros testes não estão passando. Então, por exemplo, se eu vier testar o nosso Deposit, o nosso teste de Deposit, ele não vai passar, porque ele não em o stub.

[00:24] Então, vamos produzir um stub para ele também. Eu vou fazer isso para todos eles. Vou vir aqui e vou na linha 65, vou copiar o stub que nós fizemos. Lembrando que o stub é a função when que fica verificando se o método dolarToReal foi chamado. Quando ele for chamado, ele vai responder automaticamente "5".

[00:47] Vou colocar a mesma coisa no nosso teste de widget do deposit em cima do await, antes do pump, porque ele precisa receber essa função antes do nosso dolarToReal ser chamado. Ele vai ser chamado dentro do Home, lá vem o header e vem sendo chamado o nosso dolarToReal.

[01:10] Importante que o stub esteja antes da chamada da função. Vou colocar isso. Também tem a diferença de que aqui estamos usando o nosso MockBankHttp e queremos usar o mesmo indivíduo. Vou na linha 56 em hpttpMock para usar também.

[01:27] Não precisamos de mais nada. Vou fazer a mesma coisa em todos os outros. Vamos lá, coloca uma música aí. Eu vou colocar aqui finds five box, BoxCard, mesma coisa em cima já temos o httpMock, mesma coisa aqui em cima. Vamos lá, linha 31, vou subir, colocar, apertar os botões "Ctrl + V".

[01:54] Colocar mais um stub na linha 34, mais uma vez mudar o nosso mock para o nosso indivíduo httpMock. Fazendo a mesma coisa para o LinearProgressIndicator. É só trabalho braçal mesmo.

[02:11] Mesma coisa para o nosso home, vou colocar o httpMock, na linha 26. Então, já deu para entender que o nosso mock está ali só para dar uma aparecida e ele não faz nada e no caso do nosso stub, ele pelo menos, retorna um valor desse *mock.

[02:28] Vamos mais uma vez no nosso home, na linha 17, httpMock e foi. Todos os testes foram. Vamos só verificar se todos os testes estão passando agora. É sempre importante ver se os testes estão passando.

[02:45] Um teste não passou, teve um teste que não passou. Unexpected number of calls. Ele esperou uma chamada, mas na verdade foram chamadas seis vezes o nosso dolarToReal. Por quê? Porque nós temos vários testes e ele acabou chamando várias vezes durante todo esse nosso home test a função dolarToReal.

[03:11] Vou até verificar e recapitular. Lembra que nosso testando MockHpttp.dolarToReal, nós usamos uma função chamada verify que verifica se esse nosso método foi chamado e se ele foi chamado apenas uma vez?

[03:30] No caso, agora, ele foi chamado seis vezes, porque nós fizemos vários testes e esse mesmo indivíduo chamou o mesmo método seis vezes. Então, agora o teste vai ter que ser alterado. Então, é importante termos essa noção da função called quando nós estamos buscando funções que foram chamadas no nosso teste.

[03:54] Mais uma vez vamos verificar se o teste passa agora. Não preciso rodar todos, porque todos passaram, menos esse último, só que agora ele não passou. Por quê? Porque eu rodei ele sozinho.

[04:05] Vocês estão conseguindo entender como que os testes, quando eles estão todos no mesmo arquivo, são dependentes? É importante vocês terem isso em mente também. Vou rodar o main, linha 9, completamente e agora todos os testes passam.

[04:19] Ficou mais claro? Ficou mais tranquilo? Que bom. "Testes" é um tema muito completo, muito extenso e vocês viram, não fizemos um teste nem de 10% de todo esse programa que é pequeno. Faltou testar todos os outros widgets, headers, textos, ações do transfer.

[04:41] Faltou criarmos um teste de unidade só para o nosso httpMock. Podemos criar um teste de unidade, não precisa, necessariamente, criar o pump widget. Não precisamos usar o widget para testar se a função foi chamada. Podemos só chamá-la e verificar se está sendo chamada tranquilamente.

[05:02] Existem muitas coisas que podemos fazer com testes, isso aqui é só o começo. Então, dá para explorar bastante os testes com o que vocês aprenderam até aqui. Muito obrigado.

@@08
Projeto final do curso
PRÓXIMA ATIVIDADE

Caso queira, você pode baixar aqui o projeto completo implementado neste curso.
E se preferir, você também pode acessar o repositório completo no GitHub.

https://github.com/alura-cursos/alura_flutter_curso_7/archive/refs/heads/Aula_5.zip

https://github.com/alura-cursos/alura_flutter_curso_7/tree/master

@@09
O que aprendemos?
PRÓXIMA ATIVIDADE

Vamos dar um replay no que aprendemos? Nessa aula, adicionamos ações no nosso teste e produzimos um Mock com Stub. Além disso, entendemos com mais clareza as relações de dependências nos testes:
Ações:
Quando testamos nosso aplicativos, nos deparamos com ações de interação com botões, caixas de texto, scrollables entre outros. As ações são instruções que damos ao nosso tester para interagir com certos Widgets a fim de verificar sua usabilidade.

Utilizar mocks:
Aprendemos que o Mock é usado para criar um dublê de dependências externas (como API’s ou bancos de dados fora do projeto) e que ele evita que tenhamos flaky tests.

Operar com Stub:
Descobrimos que não basta apenas criar um dublê, precisamos que esse dublê, em alguns casos, nos dê um retorno de valor utilizável, e o Stub é feito para retornar esse valor em nome do Dublê.

Entender as dependências nos testes
Agora que começamos a entrar mais a fundo nos testes, conseguimos ver com maior facilidade o quanto as dependências entre nossas Classes, métodos e Widgets podem ser complicadas, especialmente em testes automatizados.

Parabéns! Você finalizou mais um curso de Flutter! Agora você já está um passo mais perto de se tornar um(a) profissional na produção de aplicativo!

Conta pra gente o que você achou desse curso, seu feedback é extremamente importante para que a qualidade dos cursos de Flutter seja sempre encantadora.

Ah, e não esquece de entrar no Discord, na nossa comunidade de Mobile e mandar um oi pra gente lá! Estamos ansiosos para te conhecer. :)
Até a próxima!

@@10
Conclusão

[00:00] Olha só o quanto que nós aprendemos nesse curso. Começamos a entender o que são testes, para que funcionam. Depois nós demos uma olhada nesse nosso projeto chamado Alubank com algumas implementações que nós podemos depositar e transferir.
[00:16] Depois nós demos uma entendida em como que funciona o estado desse nosso projeto, mini gerenciamento de estado em que usamos o inherited widget, criamos um *bank_inherited *, um modelo de banco e depois começamos a entrar, de fato, nos testes.

[00:35] Aprendemos sobre testes unitários. Deixa eu abrir para vocês poderem ver a nossa pasta de testes. Nós criamos os testes unitários para o nosso bank model. Entendemos os nossos testes unitários, como é que esperamos um valor, é uma coisa mais simples.

[00:52] Saímos testando várias possibilidades aqui no nosso bank model e depois, no nosso teste de unidade. Nós começamos a entender melhor os testes de widget, que são um pouco mais complexos, um pouco melhores em qualidade, mas também demoram um tempo maior para serem feitos, até porque nós precisamos desenhar na tela.

[01:15] Então, aprendemos alguns conceitos como pump e usamos até o pumpWidget, ou o pumpOnSale. Depois disso tudo começamos a entender a questão do finder que é uma forma de encontrar os widgets ou objetos que estamos buscando na nossa tela.

[01:31] E podem ser de vários tipos diferentes, como texto ou por predicado ou por chave ou por tipo. Então, várias formas de encontrar os nosso widgets.

[01:44] Depois nós entendemos um pouco melhor como funcionam os matchers, como podemos comparar os nossos resultados. Pode encontrar um widget só, não encontrar nenhum widget, encontrar vários widgets diferentes, vários números de widgets diferentes*.

[01:57] Por fim, nós começamos a adentrar um pouco nas questões de ações que o nosso tester, o nosso robô, pode fazer para mudar o nosso projeto, interagir com o nosso projeto e ver se essa interação está certa.

[02:14] E só para finalizar, nós entendemos as questões de dublês que contemplam o mock. Antes de finalizar esse curso, de fato, de testes, eu queria conversar com vocês sobre a grande importância dos testes.

[02:27] Nós começamos esse curso sem saber nada e tinha até a história de que nós éramos desenvolvedores e projetamos um aplicativo por vários meses e lançamos e deu muito bug, deu muito problema e os testes eram a solução para evitar que o nosso projeto tenha muitos bugs.

[02:49] Então, o que eu quero que vocês entendam com esse curso, especificamente, não é só o conteúdo, mas a importância que os testes têm quando nós estamos produzindo algo de qualidade.

[03:01] Então, se você busca ser um profissional na área de Flutter, de programa em geral, eu aconselho fortemente que você crie o hábito de construir testes nos seus projetos. Assim você garante a qualidade deles e facilita, futuramente, quando você quiser entendê-los.

[03:22] Vamos ser sinceros, depois de um tempo nós vamos esquecendo o que nós implementamos em um projeto antigo. Então, os testes estão aqui para nos ajudar e eles podem até ser um pouco mais difíceis e um pouco trabalhosos, mas eles valem muito a pena, não só para qualidade do seu produto, mas para a sua qualidade de vida, de entendimento daquilo que você criou.

[03:45] Então, mais uma vez, muitíssimo obrigado, esse curso não foi feito só por mim, mas por uma equipe inteira e cheirosa do time de mobile da Alura.

[03:54] Qualquer coisa que vocês tenham gostado, podem nos falar lá no fórum que vamos repetir e aquilo que vocês não gostaram, podem nos falar também que nós vamos tentar evitar ao máximo. Muito obrigado e eu vejo vocês no próximo curso.

