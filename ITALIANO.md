# Come segnalare bug efficacemente

_di Simon Tatham, sviluppatore di software libero e per professione_  
_Traduzione in italiano a cura di [Roberto Schiabel](http://robertoschiabel.wordpress.com)._

## Introduzione

Chiunque abbia sviluppato software per uso pubblico sicuramente avra' ricevuto almeno una segnalazione di un bug. Alcune non dicono nulla (“Non funziona!”) o non hanno senso; altre non forniscono sufficienti informazioni oppure informazioni _errate_; altre ancora si rivelano invece essere errori dell'utente; infine segnalazioni che in realta' sono errori di altri programmi oppure che si rivelano essere problemi di rete.

L'assistenza tecnica e' spesso vista come un compito ingrato ed il motivo sta proprio nelle errate segnalazioni di bug. Ad ogni modo, non tutte le segnalazioni sono antipatiche: quando gli impegni di lavoro me lo concedono, mi occupo della manutenzione del software libero e qualche volta mi capita di riceverne _chiare_ ed utili.

In questo articolo cerchero' di esprimere chiaramente quali sono le modalita' per effettuare una segnalazione utile. Mi piacerebbe che tutti leggessero questo testo prima di fare una segnalazione. Certamente vorrei fosse fatto per quelle che to _io_ ricevo.

In sintesi, lo scopo di una segnalazione e' mettere lo sviluppatore, o piu' in generale il supporto tecnico, nella condizione di verificare l'errore direttamente. Potete persino mostrarglielo dal vivo se volete, o fornirgli precise istruzioni su come generare l'errore. Se il supporto tecnico riuscira' a ricreare le condizioni per generare l'errore, allora lo fara' per ottenere maggiori informazioni, fino a scoprirne la causa. Se le condizioni non sono riproducibili, il supporto tecnico dovra' rivolgersi a chi ha effettuato la segnalazione.

Nell'effettuare una segnalazione quindi, cercate di riportare i fatti come sono accaduti in modo chiaro (“Ero al computer ed accadde che [. . .]'”) e, se volete, le vostre ipotesi (“_Penso_ che la causa del problema sia [. . .]”). Potete tralasciare le supposizioni, ma non dimenticate i fatti.

Quando segnalate un bug lo fate perche' volete che l'errore venga risolto. Non c'e' motivo di arrabbiarvi con il personale dell'assistenza oppure di essere scortesi: potrebbe essere un problema noto e, quindi, potreste aver il diritto di essere arrabbiati, ma il bug verra' sistemato in fretta se potrete fornire le informazioni necessarie. Tengo a sottolineare il fatto che quando si tratta di software libero, l'assistenza e' fornita direttamente dallo sviluppatore, quindi se la gente e' sgarbata la risposta potrebbe non essere troppo gentile.

## "Non funziona."

Concedete al programmatore un minimo di intelligenza: se il programma effettivamente non funzionasse per nulla, probabilmente se ne sarebbe già reso conto. Dato che non e' stato notato vuol dire che, secondo il programmatore, il programma funziona. Da cio' si deduce che, o voi state facendo qualcosa di diverso oppure la vostra configurazione e' differente da quella dello sviluppatore. Il supporto tecnico ha bisogno di informazioni e fornire queste informazioni e' proprio lo scopo della segnalazione. E' meglio avere a disposizione informazioni in eccesso che averne poche.

Molti programmi, in particolare quelli liberi, rendono note le liste dei loro bug. E' consigliabile leggerle e verificare se il vostro bug e' già presente. Nel caso sia gia' noto, allora vi consiglio di non segnalarlo un'altra volta, tuttavia se pensate di avere nuovi indizi, contattate comunque il supporto tecnico. E' probabile che il bug venga risolto prima, e piu' facilmente, se fornirete nuove informazioni al supporto tecnico.

In questo testo troverete molte linee guida ma nessuna di loro rappresenta una regola ferrea. Alcuni programmatori preferiscono ricevere le segnalazioni in un particolare formato. Se assieme al programma sono fornite anche le istruzioni per le segnalazioni di bug, allora e' meglio leggerle. Se ci sono differenze fra quando scritto qui e quelle fornite a corredo del programma, allora e' meglio seguire quest'ultime!

Se invece non volete segnalare un bug ma solo chiedere un aiuto, dovreste anche riportare dove avete gia' cercato una risposta (“Ho cercato nel capitolo 4 e nella sezione 5.2 ma non ho trovato nulla che mi dicesse se e' possibile [. . .]”).In questo modo il programmatore sapra' dove ci si aspetta di trovare le informazioni desiderate e quindi potra' preparare una documentazione di piu' facile consultazione.

## "Fammi vedere."

Uno dei modi migliori per segnalare un bug e' di mostrarlo direttamente al programmatore. Mettetelo di fronte al vostro computer, eseguite il programma e mostrategli cosa non funziona. Lasciate che vi guardi mentre accendete il computer, mentre eseguite il programma e come lavorate, e lasciate anche che guardi come reagisce il programma ai vostri comandi.

Gli sviluppatori conoscono il programma come il palmo della loro mano. Sanno quali parti di codice sono affidabili e quali invece possono generare errori. Sanno gia' cosa cercare. Nel momento in cui il programma non opera correttamente avranno sicuramente gia' _notato_ qualcosa di strano che puo' fornir loro degli indizi. Sono in grado di osservare come si comporta il computer durante il test e di isolare la parte incriminata per arrivare alla soluzione del problema.

Questo purtroppo non sempre e' sufficiente a individuare il problema. Lo sviluppatore potrebbe necessitare di altre informazioni, e quindi chiedervi di mostrargli l'errore un'altra volta; chiedervi di guidarlo per mano, cosi' da poter riprodurre l'errore in autonomia, ogni volta che ne ha bisogno. Puo' provare a cambiare alcuni passi per verificare se il bug si presenta solo in un caso particolare, oppure in una serie di casi simili. Se non e' la vostra giornata fortunata, puo' essere necessario che lo sviluppatore si fermi con voi un paio d'ore per fare un debug in _piena regola_. La cosa piu' importante e' che veda l'errore mentre questo accade. Quello e' il punto di partenza da cui puo' iniziare la correzione del bug.

## "Fammi vedere come riprodurlo."

Questa e' l'era di internet. Questa e' l'era della comunicazione globale. Questa e' l'era in cui io posso inviare il mio software a qualcuno in Russia premendo un semplice un bottone, e lui puo' rispondermi con la stessa facilita'. Ma, se lui ha un problema con il mio programma, _non posso_ certo essere al suo fianco mentre si verifica l'errore. “Fammi vedere” e' un buon metodo quando applicabile ma spesso non e' possibile.

Se dovete segnalare un bug ad un programmatore che non puo' essere fisicamente presente, allora lo scopo principale della segnalazione diventa metterlo in condizione di _riprodurre_ l'errore in autonomia. Il programmatore deve poter riprodurre le stesse condizioni, fare le stesse cose nello stesso modo per ottenere l'errore. Solo quando l'avra' visto con i propri occhi, potra' cercare di risolverlo.

Quindi, raccontate al programmatore cosa avete fatto. Se e' un programma con un interfaccia grafica, ditegli quali pulsanti avete premuto e in quale ordine ( li avete premuti). Se avete eseguito il programma da linea di comando, mostrategli il comando esatto che avete scritto. Quando possibile, fornitegli un elenco delle vostre azioni, mostrategli i comandi che avete eseguito e le risposte fornite dal computer.

Fornite al programmatore tutte le informazioni che vi vengono in mente. Se il programma legge un file, probabilmente dovrete spedirgli una copia del file. Se il programma dialoga con un altro computer in rete, ovviamente non potrete inviargli una copia del computer, ma almeno gli direte che tipo di computer e' e (se possibile) che software e' installato/sta funzionando su quel computer.

## "Per me funziona. Cosa c'e' che non va?"

Se il programmatore, con in mano la lista di informazioni e azioni che gli avete fornito, esegue la sua versione del programma e non accade nulla, vuol dire che non avete fornito sufficienti informazioni. E' probabile che l'errore non avvenga su ogni computer; il vostro computer potrebbe essere differente da quello dello sviluppatore. E' probabile che voi abbiate fraintenso quali sono le funzioni del programma, o che entrambi stiate guardando la stessa cosa e voi pensate ci sia un errore mentre non lo e'.

Descrivete quindi esattamente cosa è successo e cosa avete visto. Ditegli perche' pensate di aver visto un errore o, meglio, cosa vi aspettereste di vedere. Se gli dite semplicemente“e poi si verifica l'errore” allora avete tralasciato di riportare l'informazione piu' importante.

Se notate dei messaggi d'errore riportate anche quelli, con precisione. Sono _molto_ importanti! In questa fase il programmatore non sta cercando di correggere l'errore, sta solo cercando il problema. Il programmatore ha bisogno di sapere cosa non ha funzionato, e quei messaggi d'errore sono quanto di meglio il computer puo' dirvi. Trascrivete gli errori se non avete modo di ricordarli, e vi consiglio di riportare il relativo messaggio d'errore quando segnalate un bug.

Per la precisione, se il messaggio d'errore contiene dei numeri, _fate_ in modo che il programmatore riceva anche quei numeri. Solo perche' il messaggio vi sembra criptico, non significa che non abbia senso. I numeri contengono molti tipi di informazioni utili al programmatore e molto probabilmente contengono indizi importanti. I numeri riportati nei messaggi d'errore sono li perche' il computer non e' in grado di riportare un messaggio completo, ma sta facendo di tutto per fornire tutte le informazioni in suo possesso.

Arrivati a questo punto, il programmatore avra' iniziato l'indagine; non sa ancora cosa sia accaduto e non puo' andare a vederlo di persona, quindi sta cercando un indizio che lo possa aiutare. I messaggi d'errore (parole e numeri incomprensibili), nonche' gli inspiegabili ritardi, sono importanti come le impronte digitali sulla scena del crimine. Teneteli da parte!

Se state usando Unix, il programma puo' generare un core dump. I core dump sono ottime fonti di informazioni, quindi non vanno cancellati. Capita che alcuni programmatori non amino ricevere email con grossi allegati (i core dump, appunto) senza preavviso, quindi e' sempre meglio chiedere prima. Inoltre, fate attenzione perche' i core dump contengono una registrazione completa dello stato del programma: qualsiasi “segreto” incluso (magari il programma stava gestendo un messaggio personale o analizzando dati riservati) puo' essere finito nel code dump.

## "Allora io ho provato . . ."

Ci sono un sacco di cose che potete fare quando incontrate un errore. Molte di queste peggiorano la situazione. Una mia compagna di classe cancello' tutti i suoi documenti Word per errore, e prima di chiedere aiuto ad un esperto, provo' a reinstallare Word, poi esegui' Defrag. Nessuna di queste cose la aiuto' a recuperare i file, e nel frattempo aveva anche esteso il disco fisso cosicche' nessun programma di Undelete avrebbe mai potuto recuperare qualcosa. Se solo non avesse toccato nulla avrebbe avuto qualche possibilita' in più..

Questo genere di utenti sono come una mangusta sotto assedio, quando viene messa all'angolo: con le spalle al muro e colta dal panico, la mangusta va all'attacco insensatamente perche' secondo lei fare qualcosa e' sempre meglio che non far niente. Questo comportamento e' da evitare quando si verificano problemi con i computer.

Invece di essere una mangusta, siate un'antilope. Quando l'antilope si trova di fronte ad un problema, si blocca. Sta completamente immobile, cerca di non attirare l'attenzione e, nel frattempo, pensa alla cosa migliore da fare. (In questo istante l'antilope sarebbe al telefono con il suo supporto tecnico, se solo ne avesse uno). Solo allora, quando l'antilope ha deciso quale sia la soluzione piu' sicura, agisce.

Se qualcosa va male, _fermatevi_. Non toccate nessun pulsante. Guardate lo schermo e osservate qualsiasi anomalia e memorizzatela, oppure trascrivetela. Solo allora forse potrete premere “OK” o “Annulla”, o almeno quella che vi sembra piu' sicura. Cercate si seguire un percorso sensato – se il computer si comporta in maniera inaspettata, allora non fate nulla.

Se proseguite con l'intenzione di risolvere il problema, chiudendo il programma oppure riavviando il computer, una buona cosa e' di cercare di ricreare nuovamente il problema. Ai programmatori piacciono i problemi che si possono riprodurre piu' volte. Se i programmatori sono felici allora correggono bug piu' velocemente e piu' efficacemente.

## "Credo che la modulazione dei tachioni non sia correttamente polarizzata."

Non pensiate che siano solo i non-esperti a fare pessime segnalazioni. Alcune delle peggiori che io abbia mai visto venivano proprio da programmatori, e alcuni di loro erano persino ottimi programmatori.

Una volta lavorai con un sviluppatore, che continuava a correggere bug nel suo codice, bug che lui stesso trovava. Capitava che spesso incontrasse dei bug che non riusciva a risolvere, e quindi mi chiamava perche' lo aiutassi.“Cosa c'e' che non va?” gli chiedevo, e lui mi rispondeva raccontandomi la sua idea su come correggere quel bug.

Questo funzionava bene quando le sue idee erano corrette, cioe' quando lui aveva gia' fatto meta' del lavoro da solo, cosi' potevamo completare il lavoro assieme. Quel modo di lavorare era efficiente e utile.

Spesso, però, questo metodo non funzionava. Capitava che cercassimo di capire perche' una (particolare) parte del programma non facesse il proprio dovere, poi scoprivamo che non era cosi, e che per mezz'ora avevamo analizzato una parte del codice che funzionava perfettamente mentre il vero problema stava altrove.

Sono sicuro che non fareste mai una cosa del genere con un medico. “Dottore, mi prescriva l' Hydroyoyodyne”. Tutti sappiamo che non dobbiamo comportarci in questo modo con un medico: innanzitutto bisogna descrivergli i sintomi, gli indolenzimenti, i dolori e tutto il resto, e lasciare che il dottore faccia la sua diagnosi e ci dica la cura. Altrimenti, il dottore vi potrebbe considerare un ipocondriaco, un pazzo o giu' di li.

Stesso dicasi per i programmatori. Fornir loro la vostra diagnosi a volte puo' essere utile, ma piuttosto fornite i sintomi, ogni volta. La diagnosi e' un optional, e non una alternativa ai sintomi. Stesso dicasi quando mandate la correzione del codice assieme alla segnalazione del bug, anche in questo caso non e' da considerarsi un sostituto.

Se il programmatore ha bisogno di altre informazioni, non tagliate corto. Tempo fa qualcuno mi segnalo' un bug, alche' gli chiesi di provare un comando che sapevo gia' essere non funzionante. Il motivo per cui gli chiesi di provare quel comando era di sapere quale dei 2 messaggi di errore venivano restituiti. Conoscere il messaggio d'errore era un ottimo indizio. Ma lui nemmeno ci provo' e mi rispose “No, non funziona.”. Mi ci e' voluto un bel po per convincerlo.

Utilizzate tutto il vostro buon senso per aiutare lo sviluppatore. Anche se le vostre ipotesi sono sbagliate, lo sviluppatore vi sara' grato del fatto che _state cercando_ di semplificargli la vita. Segnalate sempre e comunque i sintomi, altrimenti gli renderete la vita piu' difficile.

## "Che strano, un attimo fa non ha funzionato."

Provate a dire ad un programmatore “Errore casuale”e guardate che faccia fa. I problemi piu' facili sono quelli che generano l'errore con una semplice sequenza di azioni. Lo sviluppatore puo' quindi riprodurre quelle operazioni in un ambiente controllato e guardare cosa succede all'interno. Un sacco di bug, purtroppo, non sono di questo tipo: ci sono errori che si presentano una volta alla settimana oppure una volta al mese, oppure non si presentano mai quando lo sviluppatore e' al vostro fianco ma si presentano quando siete prossimi ad una scadenza.

Molti errori casuali non sono poi così casuali.La maggior parte di loro, in realta', ha un senso. Alcuni si verificano quando la memoria si sta esaurendo, altri quando un diverso programma cerca di modificare un file vitale nel momento sbagliato, altri ancora si presentano solo nella prima mezz'ora di ogni ora. (Ho veramente assistito ad uno di questi casi)

Inoltre, se lo sviluppatore non riesce a riprodurre l'errore mentre voi ci riuscite, e' molto probabile che i vostri computer siano differenti e questo sia il motivo del verificarsi del problema. In passato usavo un programma la cui finestra si richiudeva in un piccolo riquadro nell'angolo in alto a sinistra dello schermo e rimaneva li bloccata. Questo accadeva solo con la risoluzione 800x600 ma non con il mio monitor a 1024x768.

Gli sviluppatori vogliono sapere qualsiasi cosa a riguardo del problema. Verificate il problema su un altro computer, se potete. Provatelo 2 o 3 volte e controllate quando si presenta l'errore. Se l'errore si presenta solo quando lavorate veramente, e non quando state cercando di provocare l'errore, allora l'errore potrebbe dipendere dal fatto che lavorate per un lungo tempo oppure ai grossi file che vengono generati. Cercate di individuare quanti piu' dettagli possibili e cosa stavate facendo quando si e' presentato l'errore, inoltre segnalate qualsiasi fatto strano. Qualsiasi indicazione che potete fornire puo' essere d'aiuto. Persino informazioni di tipo probabilistico (esempio “tende a saltare piu' spesso quando Emacs e' in funzione”), anche se non forniscono un indizio direttamente legato al problema, possono aiutare lo sviluppatore a riprodurlo.

La cosa piu' importante per un programmatore, e' sapere se sta analizzando un errore casuale oppure direttamente legato al computer. Gli sviluppatori vogliono sapere un sacco di cose sulla configurazione del vostro computer, cosi' possono capire cosa cambia rispetto al loro computer. Molti di questi dettagli derivano dal programma in oggetto, ma c'e' una cosa che bisogna sempre sapere: la versione del programma. Non solo la versione del programma, anche quella del sistema operativo e quella degli altri programmi coinvolti nel problema.

## "Allora ho caricato il dischetto nel mio Windows . . ."

E' importante riportare una segnalazione con molta chiarezza. Se il programmatore non riesce a capire cosa intendete, è come se non aveste detto nulla..

Io ricevo segnalazioni di errori da tutto il mondo. Molte di queste segnalazioni provengono da persone che non sono di madrelingua inglese, e molti di loro si scusano per il loro inglese. In generale, le segnalazioni da non madrelingua inglese sono in realta' molto chiare e utili. La maggior parte delle segnalazioni poco chiare provengono da madrelingua inglese che credono che io li capisca in ogni caso, anche se non fanno alcuno sforzo per essere chiari e precisi.

*   _Siate precisi_. Se potete fare la stessa cosa in 2 modi, precisate quale avete seguito. “Ho selezionato APRI” potrebbe significare “Ho cliccato su APRI” oppure “Ho premuto Alt-L”. Specificate cosa avete fatto. Qualche volta sta proprio lì il problema.
*   _Siate esaustivi_. Date piu' informazioni possibile. Se riportate troppe informazioni, il programmatore puo' tralasciarne alcune. Se ne riportate poche, il programmatore dovrà contattarvi per chiedervi ulteriori dettagli. Una volta ho ricevuto una segnalazione d'errore che consisteva in una sola frase: ogni volta che chiedevo maggiori informazioni, l'utente mi rispondeva con una singola frase.In questo modo, ho impiegato diverse settimane per ottenere le informazioni necessarie.
*   _Non esagerate con i pronomi_. Non usate frasi come “l'ho chiusa!”, oppure far riferimenti generici come “la finestra”, quando non e' chiaro a cosa vi riferite. Considerate questa frase:”Ho eseguito l'applicazione FooApp. Ho visto la finestra con il messaggio d'errore. Ho provato a chiuderla ma e' andata in crash”. In questo esempio non e' chiaro cosa l'utente ha provato a chiudere la finestra con il messaggi d'errore, oppure tutta l'applicazione. C'e' una bella differenza. Proviamo con questa frase:”Ho eseguito l'applicazione FooApp, ed è comparsa la finestra con il messaggio d'errore. Ho cercato di chiudere la finestra d'errore e l'applicazione FooApp e' andata in crash.” Questa frase e' sicuramente piu' lunga e piu' ripetitiva, ma anche piu' chiara ed e' piu' difficile che sia fraintesa.
*   _Leggete cosa avete scritto_. Leggete voi stessi la segnalazione e verificate che sia tutto chiaro. Se avete elencato una sequenza di azioni per riprodurre il problema, cerca di ripeterla voi stessi, per vedere se avete dimenticato qualcosa.

## Conclusioni

*   Lo scopo principale della segnalazione di un bug e' far si che lo sviluppatore possa vedere gli errori con i propri occhi. Se non riesce a riprodurre l'errore direttamente, bisogna fornirgli tutte le informazioni necessarie affinche' lo possa riprodurre da solo.
*   Se lo scopo principale _non_ viene raggiunto, allora bisogna descrivete l'errore. Riportate tutto nel dettaglio. Descrivete cosa avete visto ed anche cosa vi aspettavate di vedere. Trascrivete i messaggi d'errore, _specialmente_ se contengono dei numeri.
*   Quando il vostro computer fa qualcosa di inaspettato, _bloccatevi_. Non fate nulla finche' non vi siete calmati, e non fate niente che pensiate possa crear danno.
*   Cerca di capire l'errore se credete di poterlo fare, ma se lo fate, devete riportare comunque tutti i segnali dell'errore.
*   Siate pronti a fornire informazioni aggiuntive se lo sviluppatore le richiede. Se non fosse necessario, gli sviluppatori non lo farebbero. Tenete a portata di mano le versioni dei programmi, perche' lo sviluppatore ve le chiedera'.
*   Scrivete chiaramente. Dite cosa intendete, e siate sicuri che non possano esserci fraintendimenti.
*   Soprattutto, _siate precisi_. Gli sviluppatori preferiscono la precisione.

* * *

_Avviso:_ confesso che non ho mai visto una mangusta oppure una antilope. Le mie conoscenze naturalistiche possono non essere precise.