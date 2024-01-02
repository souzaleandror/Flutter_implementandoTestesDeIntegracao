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