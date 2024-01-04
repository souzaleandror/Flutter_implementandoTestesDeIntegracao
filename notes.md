#### 02/01/2024

Curso de Flutter: aplicando testes de unidade, de Widget e Mocks

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