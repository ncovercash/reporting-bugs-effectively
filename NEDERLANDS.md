# Effectief softwarestoringen melden

_door Simon Tatham, ontwikkelaar van professionele en vrije software_

## Inleiding

Iedereen die software voor algemeen gebruik ontwikkelde heeft minstens één nietszeggend storingsrapport ontvangen ("hij doet 't niet!"); rapporten die geen hout snijden; onvolledige of _verkeerde_ informatie geven; Rapportering van problemen die een fout gebruik of fouten van een ander(mans) programma zijn; rapportering van problemen die door een ondeugdelijk netwerk zijn veroorzaakt.

Er is een reden waarom technische ondersteuning als een vreselijke baan wordt beschouwd en deze reden is verkeerde foutenrapportages. Niet alle foutmeldingen zijn echter onplezierig. Ik onderhoud vrije software wanneer ik niet mijn brood verdien en af en toe krijg ik wonderbaarlijk heldere, behulpzame en _informatieve_ storingsrapporten binnen.

In dit document zal ik duidelijk maken wat een goede foutenrapportage inhoudt. Idealiter had ik graag dat iedereen ter wereld voordat hij of zij een fout aan iemand meldt deze pagina ter harte neemt. Zeker zou ik wensen dat ze dat doen voor ze er één naar _mij_ sturen.

In een notendop, het doel van een foutenrapport is de ontwikkelaars in staat stellen de programmafouten voor zich te zien. U kunt ze persoonlijk tonen of zorgvuldige en gedetailleerde aanwijzigingen geven op welke wijze het programma mislukt. Als dat inderdaad het geval is kunnen ze zelf extra informatie verkrijgen totdat de oorzaak boven water komt. Zo niet zal men die informatie van u verlangen.

Geef in foutenrapporten heel duidelijk aan wat er feitelijk aan de hand was ("Ik zat achter de computer en toen gebeurde dit") en wat u aanneemt ("Ik _denk_ dat dit het probleem zou kunnen zijn"). Aannames kunt u desgewenst weglaten, maar vermeld de feiten.

U meldt een fout, omdat u die op wil laten lossen. Schelden op de ontwikkelaars is zinloos of op zijn minst onbeholpen: het kan wel hun schuld en uw probleem zijn en u kunt terecht kwaad op hen zijn, maar de storing is sneller opgelost als u hen alle nodige informatie verstrekt. Onthoud ook dat als programma's gratis zijn de auteurs ze leveren uit aardigheid. Daar komt een einde aan als te veel mensen ze onheus bejegenen.

## "Hij doet 't niet!"

Geef de programmeur wat krediet voor basisintelligentie: als het programma helemaal niet werkt hadden ze dat waarschijnlijk al gemerkt. Aangezien dat niet het geval is moet het bij hen gewerkt hebben. Daarom hebt u iets anders gedaan of u werkt in een andere omgeving dan zij. Ze hebben informatie nodig; het verstrekken van die informatie is het doel van een foutenverslag. Het verslag is beter naarmate het meer informatie bevat.

Veel programma's en de gratis exemplaren in het bijzonder, publiceren een lijst met bekende tekortkomingen (Engels: "buglist" of iets wat daar op lijkt). Als u zo'n lijst aantreft loont het de moeite deze door te nemen om te zien of de door u geconstateerde fout daar op staat en dan is het niet handig deze opnieuw te melden, maar bent u van mening iets toe te kunnen voegen aan de foutenlijst, neem dan wel contact op met de ontwikkelaars, zodat ze dankzij extra informatie de fout gemakkelijker op kunnen lossen, aangezien ze die informatie voorheen wellicht nog niet hadden.

Deze verhandeling staat vol met richtlijnen.. Geen enkele is een wet van Meden en Perzen. Elke ontwikkelaar heeft een eigen voorkeur voor de wijze waarop een fout gemeld wordt. Als storingsmeldrichtlijnen meegeleverd zijn, lees ze en volg ze, ook als ze deze tegenspreken!

Wanneer u alleen hulp in het gebruik verlangt geef aan waar u al gezocht hebt (bij voorbeeld: In hoofdstuk 4 en paragraaf 5.2, maar daar stond het niet"). Zo maakt u de ontwikkelaars duidelijk waar u e.e.a. verwacht, zodat ze eventueel de documentatie daarop kunnen aanpassen

## "Toon me."

Een van de beste manieren om een fout te melden is deze zichtbaar te maken voor de ontwikkelaars. Zet ze bij uw computer, start hun software and demonstreer wat er mis gaat. Start de machine waar ze bij staan, laat ze op uw vingers kijken hoe u met het programma omgaat en toon de reactie van hun geesteskind op uw commando's.

Zij kennen de software op hun duimpje. Zij weten de betrouwbare gedeeltes en de wat zwakkere punten. Zij weten intuïtief waar ze op moeten letten. Tegen de tijd dat het programma echt uit de bocht vliegt herkennen zij signalen die een hint zijn dat er iets een _beetje scheef zit._ Zodoende kunnen ze alles zien wat de computer gedurende deze test doet en daar voor hen belangrijke gebeurtenissen uit destilleren.

Misschien is dit nog niet genoeg en verlangen ze meer informatie. Dan kunnen ze u vragen hetzelfde nogmaals uit te voeren en hen dan door de procedure heen te praten, zodat ze de fout net zo vaak kunnen reproduceren als ze willen. Ze zouden de procedure een paar keer willen varieren om te zien of het onder specifieke voorwaarden voorlomt of in een serie gerelateerde omstandigheden. Als u pech hebt blijven ze een paar uur zitten met een batterij ontwikkeltools en gaan ze daarmee _echt op onderzoek uit._ Het belangrijkste is dat de programmeur naar de computer kijkt wanneer het fout gaat. Wanneer ze eenmaal het probleem hebben zien optreden kunnen ze van daaruit een begin maken met het zoeken naar een oplossing.

## "Toon me hoe mezelf te presenteren."

Dit is het Internettijdperk. Dit is het tijdperk van wereldwijde communicatie. In dit tijdperk kan ik mijn software naar iemand in Rusland sturen met één druk op de knop en deze kan net zo simpel commentaar leveren. Als hij een probleem heeft met mijn programma kan hij _niet_ bij me staan terwijl het mislukt. "Toon me" is goed als het kan, maar dikwijls kan het niet.

Als u een fout moet melden aan programmeurs die niet lijfelijk aanwezig kunnen zijn is het de kunst ze in staat te stellen de onvolkomenheid te _reproduceren_. U wil dat de ontwikkelaars hun eigen exemplaar dezelfde dingen laten doen op gelijke wijze mis laten lopen. Wanneer ze het probleem voor ogen zien kunnen ze actie ondernemen.

Vertel ze exact wat u deed. Als het een grafisch programma is, zeg welke knoppen u in welke volgorde indrukte. Als het programma door middel van het typen van commando's werkt, schrijf precies welk(e) commando(s) u typte. Voeg zo mogelijk een letterlijk verslag van de sessie bij, waarin te lezen is wat de antwoorden op welke commando's waren.

Geef de ontwikkelaar alle denkbare invoer. Als het programma een bestand leest, is het vaak nodig een kopie van dit bestand mee te sturen. Wanneer de computer via een netwerk met een andere computer in verbinding staat kunt u weliswaar geen kopie van die computer meesturen, maar geef op z'n minst aan wat voor soort computer het is en (als u dat weet) met welke (systeem)software/besturingssysteem deze is uitgerust.

## "Werkt bij mij. Dus wat gaat er mis?"

Als u de ontwikkelaars een lange lijst met invoer en acties geeft en zij zetten hun exemplaar aan het werk en er gaat niets fout dan heeft u niet genoeg informatie verstrekt. Misschien treedt de fout niet op elke computer op, is uw systeem een beetje anders dan die van hen. Misschien had u een ander idee van wat het programma zou behoren te doen, ziet u beide hetzelfde, maar denkt u dat het fout is en weten zij dat het goed is.

Geef dus ook aan wat er gebeurde. Vertel ze exact wat u zag. Zeg ze waarom u denkt dat wat u zag verkeerd is; nog beter wat u verwachtte te zien. Als u zegt "en toen ging het mis" heeft u essentiële informatie achtergehouden.

Als u foutmeldingen zag, vertel dan zorgvuldig en precies aan de programmeurs welke dat waren. Ze _zijn van belang_! Op dit moment is de programmeur nog niet bezig het probleem te herstellen, alleen maar te lokaliseren. Ze moeten weten wat er fout ging en de foutboodschappen zijn het beste wat de computer kan doen om u op de hoogte te brengen. Schrijf de fouten op als u geen andere gemakkelijke manier hebt om ze te kunnen onthouden, maar het getuigt van weinig waarde een fout te melden zonder te vermelden met welke foutmeldingen de computer zelf kwam.

In het bijzonder, als de foutboodschap getallen bevat _lever_ deze aan de ontwikkelaars. Omdat u de betekenis niet inziet betekent dat niet dat deze er niet is. Getallen bevatten een schat aan informatie voor de ontwikkelaars en zijn vaak van onschatbare waarde in het zoeken naar de oorzaak en/of locatie van een probleem. Getallen staan in foutmeldingen, omdat de computer te veel bezig is met andere dingen om de melding in woorden te leveren, maar doet toch zijn best om u en de programmeurvan essentiële informatie te voorzien.

Nu gaat de ontwikkelaar met effectief onderzoekswerk aan de slag. Ze weten niet wat er gebeurde en kunnen niet dicht genoeg bijkomen om het gebeuren met eigen ogen te zien dus zoeken ze naar aanwijzingen om het duidelijk te krijgen. Foutboodschappen, onbegrijpelijke rijen getallen en zelfs onverklaarde wachttijden zijn net zo belangrijk als vingerafdrukken op de plaats van een misdrijf. Hou ze in ere!

Als u Unix gebruikt is er een kans dat het programma de inhoud van het geheugen in een bestand (core) heeft gezet, dus gooi ze niet weg. Deze bestanden zijn aan de ene kant een bijzondere bron van aanwijzingen, aan de andere kant hebben de meeste programmeurs er een hekel aan als zonder een waarschuwende e-mail vooraf vreselijk lijvige 'core dumps' in hun postbus vinden. Stuur dus eerst een mailtje of het goed is dat u er één stuurt. Realiseer u ook dat het gehele computergeheugen er in staat met de volledige "geheime" status van het programma inclusief eventueel vertrouwelijke gegevens.

## "En toen probeerde ik . . ."

Er zijn veel dingen die u zou kunnen doen als een verstoring optreedt. Veel daarvan maken het alleen maar erger. Een klasgenote van mij wiste per ongeluk al haar Word-documenten en voordat ze een expert inschakelde installeerde ze Word opnieuw en startte het defragmentatie programma. Geen van beide herstelde de bestanden. Integendeel haar schijf is zodanig gereorganiseerd dat geen 'ontwisprogramma' op aarde nog iets kon betekenen om de documenten te redden. Als ze de boel met rust gelaten had was daar misschien nog kans op geweest.

Klanten als deze zijn als een stokstaartje in een hoekje: met de rug naar de muur, de dood in de ogen valt-ie zenuwachtig aan, omdat iets doen altijd beter is dan afwachten. Dat is niet van toepassing op computerproblemen.

In plaats van als een stokstaartje, reageer als een antilope. Wanneer een antilope iets onverwachts of engs constateert houdt hij zich gedeisd. Houdt zich volledig stil en vermijdt alle aandachttrekkerij. Dat is het beste wat men doen kan (Stel antilopes hadden technische ondersteuning dan zouden ze deze hulp in zo'n geval inroepen) Dan, eenmaal besloten wat het veiligst is, dan doen ze dat.

Wanneer iets mislukt, houd onmiddellijk op ook maar _iets_ te doen. Blijf van alle knoppen af. Kijk naar het scherm en merk alle vreemde zaken op, onthoud ze of schrijf ze op. Daarna voorzichtig misschien op 'OK' of 'Annuleren' klikken, welke van de twee volgens uw intuïtie het veiligst lijkt. Ontwikkel een reflectieve reactie - als een computer iets onverwachts doet - houd u gedeisd.

Als het u lukt uit de problemen te komen, hetzij door het geraakte programma af te sluiten, danwel de computer te herstarten, dan is het goed dit nog eens te laten gebeuren.Programmeurs zijn dol op terugkerende problemen. Vrolijke ontwikkelaars verhelpen storingen sneller en efficiënter.

## "Ik denk dat de tachyonmodulatie reversief gepolariseerd is."

Het zijn niet alleen niet-programmeurs die slechte foutenmeldingen samenstellen. Enkele van de slechtste die ik ooit zag kwamen van ontwikkelaars en zelfs van goede programmeurs.

Ik werkte ooit met een andere ontwikkelaar, die steeds fouten in zijn eigen code vond en deze trachtte te verhelpen. Eens in de zoveel tijd vond hij een fout die hij niet op kon lossen en dan mij om raad vroeg. "Wat ging er mis?" vroeg ik. Hij zou antwoorden door mij zijn huidige mening te geven over wat er gerepareerd diende te worden.

Dit werkte voor die gevallen waar de mening correct was. Dit hield in dat het werk half af was en we het karwei samen zouden kunnen klaren. Efficiënt and nuttig.

Nogal vaak had hij het bij het verkeerde eind. We wildende voor een tijdje ons best doen om uit te zoeken waarom een bepaald deel van het programma onjuiste gegevens leverde en eventueel zouden we tot de ontdekking dat we gedurende een half uur een perfect stukje programmatuur onder de loupe hadden en het eigenlijke probleem zich elders bevond.

Ik weet zeker dat hij tegen een arts anders zou zijn. "Dokter, Ik wil graag een recept voor Hydroyoyodyne." Mensen weten niet wat ze tegen een arts moeten zeggen: U beschrijft de symptomen, de werkelijke ongemakken, kwalen, pijnen, uitslag en koorts en laat de diagnose wat er aan de hand is en wat er tegen te doen aan de geneesheer over. Anders stuurt de dokter u weg als hypochonder of simulant en terecht.

Dat is met ontwikkelaars net zo. Uw eigen diagnose stellen mag dan soms helpen, maar beschrijf altijd de symptomen. De diagnose is een optie bij, maar geen alternatief voor het geven van symptomen. Evenzo is het sturen van gewijzigde code ter herstel van het probleem een nuttige toevoeging, maar geen afdoende vervanging.

Als een programmeur u meer informatie vraagt, verzin die dan niet! Iemand meldde mij een keer een storing en ik vroeg hem een commando te proberen waarvan ik wist dat-ie niet zou werken. Ik vroeg dat, omdat ik wilde weten welke van twee verschillende foutboodschappen er zou komen. Eenmaal bekend met de foutmelding zou een essentiële aanwijzing opleveren. Hij probeerde het echter niet in werkelijkheid - hij mailde mij slechts het volgende terug: "Nee, dat zal niet werken". Ik had enige tijd nodig hem te overtuigen het wel te proberen.

Uw verstand gebruiken om de programmeur te helpen is prima. Zelfs als uw redenering niet klopt zullen de ontwikkelaars blij zijn dat u uw best heeft gedaan hun leven te veraangenamen, maar geef ook de symtomen weer of u loopt goede kans dat u het hen inplaats daarvan moeilijker maakt

## "Dat is raar, net deed-ie het nog."

Zeg "onderbroken fout" tegen een willekeurige ontwikkelaar en zie zijn gezicht betrekken. Het zijn eenvoudige problemen waar een simpele serie acties de fout laten optreden. De programmeur kan die acties dan herhalen onder nauwgezette testomstandigheden en kijken tot in detail kijken wat er gebeurt. Te veel problemen werken eenvoudigweg niet zo: er zullen programma's wekelijks stuklopen of eens in de zoveel tijd of nooit wanneer de ontwikkelaar er naar staat te kijken, maar altijd als de opleveringsdatum nadert.

De meeste onderbroken fouten zijn niet echt onderbroken. De meeste zijn ergens logisch verklaarbaar. Sommige kunnen voorkomen wanneer het geheugen volloopt, andere wanneer een ander programma een kritisch bestand wil veranderen.weer andere alleen in de eerste helft van een uur (Zo een heb ik echt meegemaakt.)

Ook als u de bug kunt reproduceren, maar de ontwikkelaars niet, zou het heel goed kunnen dat er verschil zit tussen hun en uw computer en dat dit verschil de oorzaak is van het probleem.. Er was eens een programma wier venster verkleinde tot een balletje en bleef steken in de linkerbovenhoek van het scherm. Dit gebeurde uitsluitend op 800x600 schermen; ging prima op mijn 1024x768 monitor.

De programmeur zal alles wat u over het probleem kunt vinden willen weten Probeer het uit op een andere machine Probeer het twee, die keer en kijk hoe vaak het mislukt. Als het fout gaat wanneer u serieus bezig bent en wanneer u het wilt demonstreren dan zouden lange draaitijden of grote bestanden mogelijkerwijs het programma laten ontsporen. Probeer zo veel mogelijk details te onthouden over wat u aan het doen was toen het mis ging en als u patronen herkent noem die. Alles wat kunt leveren kan van pas komen. Zelfs als het slechts mogelijkerwijze (zoals "'t neigt meer te klappen wanneer Emacs draait") is, zal het misschien niet direct aanwijzigingen opleveren, maar toch behulpzaam zijn bij het reproduceren.

Het belangrijkste is dat de ontwikkelaars zekerheid willen of hier sprake is van een echte onderbroken fout of een machine-afhankelijke. Zij zullen een heleboel details van uw computer willen weten zo dat ze uit kunnen zoeken in hoeverre deze van de hunne verschilt. Veel van deze details hebben realties met een specifiek programma, maar één ding dat u echt zou moeten ophoesten is zijn versienummers. Het versienummer van het onderhavige programma, het besturingssysteem en waarschijnlijk die van andere programma's die aan het probleem zijn gerelateerd.

## "Dus laadde ik de disk in mijn vensters . . ."

Heldere taal is essentieel in een foutenrapport. Als de programmeur niet kan zeggen wat u bedoelde hebt u vast niet veel gezegd.

Ik krijg storingsmeldingen uit de hele wereld. Veel daarvan komen van mensen die Engels niet als moedertaal hebben en velen bieden hun verontschuldiging aan voor hun slechte Engels. In het algemeen zijn de rapporten met verontschuldigingen eigenlijk zeer helder en nuttig. Alle onduidelijk rapporten komen van Engelstaligen die er van uit gaan dat ik hen begrijp ook al doen ze niet hun best klip en klaar te zijn.

*   _Wees specifiek_. Als u hetzelfde kan doen op twee verschillende manieren, zeg welke u gebruikte. "Ik koos Laad"zou kunnen betekenen "ik klikte op Laad" of "ik typte Alt-L" hetgeen u deed. Soms maakt dat wat uit.
*   _Wees uitgebreid_. Geef bij voorkeur te veel informatie dan te weinig. Als u te veel zegt kunnen de ontwikkelaars wat negeren. Wanneer u te weinig zegt moeten ze weer aankloppen voor aanvullende gegevens. Een foutenverslag dat ik kreeg bestond uit een enkele regel; telkens wanneer ik weer een vraag stelde gaf de verlaggever een ander eenregelig antwoord. Het nam verscheidene weken in beslag voor ik een nuttige hoeveelheid informatie bezat, omdat het met 1 regel tegelijk binnen kwam.
*   _Wees voorzichtig met voornaamwoorden_. Vermijd woorden als "het" of verwijzingen als "het venster" wanner niet duidelijk blijkt waar ze op slaan. Beschouw dit:: "Ik startte BlaApp. Het zette een waarschuwingsvenster in beeld. Ik probeerde het te sluiten en het klapte." Het is niet helder wat de gebruiker wilde sluiten. Het waarschuwingsvenster of de totale BlaApp? Daar zit verschil tussen. In plaats daarvan zou u kunnen melden: "Ik startte BlaApp, die een waarschuwingsvenster in beeld bracht. Ik probeerde dit waarschuwingsvenster te sluiten en BlaApp klapte." Dit is langer en repeterender, maar tevens helderder en minder vatbaar voor misverstanden.
*   _Lees wat u schreef_. Lees het verslag voor u zelf na en kijk of _u_ denkt dat het duidelijk is. Als u een serie acties hebt opgesomd die de fout teweeg zouden brengen probeer ze voor uzelf te volgen om na te gaan of u geen stap hebt overgeslagen.

## Samenvatting

*   Het eerste doel van een foutenverslag is de programmeurs de fout met eigen ogen te laten zien. Als dat niet lijfelijk kan, geef ze dan gedetailleerde instructies hoe ze deze mislukking bij zichzelf kunnen naspelen.
*   In het geval dat het eerste doel niet slaagt en de programmeurs zijn _niet in_ staat de fout voor zichzelf te reproduceren is het tweede doel van een foutenverslag et beschrijven van hetgeen verkeerd liep.Beschrijf alles tot in de puntjes. Leg cast wat u zag and vermed tevens wat u verwachtte te zien. Schrijf de foutmeldingen op, _vooral_ als er getallen in staan. Wanneer uw computer iets onverwachts doet, _houd u gedeisd_. Doe niets totdat u tot rust gekomen bent en doe zeker niet iets waarvan u denkt dat het riskant zou kunnen zijn. Probeer in ieder geval de fout voor uzelf te diagnosticeren als u daar toe in staat denkt te zijn, maar als u dat doet stuur dan toch het verslag op met daarin ook de symptomen. Wees bereid de ontwikkelaars van alle gewenste informatie te voorzien. Als ze het niet nodig hadden zouden ze er niet om vragen. Ze doen niet met opzet vervelend. Houd versienummers bij de hand, omdat ze die waarschijnlijk nodig hebben. Schrijf helder. Zeg wat u bedoelt en verzeker u ervan dat het niet verkeerd begrepen kan worden.
*   Boven alles, _wees precies_. Programmeurs houden van precisie.

* * *

_Vrijwaring_: Ik ben nog nooit een stokstaartje of antilope in het wild tegengekomen. Mijn dierkunde kan onnauwkeurig zijn