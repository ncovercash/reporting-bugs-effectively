# Como Relatar Bugs De Maneira Eficaz

_por Simon Tatham, programador profissional e de softwares de código-livre. Tradução para o português por [CJr](http://www.celiojunior.com.br)._

## Introdução 

Qualquer um que tenha escrito software para uso público provavelmente recebeu ao menos um relatório de bugs ruim. Relatórios que não dizem nada ("Isso não funciona!"); relatórios que não fazem sentido; relatórios que trazem informações _erradas_. Relatórios contendo problemas que acabam por ser identificados como erros de usuário; relatórios de problemas que acabam sendo identificados como falhas de um programa externo; relatórios de problemas que acabam sendo identificados como falhas de rede.

Existe uma razão pela qual o suporte técnico é visto como um trabalho horrível para se fazer, e esta razão são os relatórios de bugs ruins. Entretanto, nem todos os relatórios de bug são desagradáveis: eu mantenho software livre quando não estou ganhando a vida, e algumas vezes recebo relatórios de bug maravilhosamente claros, úteis, _informativos_.

Neste ensaio vou tentar identificar claramente o que faz um relatório de bugs ser bom. Idealmente, eu gostaria que todo o mundo lesse esse ensaio antes de fazer qualquer relatório de bug para qualquer um. Certamente eu gostaria que todos que fazem relatórios de bug para _mim_ o lessem.

Sinteticamente, o objetivo de um relatorio de bug é tornar os programadores capazes de ver a falha do programa acontecer em frente aos seus olhos. Você pode mostrar a eles pessoalmente, ou fornecer-lhes instruções detalhadas e cuidadosas sobre como fazer o programa falhar. Se eles puderem fazê-lo falhar, tentarão obter informações extras até descobrirem a causa da falha. Se eles não podem fazê-lo falhar, vão ter que pedir a você para conseguir essas informações para eles.

Quando fizer relatórios de bug, tente fazer uma distinção muito clara entre os fatos reais ("Eu estava no computador e isso aconteceu") e especulações ("Eu _acho_ que o problema pode ser esse"). Se quiser, deixe de fora as especulações, mas não os fatos.

Quando você relata um bug, é porque deseja que ele seja consertado. Não faz sentido massacrar os programadores ou ser deliberadamente obscuro: o erro pode ser deles e o problema seu, e você pode estar certo em estar com raiva deles, mas o bug vai ser consertado mais rapidamente se você ajudá-los fornecendo todas as informações de que eles precisam. Lembre-se também de que se o programa é gratuito, então os autores estão fornecendo-o por bondade. Se muitas pessoas forem rudes com eles, eles podem deixar de ser bons.

## "Isso não funciona." 

Dê aos programadores o crédito de possuírem uma inteligência de nível básico: se o programa realmente não tem nada que funcione, eles provavelmente teriam notado. Como não notaram, ele tem que estar funcionando com eles. Portanto, ou você está fazendo alguma coisa diferente do que eles fazem ou seu ambiente é diferente do deles. Eles precisam de informação; fornecer essa informação é o propósito de um relatório de bug. Mais informação é quase sempre melhor que menos informação.

Muitos programadores, particularmente os que trabalham em softwares livres ou gratuitos, publicam suas listas de bugs conhecidos. Se você encontrar uma lista de bugs conhecidos, vale a pena lê-la para verificar se o bug que você encontrou já é conhecido. Se já é, provavelmente não vale a pena relatá-lo novamente, mas se você acha que tem mais informações para fornecer do que as que constam na lista, deve entrar em contato os programadores. Eles podem consertar o bug mais facilmente se você puder fornecer a eles informações que eles ainda não têm.

Este ensaio está cheio de diretrizes. Nenhuma delas é uma regra absoluta. Programadores específicos gostam de maneiras específicas de relatar bugs. Se o programa vem com diretrizes próprias sobre como relatar bugs, leia-as. Se as dicas que vem com o programa contradizem as descritas neste ensaio, siga-as!

Se você não está relatando um bug, mas apenas pedindo ajuda para utilizar o programa, deveria deixar claro que já procurou pela resposta para a sua pergunta ("Li a seção 5.2 e o capítulo 4, mas não encontrei nada que me dissesse se o que quero fazer é possível.") Isto vai permitir aos programadores saber como as pessoas esperam encontrar as respostas, e assim eles poderão fazer com que a documentação fique mais fácil de usar.

## "Mostre-me." 

Uma das melhores maneiras de relatar bugs é mostrá-los aos programadores. Coloque-os em frente ao seu computador, inicie o software e demonstre o erro. Deixe-os observar como você inicia a máquina, como você executa o software e interage com ele e também o que o software faz em resposta às suas entradas.

Eles sabem que o software gosta deles. Sabem quais as partes dele em que confiam, e sabem quais as que mais provavelmente contem falhas. Sabem intuitivamente o que esperar. Quando o software faz alguma coisa obviamente errada, eles já podem ter notado algo _sutilmente_ errado que aconteceu antes disso, e que pode lhes fornecer uma pista. Podem observar tudo que o computador faz durante a execução do teste, e escolher as informações relevantes por si mesmos.

Isso pode não ser o suficiente. Eles podem decidir que precisam de mais informações, e pedir a você para mostrar tudo de novo. Podem pedir a você para ensiná-los a realizar os passos do teste, e assim podem reproduzir o bug para si mesmos quantas vezes desejarem. Podem tentar variar os passos por algumas vezes, para verificar se o problema ocorre apenas em um caso ou em uma família de casos relacionados. Se você for azarado, eles podem precisar usar ferramentas de desenvolvimento por algumas horas e _realmente_ começar a investigar. Mais a coisa mais importante é tê-los olhando para o computador quando o erro acontecer. Uma vez que eles possam ver o problema acontecendo, usualmente podem sair dali e começar a consertá-lo.

## "Mostre-me como mostrar a mim mesmo" 

Esta é a era da Internet. Esta é a era das comunicações globais. Esta é a era em que eu posso enviar meu software para alguém na Rússia com o toque de um botão, e essa pessoa pode me enviar comentários sobre ele com a mesma facilidade. Mas se essa pessoa verifica um problema com o meu programa, ela _não pode_ me ter em frente ao computador quando ele ocorre. "Mostre-me" é bom quando você pode, mas você muitas vezes não pode.

Se você tem que reportar um bug para um programador que não pode estar com você pessoalmente, o objetivo do exercício é capacitá-lo a _reproduzir_ o problema. Você quer que o programador execute a sua própria cópia do programa, faca as mesmas coisas que você fez com ele e faça-o falhar da mesma maneira. Quando eles podem ver o problema acontecendo em frente aos seus olhos, então eles podem lidar com ele.

Então diga exatamente a eles o que você fez. Se o programa tem uma interface gráfica, diga quais botões você pressionou e em que ordem o fez. Se for um programa que você executa digitando um comando, mostre a eles precisamente que comando você digitou. Sempre que possível você deve fornecer uma transcrição fiel da sessão, mostrando quais comandos você digitou e o que o computador exibiu em resposta.

Dê ao programador toda a informação que você puder imaginar. Se o programa lê um arquivo, você provavelmente precisa enviar uma cópia dele. Se o programa troca dados com outro computador através de uma rede, você provavelmente não poderá enviar uma cópia do outro computador, mas pode ao menos dizer que tipo de computador ele é, e (se você puder obter a informação) que software ele está executando.

## "Funciona comigo. Então qual é o erro?" 

Se você fornecer a um programador uma longa lista de entradas e ações, e ele executá-las em sua própria máquina e nada der errado, então você não forneceu a ele informações suficientes. Possivelmente a falha não vai aparecer em todos os computadores; seu sistema e o dele podem ser diferentes em alguns pontos. Possivelmente você entendeu mal o que o programa deveria fazer, e vocês estão olhando exatamente para o mesmo resultado na tela e você acha que ela está errada e ele sabe que está certa.

Então, descreva também o que aconteceu. Diga a ele exatamente o que você viu. Diga a ele que você acha que o que viu era errado; melhor ainda, diga a ele exatamente o que você esperava ver. Se você disser apenas “e então deu errado”, deixou de fora informações importantes.

Se você viu mensagens de erro, diga ao programador, cuidadosa e precisamente, o que elas eram. Elas são importantes! Neste estágio, o programador não está tentando consertar o problema; ele está apenas tentando encontrá-lo. Ele precisa saber o que aconteceu de errado, e estas mensagens são o melhor que o computador pode fazer para dizê-lo a você. Anote as mensagens se não houver outra maneira de se lembrar delas; não vale a pena relatar que o programa apresentou erros se você não puder relatar também o conteúdo das mensagens de erro.

Se a mensagem de erro contém números, forneça-os ao programador. Só porque você não consegue ver nenhum significado neles isso não significa que não exista algum. Números contêm todos os tipos de informação que pode ser lida por programadores, e é provável que eles contenham pistas vitais. Números em mensagens de erro estão lá porque o computador está muito confuso para relatar o erro em palavras, mas está dando o melhor de si para fornecer a você a informação de algum jeito.

Neste estágio, o programador está na realidade fazendo um trabalho de detetive. Ele não sabe o que aconteceu, e não pode estar perto o suficiente para ver por si próprio o erro acontecer. Ele está então procurando por pistas que podem dizer o que houve. Mensagens de erro, seqüências incompreensíveis de números e mesmo lentidão inesperada são tão importantes quanto impressões digitais em uma cena de crime. Guarde-as!

Se você está usando Unix, o programa pode ter produzido um dump. Dumps são uma fonte particularmente boa de pistas, então não os jogue fora. Por outro lado, muitos programadores não gostam de receber arquivos imensos de dump por email sem ser avisados disso, então peça permissão antes de enviar esses arquivos para qualquer pessoa. Esteja atento para o fato que o dump contém um registro de todos os dados de estado do programa: quaisquer “segredos” envolvidos (talvez o programa estivesse tratando uma mensagem pessoal, ou trabalhando com dados confidenciais) podem estar contidos no arquivo de dump.

## "Então eu tentei…" 

Há várias coisas que você pode fazer quando um erro ou bug aparece. Muitas delas tornam o problema pior. Uma das minhas amigas da faculdade apagou todos os seus arquivos do Word por engano, e, antes de chamar por ajuda especializada, tentou reinstalar o Word; depois disso, tentou rodar o Defrag. Nada disso ajudou-a a recuperar seus arquivos, e fazendo isso ela bagunçou de tal maneira o seu HD que nenhum programa de recuperação seria capaz de recuperar nada. Se ela tivesse simplesmente deixado como estava, ela poderia ter tido uma chance de resgatar seus arquivos.

Usuários como ela são como uma fuinha acuada num canto: com as costas na parede e vendo a morte certa pela frente, ela ataca freneticamente, porque fazer alguma coisa tem que ser melhor do que não fazer nada. Esta atitude não é bem adaptada ao tipo de problemas que computadores produzem.

Ao invés de ser uma fuinha, seja um antílope. Quando um antílope se confronta com algo inesperado ou assustador, ele congela. Ele fica absolutamente parado e tenta não atrair nenhuma atenção, enquanto pensa e tenta descobrir a melhor coisa a fazer. (Se houvesse suporte técnico para antílopes, eles o chamariam nestes momentos.) Então, uma vez que eles tenham decidido qual é a coisa mais segura a fazer, eles a fazem.

Quando alguma coisa dá errado, pare imediatamente de fazer qualquer coisa. Não clique qualquer botão. Olhe para a tela e tente perceber qualquer coisa fora do comum, e memorize-a ou anote-a. Então, cautelosamente, pressione "OK" ou "Cancel", o que parecer mais seguro. Tente desenvolver um ato reflexo - se um computador fizer algo inesperado, congele.

Se você conseguir se safar do problema, seja fechando o programa afetado ou reiniciando o computador, uma boa coisa a fazer é tentar reproduzir novamente o erro. Programadores gostam de problemas que eles possam reproduzir. Programadores felizes consertam bugs mais rapidamente e com mais eficácia.

## "Acho que a modulação do tachyon deve estar com a polarização errada." 

Maus relatórios de bug não são produzidos somente por não-programadores. Alguns dos piores relatórios que eu já vi foram feitos por programadores, e algumas vezes por programadores.

Uma vez eu trabalhei com um programador que encontrava bugs em seu próprio código e tentava consertá-los. Muitas vezes ele achava um bug que não conseguia resolver, e me chamava para ajudar. "O que deu errado?", eu perguntava. Ele me respondia dizendo qual a sua opinião sobre o que precisava de ser consertado.

Isto funcionava bem quando a opinião dele estava certa. Isto significava que ele já tinha feito metade do trabalho, e que conseguiríamos finalizar o restante juntos. Era eficiente e útil.

Mas era muito diferente quando ele estava errado. Trabalhávamos por algum tempo tentando descobrir porque uma parte específica do programa estava produzindo dados incorretos, e eventualmente descobríamos que não estava, que estivéramos investigando código perfeitamente funcional por meia hora, e que o problema real estava em outro lugar.

Estou certo de que ele não agiria assim com um médico. "Doutor, preciso de uma receita para Hidroioiodina." As pessoas sabem que não podem dizer isso a um médico: você descreve os sintomas, os desconfortos reais e as dores, as erupções, as febres, e deixa o doutor fazer o diagnóstico de qual é o problema e o que fazer para resolvê-lo. Se não for assim, o doutor acha que você é um hipocondríaco ou drogado e te manda embora, o que é certíssimo.

É a mesma coisa com programadores. Fornecer seu próprio diagnóstico pode ser útil às vezes, mas sempre diga os sintomas. O diagnóstico é um extra opcional e não uma alternativa a fornecer os sintomas. Da mesma maneira, enviar o código-fonte com o conserto do problema é um acréscimo útil a um relatório de bugs, mas não um substituto para ele.

Se um programador pede informação extra a você, colabore! Uma vez alguém me relatou um problema, e eu pedi a essa pessoa para executar um comando que eu sabia que não funcionava. Pedi isso a ela porque queria saber qual das duas mensagens de erro possíveis o comando geraria. Saber isso forneceria uma pista vital. Mas a pessoa não executou o comando - ela só me enviou um email dizendo "Não, isso não vai funcionar.". Levou algum tempo até que eu a convencesse a realmente executar o comando.

Usar sua inteligência para ajudar os programadores é ótimo. Mesmo que suas deduções estejam erradas, eles seriam gratos pela sua tentativa de tornar a vida deles mais fácil. Mas relate os sintomas também, ou você com certeza vai tornar a vida deles muito mais difícil.

## "Engraçado, consegui fazer isso há cinco minutos sem problemas." 

Diga “problema intermitente” para qualquer programador e veja a careta que ele faz. Os problemas fáceis são aqueles onde repetir uma seqüência de passos simples vai fazer com que o erro ocorra. O programador pode então repetir estas ações em condições de teste bastante monitoradas e ver o que acontece com grande detalhe. Muitos problemas simplesmente não acontecem dessa forma: vai haver programas que falham uma vez por semana, uma vez a cada lua cheia, ou nunca falham quando você tenta reproduzi-los diante do programador, mas sempre falham quando você tem um prazo apertado para cumprir.

A maior parte dos problemas intermitentes não é verdadeiramente intermitente. Muitos deles têm uma lógica escondida em algum lugar. Alguns ocorrem somente quando a máquina está com pouca memória disponível, alguns acontecem apenas quando outro programa tenta modificar um arquivo crítico no momento errado, e alguns outros ocorrerão somente na primeira metade de cada hora! (Eu realmente vi alguns desses.)

Se você consegue reproduzir o bug, mas o programador não, uma causa provável é que o seu computador e o dele são diferentes de alguma maneira e esta diferença é a causa do problema. Eu tive um programa cuja janela se enrolava em uma pequena bola no canto superior esquerdo da tela, ficava lá _me aborrecendo_ . Mas ele só fazia isso em telas com resolução de 800x600 pixels; executava normalmente em meu monitor de 1024x768\.

O programador vai querer saber tudo o que você puder descobrir sobre o problema. Tentar reproduzi-lo em outra máquina, talvez. Tente reproduzi-lo duas ou três vezes e ver quantas vezes ele falha. Se ele acontece quando você está fazendo uma tarefa importante, mas não quando está tentando demonstrá-lo, a causa da falha pode ser o grande tempo de execução ou o tratamento de grandes arquivos. Tente lembrar com quantos detalhes puder sobre o que você estava fazendo quando o erro ocorreu e, se identificar padrões, mencione-os. Tudo o que você puder fornecer pode ajudar. Mesmo que seja somente uma informação probabilística (como “o programa tende a falhar quando o Emacs está executando”) que não forneça pistas diretas sobre a causa do problema, ela pode ajudar o programador a reproduzir o erro.

Mais importante ainda, o programador vai querer estar certo de que ele está lidando com um verdadeiro problema intermitente ou com um problema específico da sua máquina. Ele vai querer saber montes de detalhes sobre seu computador, para assim poder descobrir como o computador dele difere do seu. Vários destes detalhes vão depender especificamente do programa, mas algo que você deve estar definitivamente pronto para fornecer são números de versão. O número de versão do programa em si, o do sistema operacional e provavelmente os de qualquer outro programa que esteja envolvido no problema.

## "Então eu carreguei o disco no meu Windows..." 

Em relatórios de bug, escrever claramente é essencial. Se o programador não consegue entender o que você quis dizer, era preferível que você não tivesse dito nada.

Eu recebo relatórios de bug de todas as partes do mundo. Muitos deles vêm de pessoas que não têm o inglês como sua língua-mãe, e muitos deles pedem desculpas pelo seu inglês ruim. Em geral, os relatórios de bug que contêm pedidos de desculpas pelo mau inglês são realmente claros e úteis. Todos os relatórios mais confusos vêm de pessoas cuja língua-mãe é o inglês e que presumem que eu vou entendê-los mesmo que não façam qualquer esforço por clareza e precisão.

*   _Seja específico_. Se você puder fazer a mesma coisa de duas maneiras diferentes, diga qual delas usou. "Eu selecionei a opção Carregar" pode significar "Eu cliquei o botão Carregar" ou "Eu pressionei Alt-L". Diga qual delas você usou. Algumas vezes isso é importante.
*   _Seja prolixo_. Dê mais informação ao invés de menos. Se você der informações demais, o programador pode ignorar algumas delas. Se você der informações de menos, eles tem que voltar a você e perguntar mais. Uma vez tive que gastar semanas para conseguir uma quantidade de informações que fosse útil, porque elas apareciam em pequenas frases de cada vez.
*   _Seja cuidadoso com os pronomes_. Não use palavras como "isso", ou referências como "a janela" quando o que elas puderem significar não for totalmente claro. Considere a frase: "Eu iniciei o programa FooApp. Ele mostrou uma janela de advertência. Tentei fechar e ele travou." Não está claro o que o usuário tentou fechar. Foi a janela de advertência ou a aplicação FooApp? Isso faz diferença. Ao invés disso, ele poderia ter dito "Eu iniciei o programa FooApp, que mostrou uma janela de advertência. Tentei fechar esta janela, e o programa travou.". Esta última frase é mais longa e mais repetitiva, mas também é mais clara e menos propensa a ambiguidades.
*   _Leia o que você escreveu_. Leia o relatório para você mesmo, e verifique se o que você pensou está claro. Se você fez uma lista de passos que deveriam produzir a falha, tente segui-los você mesmo, para verificar se esqueceu algum deles.

## Sumário 

*   O objetivo principal de um relatório de bugs é permitir que os programadores possam ver o erro com seus próprios olhos. Se você não pode estar com eles pessoalmente para reproduzir a falha, dê-lhes instruções detalhadas para que possam reproduzir a falha por si próprios..
*   No caso de o objetivo principal não ter sido alcançado e os programadores _não puderem_ ver a falha por si mesmos, o segundo objetivo de um relatório de bug é descrever o que aconteceu de errado. Descreva tudo em detalhes. Diga o que você viu, e também o que esperaria ver acontecer. Escreva as mensagens de erro, especialmente se elas contém números.
*   Quando o seu computador fizer alguma coisa inesperada, _pare_.Não faça nada até que esteja calmo, e não faça nada que você ache que possa ser perigoso.
*   Tente por todos os meios diagnosticar a falha por você mesmo se acha que pode fazê-lo; mas mesmo que faça isso, você ainda deve relatar os sintomas.
*   Esteja pronto para fornecer informações extras no caso de os programadores precisarem delas. Se eles não precisassem, não as pediriam. Eles não estão sendo deliberadamente inábeis. Tenha os números de versão do programa à mão, porque provavelmente eles serão necessários.
*   Escreva com clareza. Diga o que tem para dizer, e esteja certo de que o texto não possa ser mal interpretado.
*   Acima de tudo, seja _preciso_. Programadores gostam de precisão.

* * *

_Aviso de negação de responsabilidade_ : Nunca vi uma fuinha ou um antílope ao vivo. Minha zoologia pode ser inexata.
