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
PRÓXIMA ATIVIDADE

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
PRÓXIMA ATIVIDADE

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
PRÓXIMA ATIVIDADE

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
PRÓXIMA ATIVIDADE

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
PRÓXIMA ATIVIDADE

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