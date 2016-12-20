# Comment signaler efficacement un bug

_Version originale écrite par Simon Tatham, programmeur professionnel et de logiciels libres;  
traduit par Julien Kirch, développeur._

## Introduction

Quiconque a déjà développé un logiciel destiné à un usage public a probablement déjà reçu au moins un mauvais rapport de bug. Il y a les rapports qui ne disent rien ("Ça ne marche pas !"), qui n'ont aucun sens, qui ne donnent pas assez d'informations, ou même qui donnent de _fausses_ informations. Il y a des comptes-rendus de problèmes qui sont dus à des erreurs de l'utilisateur, dus au programme de quelqu'un d'autre, ou dus à des problèmes de réseau.

Une chose explique qu'on considère le support technique comme une tâche horrible : les mauvais rapports de bug. Toutefois, tous les rapports de bug ne sont pas désagréables : quand je ne gagne pas ma vie, je développe des logiciels libres, et quelquefois je reçois des rapports de bug merveilleux, clairs, utiles et _informatifs_.

Dans ce texte, je vais essayer d'exposer clairement ce qui fait un bon rapport de bug. Idéalement, j'aimerais que tout le monde sur terre lise ce texte avant de signaler un bug à qui que ce soit. En tous cas j'aimerais au moins que tous ceux qui _me_ signalent des bugs l'aient lu.

En gros, le but d'un rapport de bug est de permettre au programmeur de voir le programme planter devant lui. Vous pouvez soit lui montrer de visu, soit lui fournir des instructions soignées et détaillées sur la façon de le faire planter. S'il parvient à le faire planter, il essaiera de collecter des informations jusqu'à découvrir la cause du bug. S'il n'y parvient pas, il devra vous demander d'obtenir ces informations pour lui.

Dans un rapport de bug, essayez de séparer nettement les faits ("J'étais devant l'ordinateur et ceci _s'est produit_") des spéculations ("Je _pense_ que c'est ça le problème"). Si vous voulez, vous pouvez laisser tomber les spéculations, mais en aucun cas les faits.

Quand vous signalez un bug, vous le faites car vous voulez que ce bug soit corrigé. Ce n'est pas la peine de houspiller les programmeurs, ou de leur faire délibérément perdre leur temps : c'est peut-être leur faute et votre problème, et vous avez le droit d'être en colère contre eux, mais le bug sera corrigé plus rapidement si vous les aidez en leur fournissant toutes les informations dont ils ont besoin. D'autre part, n'oubliez pas que si ce programme est gratuit, c'est que l'auteur s'en occupe par gentillesse, alors si trop de gens se montrent désobligeants avec lui, il arrêtera peut-être d'être gentil.

## "Ça ne fonctionne pas"

Les programmeurs ne sont pas des idiots : si le programme ne fonctionnait pas du tout, ils s'en seraient probablement déjà rendu compte. Comme ils n'ont rien remarqué, pour eux, il doit fonctionner. Donc, soit vous faites quelque chose d'une autre manière qu'eux, ou votre environnement est différent du leur. Ils ont besoin d'informations ; leur fournir ces informations et l'objectif d'un rapport de bug. Plus d'informations est toujours mieux que moins.

Beaucoup de programmes, particulièrement les programmes libres, sont accompagnés de la liste de leurs bugs connus. Si vous pouvez mettre la main dessus, mieux vaudrait la lire pour vérifier si le bug que vous venez de découvrir n'est pas déjà référencé. S'il l'est déjà, il est probablement inutile de faire un nouveau rapport, sauf si vous pensez disposer de plus d'informations que n'en contient le rapport dans la liste de bugs. Les programmeurs pourront peut-être corriger plus facilement le bug si vous leur fournissez des informations qu'ils ne possèdent pas encore.

Ce texte est rempli de consignes, et aucune d'entre elles n'est une règle absolue. Certains programmeurs veulent que les bugs leur soient signalés sous une forme particulière. Si le programme est fourni avec son propre assortiment de règles de rapport de bug, lisez le. S'il contredit celles de ce texte, suivez le.

Si vous ne signalez pas un bug mais demandez seulement de l'aide pour utiliser le programme, vous devriez indiquer où vous avez déjà cherché la réponse à votre question ("J'ai regardé dans le chapitre 4 et dans la section 5.2 mais je n'ai rien trouvé m'indiquant si c'était possible"). Cela permettra aux programmeurs de savoir où les gens pensent trouver la réponse, et ainsi d'améliorer la documentation.

## "Montre moi."

L'une des meilleures manières dont vous pouvez signaler un bug est de le montrer à un programmeur. Amenez-le devant votre ordinateur, lancez son programme, et montrez lui ce qui se passe mal. Laissez le vous voir démarrer la machine, lancer le programme, l'utiliser, et voir comment il répond à vos actions.

Il connaît ce programme comme sa poche. Il sait en quelles parties il peut avoir confiance, et quelles parties peuvent avoir des défauts. Il sait intuitivement ce qu'il cherche. Quand arrive le moment où le programme se met à faire clairement n'importe quoi, il a peut-être déjà remarqué une _légère_ erreur survenue plus tôt et qui pourrait lui donner une indication. Il peut observer tout ce que fait l'ordinateur pendant le test et noter les choses importantes.

Cela ne sera peut-être pas suffisant. Il pourrait décider qu'il a besoin de plus d'informations, et vous demander de refaire la même chose. Il pourrait vous demander de lui décrire toute l'opération, pour qu'il puisse reproduire le bug autant de fois qu'il le désire. Il pourrait faire varier la procédure plusieurs fois, pour vérifier si le problème apparaît dans un seul cas ou dans un ensemble lié de cas. Si vous êtes malchanceux, il aura peut-être besoin de prendre votre place pendant quelques heures, avec des outils de développement, et _vraiment_ commencer à creuser. Mais la chose la plus importante est que le programmeur observe l'ordinateur quand ça se passe mal. Quand il a vu le problème se produire, il peut généralement commencer à le résoudre.

## "Montre moi comment y arriver"

Nous sommes à l'ère d'Internet, de la communication globale, où en appuyant simplement sur un bouton, je peux envoyer mon programme à quelqu'un en Russie, et où tout aussi simplement il peut m'envoyer ses commentaires sur celui-ci. Mais s'il a un problème avec mon programme, je ne peux _pas_ aller chez lui voir le programme planter. "Montre moi" c'est bien quand on peut, mais souvent, on ne peut pas.

Si vous devez signaler un bug à un programmeur qui ne peut être physiquement présent, le but de l'exercice est de lui permettre de _reproduire_ ce bug. Vous voulez que le programmeur exécute sa propre copie du programme, effectue les mêmes manipulations, et le fasse planter de la même manière. Quand il réussit à faire planter le programme devant lui, il peut s'en occuper.

Alors dites-lui _exactement_ ce que vous avez fait. S'il s'agit d'un programme graphique, dites lui sur quels boutons vous avez cliqué, et dans quel ordre. Si c'est un programme que vous avez lancé par une commande, donnez lui précisément la commande que vous avez utilisée. Si possible, vous devriez lui fournir une transcription complète de la session, montrant quelles commandes vous avez tapées, et quelles réponses l'ordinateur a retournées.

Donnez au programmeur toutes les entrées auxquelles vous pouvez penser. Si le programme lit un fichier, vous devriez probablement en envoyer une copie. Si l'ordinateur communique avec un autre ordinateur via un réseau, vous ne pourrez probablement pas envoyer une copie de cet ordinateur, mais vous pouvez au moins indiquer de quel type d'ordinateur il s'agit, et (si vous le pouvez) quels logiciels s'y exécutent.

## "Chez moi ça fonctionne. Alors d'où vient le problème ?"

Si vous donnez au programmeur une longue liste d'entrées et d'actions, qu'il lance sa propre copie du programme, et qu'aucun problème n'apparaît, c'est que vous ne lui avez pas donné suffisamment d'informations. Peut-être que l'erreur n'apparaît pas sur tous les ordinateurs ; vos deux systèmes diffèrent peut-être d'une manière ou d'une autre. Vous avez peut-être mal compris ce que le programme est censé faire, et vous êtes tous deux exactement devant le même écran, mais vous pensez qu'il s'agit d'une erreur, et il sait qu'il n'y a aucun problème.

Donc décrivez ce qui s'est passé. Dites _exactement_ ce que vous avez vu. Dites pourquoi vous pensez que ce que vous avez vu était une erreur ; au mieux dites lui exactement ce que vous pensiez voir. Si vous dites "et là, ça a planté", vous oubliez des informations très importantes.

Si des messages d'erreur apparaissent, rapportez les soigneusement et précisément au programmeur. Ils sont _importants_. A cet instant, le programmeur n'essaie pas de résoudre le problème : il essaie seulement de le localiser. Il a besoin de savoir ce qu'il s'est mal passé, et ces messages d'erreurs représentent le résultat des efforts de l'ordinateur pour vous l'indiquer. Recopiez ces erreurs si vous n'avez pas d'autre moyen de les conserver, mais il n'est pas très utile d'indiquer que le programme a généré une erreur, à moins que vous ne puissiez rapporter également quel était ce message d'erreur.

En particulier, si le message d'erreur comprend des nombres, _rapportez les_ au programmeur. Ce n'est pas parce que vous n'y voyez aucune signification qu'ils n'en ont pas. Ces nombres contiennent toutes sortes d'informations qui peuvent être exploitées par les programmeurs, et qui sont susceptibles de contenir des indications vitales. Les nombres dans les messages d'erreurs apparaissent dans les cas où l'ordinateur est trop embrouillé pour rendre compte de l'erreur sous forme de mots, mais il fait son possible pour vous fournir les informations importantes d'une manière ou d'une autre.

À ce moment, le programmeur effectue en fait un travail de détective. Il ne sait pas ce qui est arrivé, et ne peut pas s'approcher suffisamment pour le voir par lui-même, il cherche donc des éléments lui permettant de découvrir ce qu'il cherche. Les messages d'erreurs, les chaînes de nombres incompréhensibles, et mêmes des retards inexpliqués sont pour lui comme des empreintes digitales sur la scène d'un crime. Conservez les !

Si vous utilisez Unix, le programme a peut-être généré un core dump. Les core dumps sont une source d'informations particulièrement bonne, alors ne les effacez pas. D'un autre côté, la plupart des programmeurs n'apprécient guère de recevoir d'énormes core dumps par mail sans avoir été prévenu, alors demandez leur avant d'en envoyer un. Sachez également que les core dump contiennent un enregistrement complet de l'état du programme, toute donnée "secrète" (si par exemple le programme contenait un message personnel, ou traitait des données confidentielles) peut être contenue dans ce fichier.

## "Alors j'ai essayé ..."

Quand un bug arrive, vous pouvez faire beaucoup de choses. Beaucoup d'entre elles ne font qu'aggraver le problème. Une de mes amies à l'école a effacé tous ses fichiers Word par erreur, et avant de demander de l'aide, elle a essayé de réinstaller Word, puis de lancer defrag. Aucun des deux n'a contribué à récupérer les fichiers, et ils ont altéré le disque dur au point qu'aucun programme de récupération ne serait capable de sauver quoi que ce soit. Si elle n'avait rien fait, elle aurait pu avoir une chance.

Ce genre d'utilisateurs est comme une mangouste acculée dans un coin : le dos au mur et voyant une mort certaine arriver, elle attaque frénétiquement parce qu'il vaut mieux faire quelque chose plutôt que rien. Mais cette attitude n'est pas très bien adaptée au type de problèmes que les ordinateurs produisent.

Au lieu d'être une mangouste, soyez une antilope. Quand une antilope est confrontée avec quelque chose d'inattendu ou d'effrayant, elle s'immobilise. Elle reste totalement immobile et essaie de ne pas attirer l'attention; et, pendant qu'elle est stoppée, elle réfléchit à la meilleure chose à faire. (Si les antilopes disposaient d'un support technique, c'est à ce moment là qu'elles téléphoneraient.) Puis, une fois qu'elle a décidé quelle était la chose la plus sûre à faire, elle la fait.

Quand quelque chose se passe mal, cessez immédiatement de faire _quoi que ce soit_. N'appuyez sur aucun bouton. Regardez l'écran et observez tout ce qui sort de l'ordinaire, et souvenez vous-en ou notez le. Ensuite seulement, vous pourrez cliquer prudemment sur "OK" ou "Annuler", suivant ce qui vous semble le plus sûr. Essayez de développer une réaction réflexe : si un ordinateur a une réaction inattendue, arrêtez vous.

Si vous réussissez à vous tirer du problème, que ce soit en fermant l'application concernée ou en rebootant l'ordinateur, il serait bon d'essayer de le reproduire. Les programmeurs aiment les problèmes qu'ils peuvent reproduire. Et les programmeurs heureux corrigent les bugs plus rapidement, et plus efficacement.

## "Je pense que la modulation tachyonique doit être mal polarisée"

Les non programmeurs n'ont pas le monopole des mauvais rapports d'erreur. Certains des plus mauvais rapports d'erreur que j'ai jamais vu proviennent de programmeurs, et même de bons programmeurs.

Il m'est arrivé une fois, de travailler avec un autre programmeur, qui ne cessait de trouver de erreurs dans son propre code et de les corriger. De temps en temps il tombait sur un bug qu'il n'arrivait pas à corriger et il me demandait de l'aide. "Quel est le problème ?", lui demandais-je. Il me répondait en me donnant sa propre opinion sur ce qu'il fallait corriger.

Quand son opinion était juste, ça se passait bien. Dans ce cas, il avait déjà fait la moitié du travail, et nous étions capable de terminer ensemble. C'était efficace et utile.

Mais parfois, il se trompait. Nous pouvions alors passer un certain temps à essayer de comprendre pourquoi une certaine partie du programme produisait des données incorrectes, pour parfois nous rendre compte qu'au contraire il fonctionnait parfaitement, et que nous venions de passer une demi-heure à examiner une portion de code parfaitement fonctionnelle, et qu'en fait le problème se situait ailleurs.

Je suis sûr qu'il ne se conduirait pas ainsi avec un médecin: "Docteur, je voudrais une prescription pour de l'Hydroyoyodyne." Les gens savent qu'il ne faut pas se conduire ainsi avec un médecin : vous lui décrivez les symptômes, gènes, souffrances, douleurs, éruptions et fièvres, et vous le laissez diagnostiquer le problème et ce qu'il faut faire. Dans le cas contraire, le médecin vous prend pour un hypocondriaque ou un cinglé, et il a plutôt raison.

Il en va de même avec les programmeurs. Fournir votre propre diagnostic est parfois utile, mais donnez toujours les symptômes. Le diagnostic est un plus, et pas une alternative aux symptômes. De même, envoyer une modification à effectuer sur le code pour résoudre est un bon ajout à un rapport de bug, mais pas un substitut adéquat.

Si un programmeur vous demande des informations supplémentaires, ne l'ignorez pas. Une fois, quelqu'un m'a signalé un bug, et je lui ai demandé d'essayer une commande en sachant qu'elle ne fonctionnerait pas. Je voulais qu'il l'essaie parce que je voulais savoir lequel de deux messages d'erreur allait en résulter. Avoir cette réponse m'aurait donné un indice vital. Mais il n'a pas essayé, il s'est contenté de me répondre "Non, ça ne fonctionnera pas". Il m'a fallu du temps pour le persuader d'essayer réellement.

C'est très bien d'utiliser son intelligence pour aider le programmeur. Même si vos déductions sont fausses, le programmeur devrait vous être reconnaissant d'avoir, au moins, essayé de lui simplifier la vie. Mais n'oubliez pas de lui fournir aussi les symptômes, sans cela vous pourriez bien lui rendre la vie bien plus difficile.

## "C'est marrant, j'ai fait ça il y a juste une seconde."

Dites "bug intermittent" à n'importe quel programmeur et regardez son visage se décomposer. Les problèmes simples sont ceux qui sont déclenchés par une séquence d'actions simple. Dans ce cas le programmeur peut répéter ces actions, en observant attentivement les conditions de tests et surveiller en détail ce qui arrive. Trop de problèmes ne suivent pas cette règle : il y a des programmes qui se plantent une fois par semaine, de temps en temps, ou jamais quand vous essayez devant le programmeur, mais systématiquement quand une deadline se rapproche.

La plupart des bugs intermittents ne sont pas réellement intermittents. Ils obéissent généralement à une certaine logique. Certains se manifestent quand la machine arrive à court de mémoire, certains quand un autre programme essaie de modifier un fichier critique au mauvais moment, et certains uniquement pendant la première demie de chaque heure. (J'en ai déjà vu un de cette dernière sorte).

Par ailleurs, si vous pouvez reproduire le bug, mais que le programmeur n'y parvient pas, il se peut très bien que vos ordinateurs diffèrent, et que ce soit cette différence, qui cause le problème. Un jour j'ai eu un programme dont la fenêtre s'enroulait en une petite balle dans le coin supérieur gauche de l'écran, et restait là _à bouder_. Mais il ne se comportait ainsi que sur des écrans 800x600, sur mon moniteur 1024x768, tout se passait bien.

Le programmeur voudra connaître tout ce que vous pouvez découvrir sur le problème. Essayez sur une autre machine. Essayez deux ou trois fois pour connaître la fréquence du plantage. Si ça se passe mal quand vous faites un travail lourd mais pas quand vous voulez le montrer, c'est que c'est peut-être l'utilisation pendant une longue durée ou avec de gros fichiers qui cause le problème. Essayez de vous rappeler autant de détails que vous le pouvez sur ce que vous faisiez quand l'erreur est apparue, et si vous y voyez un modèle, mentionnez le. Toute information peut être utile, même s'il ne s'agit que d'une probabilité (comme "ça a tendance à planter plus souvent quand emacs est lancé"), peut-être que ça ne donne pas d'indication directe sur la cause du problème, mais il est possible que ça puisse aider le programmeur à le reproduire.

Et le plus important : le programmeur voudra être sûr de savoir s'il s'agit d'une vraie erreur intermittente ou d'un bug spécifique à l'ordinateur. Il voudra connaître le maximum de détails sur votre ordinateur, pour pouvoir travailler sur ce qui le différencie du sien. Beaucoup d'entre eux sont spécifiques au programme, mais les numéros de versions seront très certainement une chose à préciser : le numéro de version du programme, celui du système d'exploitation, et probablement ceux de tout programmes impliqués dans le problème.

## "Alors j'ai chargé ma disquette dans Windows . . ."

Il est essentiel qu'un rapport de bug soit rédigé clairement. Si le programmeur ne parvient pas à comprendre ce que vous voulez dire, vous auriez tout aussi bien fait de n'avoir rien écrit.

Je reçois des rapports de bugs qui viennent de partout. Beaucoup d'entre eux proviennent de personnes dont l'anglais n'est pas la langue maternelle, et un grand nombre d'entre eux s'excusent de leur mauvais anglais. En général, ces rapports de bugs sont clairs et utiles ; les rapports les plus obscurs étant envoyés par des personnes dont l'anglais est la langue maternelle, et qui pensent que je parviendrai à les comprendre même s'ils ne font aucun effort de clarté ou de précision.

*   _Soyez spécifique._ Si vous pouvez faire une chose de deux manières différentes, indiquez celle que vous avez utilisée. "J'ai sélectionné Charger" peut signifier "J'ai cliqué sur charger" ou "J'ai appuyé sur ALT-L". Ça peut sembler inutile, mais parfois, ça compte.
*   _Soyez prolixe._ Donnez plutôt plus d'informations que moins. Si vous en dites trop, le programmeur pourra en ignorer une partie, mais si vous n'en dites pas suffisamment, il devra vous répondre en vous posant d'autres questions. Il m'est arrivé de recevoir un rapport d'erreur constitué d'une seule phrase ; et à chacune de mes demandes d'informations, la réponse du rapporteur tenait en une phrase. Il m'a fallu plusieurs semaines pour obtenir une quantité suffisante d'information, tellement les réponses étaient brèves.
*   _Faites attention aux pronoms._ N'utilisez pas des mots comme "il", ou des références comme "la fenêtre" quand leur signification est imprécise. Considérez l'exemple suivant : "J'ai lancé l'application FooApp. Elle a affiché une fenêtre d'erreur. J'ai essayé de la fermer et elle a planté". Quel élément l'utilisateur a-t-il bien pu essayé de fermer ? S'agit-il de la fenêtre d'erreur ou de toute l'application ? Ça fait une différence ! Au lieu de cela, dites plutôt : "J'ai lance l'application FooApp. Elle a affiché une fenêtre d'erreur. J'ai essayé de fermer la fenêtre d'erreur et FooApp a planté". C'est plus long et répétitif, mais également plus clair et moins susceptible d'être compris de travers.
*   _Relisez ce que vous avez écrit._ Relisez le rapport et voyez si vous pensez qu'il est clair. Si vous avez fait une liste des actions qui devraient produire le bug, essayez de la suivre, et vérifier ainsi qu'aucune étape ne manque.

## Résumé

*   Le premier objectif d'un rapport de bug est de permettre au programmeur de voir le bug de ses propres yeux. Si vous _ne pouvez_ le faire planter devant lui, donnez lui des instructions _détaillées_ afin qu'il puisse le faire planter par lui-même.
*   Si le premier objectif ne peut être atteint, et donc si le programmeur ne peut voir l'erreur se produire, le second objectif d'un rapport de bug est de décrire ce qui s'est mal passé. Décrivez tout, en détails. Dites ce que vous avez vu, mais dites aussi ce que vous vous attendiez à voir. Recopiez les messages d'erreur, _surtout_ s'ils contiennent des nombres.
*   Quand votre ordinateur fait quelque chose d'inattendu, _arrêtez-vous_. Ne faites rien tant que vous n'êtes pas calme, et ne faites rien que vous pensez pouvoir être dangereux.
*   Bien entendu, si vous pensez en être capable, diagnostiquez l'erreur par vous-même, mais si vous le faites, vous devriez tout de même lui communiquer les symptômes.
*   Soyez prêt à fournir des informations supplémentaires si le programmeur en a besoin. S'il pouvait s'en passer, il ne vous les demanderait pas. Il ne vous dérange pas pour le plaisir.
*   Écrivez clairement. Dites ce que vous voulez dire, et soyez sûr que ça ne peut pas être mal compris.
*   Et surtout, soyez précis : les programmeurs aiment la précision.

* * *

_Précision :_ je n'ai en fait jamais vu ni mangouste ni antilope, ma zoologie est donc peut-être incorrecte.