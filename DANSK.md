# Sådan rapporterer man fejl effektivt

_af Simon Tatham, professionel og fri software programmør_

## Introduktion

Enhver som har skrevet software til offentlig brug har sikkert modtaget mindst en dårlig fejlrapport. Rapporter der ikke siger noget ("Det virker ikke!"); rapporter der ikke giver mening; rapporter der ikke giver nok information; rapporter der giver _forkert_ information. Fejlrapporter der viser sig at være brugerfejl; rapporter om fejl der viser sig at være et andet programs fejl; rapporter om problemer der viser sig at være netværksfejl.

Der er en grund til at teknisk support anses for at være en forfærdelig branche at være i, og den grund er dårlige fejlrapporter. Men ikke alle fejlrapporter er ubehagelige: Jeg vedligeholder fri software, når jeg ikke tjener til føden, og nogle gange modtager jeg vidunderligt klare, hjælpsomme, _informative_ fejlrapporter.

I dette essay vil jeg prøve klart at formulere hvad der skal til i en god fejlrapport. Ideelt set ville jeg ønske at alle i verden læste dette essay før de rapporterer fejl til nogen som helst. Jeg ville i hvert fald ønske at alle som rapporterer fejl til _mig_ havde læst det.

I en nøddeskal er målet for en fejlrapport at gøre programmørerne i stand til at se programmet fejle foran sig. Du kan enten vise det personligt, eller give omhyggelige og detaljerede instruktioner i hvordan man får fejlen frem. Hvis de kan få fejlen frem selv, vil de prøve at samle yderligere information indtil de kender årsagen. Hvis de ikke kan få fejlen til at ske selv, bliver de nød til at bede dig om at samle denne yderligere information for dem.

Prøv at gøre det meget klart i en fejlrapport, hvad der er egentlige fakta ("Jeg sad ved computeren og dette er hvad der skete") og hvad der er dine egne teorier ("Jeg _tror_ problemet måske er dette"). Udelad teorierne hvis du vil, men udelad aldrig fakta.

Når du rapporterer en fejl så gør du det fordi du gerne vil have fejlen rettet. Der er ingen idé i at svine programmørerne til eller være overlagt uhjælpsom; det kan være at det er deres fejl og dit problem, og det kan være du måske har ret til at være sur på dem, men fejlen bliver rettet hurtigere hvis du hjælper ved at give dem al den information de har brug for. Husk også at hvis programmet er frit så har forfatterne ofte gjort det frit ud af venlighed og hvis folk er ubehøvlede over for dem kan det være det holder op med at være venlige.

## "Det virker ikke."

Gå ud fra at programmørerne ikke er helt uintelligente: hvis programmet virkelig slet ikke virkede, så ville de sandsynligvis have opdaget det. Da de ikke har det, så virker det for dem. Det vil sige, enten gør du noget andet end de gør eller også er dit miljø anderledes end deres. De har brug for information; at give denne information er formålet med en fejlrapport. Mere information er altid bedre end mindre.

Mange programmer, specielt frie, offentliggør en liste over kendte fejl. Hvis du kan finde en liste over kendte fejl er det værd at læse den for at se om den fejl du lige har fundet allerede er kendt eller ej. Hvis den allerede er kendt, så er det sandsynligvis ikke nødvendigt at rapportere den igen, men hvis du mener du har mere information end der allerede står i fejllisten så har du måske lyst til at kontakte programmørerne alligevel. De kan måske rette fejlen nemmere hvis du giver dem information de ikke havde i forvejen.

Dette essay er fuld af retningslinier. Ingen af dem er ufravigelige regler. Hver programmør har sin foretrukne måde at modtage fejlrapporter på. Hvis programmet har sine egne fejlrapporteringsprocedurer: læs dem. Hvis retningslinierne modsiger hvad dette essay siger så følg programmets!

Hvis du ikke rapporterer en fejl, men bare spørger om hjælp til at bruge programmet, så bør du angive hvor du har kigget efter løsninger til dit problem. ("Jeg kiggede i kapitel 4 afsnit 5.2, men kunne ikke finde noget om dette er muligt eller ej.") Når du gør dette viser du programmørerne hvor du forventede at finde svaret, så de kan gøre dokumentationen nemmere at bruge.

## "Vis mig hvordan."

En af de allerbedste måder du kan rapportere en fejl er ved at vise programmøren hvordan den opstår. Stil dem foran din computer, start deres program og demonstrér det der går galt. Lad dem følge med mens du starter maskinen, mens du starter programmet, i hvordan du bruger programmet og i hvad programmet gør når du bruger det.

De kender programmet som deres egen bukselomme. De véd hvilke dele de stoler på og de véd hvilke dele der sandsynligvis er problemer med. På det tidspunkt hvor programmet gør noget indlysende forkert har de måske allerede tidligere opdaget noget _småt_ der er forkert, som kan give dem en ledetråd. De kan se alt computeren gør undervejs, og selv sortere de ligegyldige informationer fra.

Det kan være det ikke er nok. Det kan være de beslutter at de har brug for mere information og beder dig om at vise det samme en gang til. Det kan være de beder dig om at forklare hvad de skal gøre, så de selv kan genskabe fejlen så mange gange de har lyst til. Det kan være de prøver små variationer af fremgangsmåden for at se om problemet kun sker i nogle nært beslægtede tilfælde. Hvis du er uheldig er det måske nødvendigt at de sætter sig ned i nogle timer med forskellige udviklingsværktøjer for _virkelig_ at fejlsøge. Under alle omstændigheder er det vigtigste at programmørerne ser maskinen når fejlen sker. Når de kan se problemet ske, kan de som oftest tage det som udgangspunkt når de skal rette fejlen.

## "Vis mig hvordan jeg kan vise mig selv hvordan."

Vi lever i internettets æra. Den internationale kommunikations æra. I denne æra kan jeg sende mit program til en Rusland med et tryk på en knap og han kan sende mig kommentarer om det lige så nemt. Men hvis han har et problem med mit program, så kan han _ikke_ få mig til at stå foran hans computer mens fejlen sker. "Vis mig hvordan" er godt når det er muligt, men det er det ofte ikke.

Hvis du skal rapportere en fejl til programmører som ikke kan være til stede personligt så er målet med øvelsen at gøre det muligt for dem at _genskabe_ problemet. Du ønsker at programmørerne kører deres egne udgaver af programmet, gør det samme ting som du gør og får det til at lave fejl på samme måde. Når de kan se problemet ske foran sig, så kan de gøre noget ved det.

Altså: fortæl dem præcis hvad du gjorde. Hvis det er et program med grafisk brugergrænseflade, fortæl hvilke knapper du klikker på i hvilken rækkefølge. Hvis det er et kommandolinieprogram vis dem præcis den kommando du skrev, bogstaveligt talt. Når det er muligt bør du altid stille en eksakt afskrift af interaktionen med programmet til rådighed, der viser hvilke kommandoer du skrev og hvad computeren svarede.

Giv programmøren alle de oplysninger du kan komme på. Hvis programmet læser en fil, så vil det sandsynligvis være en god idé at sende en kopi af filen. Hvis programmet taler med en anden computer over et netværk kan du nok ikke sende en kopi af den computer, men du kan i hvert fald sige hvilken type computer det er og (hvis du kan) oplyse hvilke programmer der kører på den.

## "Det virker for mig. Hvad er problemet?"

Hvis du giver programmørerne en lang liste af inddata og handlinger og de starter programmet på deres egne maskiner og alt virker hos dem, så har du ikke givet dem nok information. Måske opstår fejlen ikke på alle computere; dit system og deres er måske forskellige på en eller anden måde. Måske har du misforstået hvad det er meningen programmet skal gøre og I kigger i virkeligheden på det samme, men du tror det er forkert og de ved det er korrekt.

Altså: beskriv hvad der skete. Fortæl dem præcist hvad du så. Fortæl dem hvorfor du mener det du så er forkert; eller endnu bedre: fortæl dem præcis hvad du forventede at se. Hvis du siger "og så kom fejlen", så har du udeladt vigtig information.

Hvis du så fejlmeddelelser så fortæl programmørerne om dem, omhyggeligt og præcist. De _er_ vigtige! På dette tidspunkt er programmørerne ikke i gang med at løse problemet: de er alene ved at finde det. De skal vide hvad der er gået galt, og fejlmeddelelserne er computerens bedste forsøg på at fortælle hvad det er. Skriv fejlmeddelelserne ned hvis du ikke har nogen anden nemmere måde at huske dem på. Det er ikke værd at fortælle at der kom en fejlmeddelelse hvis du ikke kan fortælle hvad fejlmeddelelsen var.

Specielt, hvis fejlmeddelelsen indeholder tal _fortæl_ programmøren hvad tallene var. Selv hvis du ikke kan se nogen mening i dem betyder det ikke at der ikke er nogen mening. Tal kan indeholde alle mulige oplysninger som programmørerne kan bruge og sandsynligvis giver de essentielle ledetråde. Tal i fejlbeskeder er der oftest fordi computeren er for forvirret til at give en fejlmeddelelse i ord, men den prøver så godt den kan at give vigtig information.

På dette tidspunkt er programmørerne i gang med detektivarbejde. De ved ikke hvad der er sket og de kan ikke komme tæt nok på til at se fejlen opstå selv, så de søger efter ledetråde som måske kan vise hvad det er. Fejlmeddelelser, uforståelighed tal, ja endda uforklarlige tidsmæssige forsinkelser er alle lige så vigtige som fingeraftryk på et gerningssted. Registrer dem!

Hvis du bruger Unix har programmet måske lavet et core dump. Core dumps er en god kilde til ledetråde, så slet dem ikke. På den anden side kan de fleste programmører ikke lide at modtage store filer per e-mail uden varsel, så spørg før du sender et core dump til nogen. Bemærk også at et core dump indeholder oplysninger om hele programmets tilstand: alle "hemmeligheder" der er involveret (måske var programmet ved at håndtere en personlig besked eller ved at håndtere fortrolige data) kan måske være indeholdt i core dumpet.

## "Og så prøvede jeg . . ."

Der er mange ting du kan gøre når en fejl viser sig. Mange af dem gør problemet værre. En af mine venner i skolen kom til at slette alle sine Word-dokumenter ved et uheld. Før hun ringede efter eksperthjælp prøvede hun først at geninstallere Word, hvorefter hun prøvede at køre Defrag. Hverken det ene eller det andet hjalp hende med at få filerne tilbage og tilsammen ændrede de hendes disk så meget at intet Undelete program i verden kunne have fået noget tilbage. Hvis hun bare havde ladet være med at gøre noget havde der måske været en chance.

Sådanne brugere er som et desmerdyr der er fanget i et hjørne: med ryggen mod muren og sikker død i udsigt angriber den som en bersærk, fordi at gøre noget må være bedre end intet at gøre. Det er ikke en særlig fornuftig fremgangsmåde for den type problemer computere præsenterer.

I stedet for at opføre dig som et desmerdyr, opfør dig som en antilope. Når en antilope konfronteres med noget uventet eller uhyggeligt, så står den helt stille. Den står stille og prøver på ikke at tiltrække sig opmærksomhed mens den tænker sig om og prøver at finde ud af hvad det mest fornuftige er at gøre. (Hvis antiloper havde en teknisk support telefonlinie, så ville den ringe dertil i denne situation). Når den så har fundet ud af hvad det sikreste er at gøre, så gør den det.

Når noget går galt så hold med det samme op med at gøre _noget som helst_. Rør ikke ved knapperne overhovedet. Kig på skærmen og læg mærke til alt der er unormalt, husk det eller skriv det ned. Derefter kan du forsigtigt tykke "OK" eller "Fortryd", hvad der nu virker sikrest. Prøv at opbygge en refleks der siger - hvis computeren gør noget unødvendigt, så stop op.

Hvis det lykkes dig at komme ud af problemet, hvadenten det sker ved at lukke programmet ned eller genstarte computeren, så er det en god idé at prøve på at få det til at opstå igen. Programmører kan bedst lide problemer man kan genskabe mere end en gang. Glade programmører retter fejl hurtigere og mere effektivt.

## "Jeg tror tachyon modulatoren er polariset forkert."

Det er ikke kun ikke-programmører som laver dårlige fejlrapporter. Nogle af de værste fejlrapporter jeg har set er fra programmører, og det endda gode programmører.

Jeg arbejdede med en programmør engang, som blev ved med at finde fejl i sin egen kode og prøvede at rette dem. En gang i mellem fandt han en fejl han ikke kunne løse og bad mig komme over og hjælpe. "Hvad er der galt?" spurgte jeg. Han svarede med at fortælle sin øjeblikkelige mening om hvad der burde rettes.

Det virkede fint når hans øjeblikkelige opfattelse var korrekt. Det betød at han allerede havde gjort halvdelen af arbejdet og vi kunne afslutte det sammen. Det var effektivt og brugbart.

Men ofte tog han fejl. Vi arbejdede et stykke tid på at prøve at gennemskue hvorfor en eller anden specifik del af programmet producerede forkert data og til sidst opdagede vi at det slet ikke gjorde det, at vi havde brugt en halv time på at finkæmme et stykke helt fin kode og at problemet lå et andet sted.

Jeg er sikker på at han ikke ville gøre det samme med en læge. "Doktor, jeg har brug for en recept på Hydroyoyodyne." Folk ved ikke hvad de skal sige hos lægen: man beskriver symptomerne, ubehaget, hvor det gør ondt, udslet og feber og så lader man lægen udarbejde diagnosen og hvad der skal gøres ved det. Hvis man ikke gør det kategoriserer lægen én som hypokonder eller småskør, med god ret.

Det er det samme med programmører. Det kan nogle gange være en hjælp at du kommer med din egen diagnose, men forklar altid hvad symptomerne er. Din egen diagnose er en valgfri ekstraoplysning og ikke et alternativ til at oplyse om symptomerne. På samme måde er det at sende en kodeændring en brugbar tilføjelse til en fejlrapport, men det er ikke en brugbar erstatning for samme.

Hvis en programmør beder dig om yderligere information skal du ikke bare opfinde noget! Der var en som rapporterede en fejl til mig engang og jeg bad ham om at prøve en kommando jeg vidste ikke ville virke. Grunden til at jeg bad ham om at prøve den var at jeg var interesseret i at vide hvilken af to fejlmeddelelser kommandoen ville give. At vide hvilken af dem der kom tilbage ville give en vigtig ledetråd. Men han prøvede den ikke - han skrev bare tilbage og sagde "Nej, det virkede heller ikke". Det tog mig et stykke tid at overtale ham til virkelig at prøve.

Det er fint at bruge sin intelligens til at hjælpe programmørerne. Selv hvis dine deduktioner er forkerte bør programmørerne være glade for at du i det mindste _prøvede_ på at gøre deres liv nemmere. Men rapporter også symptomerne, ellers gør du deres liv meget mere besværligt i stedet.

## "Det var sjovt, den gjorde det lige før."

Sig "periodisk fejl" til en hvilken som helst gruppe programmører og se dem blegne. De nemme problemer er dem hvor fejlen kommer når man udfører en simpel række af handlinger. Programmørerne kan gentage disse handlinger under tæt observation og se hvad der sker i detaljer. Mange problemer er ikke af den type: der er programmer som fejler en enkelt gang om ugen, ved højvande, og som aldrig fejler når du viser dem for en programmør, men altid lige før deadline.

De fleste periodiske fejl er ikke rigtigt periodiske. De fleste af dem han en eller anden slags logik et eller andet sted. Nogle sker måske kun når maskinen løber tør for hukommelse, nogle sker måske når et andet program prøver at modificere en vigtig fil på det forkerte tidspunkt og nogle sker måske kun i den første halvdel af hver time! (Jeg har faktisk været ude for sådan en).

Når du kan genskabe en fejl, men programmørerne ikke kan, så kan det meget vel være fordi deres computere er forskellig fra din og denne forskel udløser problemer. Jeg havde et program engang vis vindue krøllede sammen som en lille kugle i øverste venstre hjørne af skærmen, hvor det så sad og _klynkede_. Men det gjorde det kun på 800x600 skærme; det virkede fint på min 1024x768 skærm.

Programmørerne vil have alt du kan finde ud af om problemet at vide. Prøv det for eksempel på en anden maskine. Prøv det to eller tre gange og se hvor ofte det sker. Hvis fejlen opstår mens du laver rigtigt arbejde og ikke når du prøver at demonstrere den, kan det være lang køretid eller store filer der får fejlen til at optræde. Prøv at huske så mange detaljer du kan om hvad du var ved at gøre, da fejlen opstod, og hvis du ser nogen mønstre, nævn dem. Alt hvad du kan levere kan være til hjælp. Selv hvis det kun er sandsynligheder (som "det plejer at gå ned oftere når Emacs kører"), det giver måske ikke direkte spor til hvad årsagen er, men det kan måske hjælpe programmørerne til at genskabe fejlen.

Vigtigst af alt: Programmørerne vil ønske at være sikker på om det er en ægte periodisk fejl eller en maskin-specifik ting. De vil ønske at kende en masse detaljer om din computer, så de kan finde ud af hvordan din maskine adskiller sig fra deres. Hvilke detaljer der er relevante vil afhænge af hvad det er for et program, men en ting du helt sikkert skal have parat er versionsnumre. Versionsnummeret for programmet selv, versionsnummeret for operativsystemet og evt. for andre programmer involveret i problemet.

## "Jeg satte disken i min Windows . . ."

At formulere sig klart er essentielt i en fejlrapport. Hvis programmøren ikke kan forstå hvad du mente kunne du lige så godt ikke have sagt noget.

Jeg modtager fejlrapporter fra hele verden. Mange af dem er fra folk der ikke har engelsk som modersmål og en masse af dem undskylder for deres dårlige engelsk. For det meste er fejlrapporterne med undskyldninger for dårligt engelsk faktisk meget tydelige og brugbare. Alle de mest uklare rapporter kommer fra folk med engelsk som modersmål som går ud fra at jeg vil forstå dem selvom de ikke gør nogen som helst indsats for at være tydelige og præcise.

*   _Vær specifik_. Hvis du kan gøre det samme på to forskellige måder, fortæl hvilken af måderne du brugte. "Jeg valgte Åben" kan måske betyde "Jeg klikkede på Åben" eller "Jeg trykker Alt-L". Sig hvad du gjorde. Nogle gange har det betydning.
*   _Vær omhyggelig_. Giv hellere mere information end mindre. Hvis du siger for meget kan programmørerne ignorere noget af det. Hvis du siger for lidt bliver de nød til at stille dig yderligere spørgsmål. En fejlrapport jeg modtog var på en enkelt sætning; hver gang jeg bad om flere informationer fik jeg svar på en enkelt sætning tilbage. Det tog mig flere uger at få en brugbar mængde information lirket ud af vedkommende, fordi det kom en sætning af gangen.
*   _Vær forsigtig med stedordene_. Brug ikke ord som "den" og referér ikke til "vinduet" når det er uklart hvad ordene hentyder til. Et eksempel: "Jeg startede FooApp. Den viste et advarselsvindue. Jeg prøvede at lukke det og den gik ned.". Det er ikke klart hvad brugeren prøvede at lukke. Prøvede vedkommende at lukke advarselsvinduet eller hele FooApp? Det gør en forskel. I stedet kunne man have skrevet: "Jeg startede FooApp, som viste et advarselsvindue. Da jeg prøvede at lukke advarselsvinduet gik FooApp ned." Det er længere og indeholder mere gentagelse, men det er samtidig klarere og ikke så nemt at misforstå.
*   _Læs hvad du har skrevet_. Læs fejlrapporten igennem og se om _du_ synes den er klar. Hvis du har skrevet en række trin som skulle fremprovokere fejlen så prøv at følge dem selv, for at se om du har glemt et trin.

## Resumé

*   Det første mål for en fejlrapport er at give programmørerne mulighed for at opleve fejlen ved selvsyn. Hvis du ikke kan vise dem hvordan fejlen opstår personligt, så giv dem detaljerede instruktioner se de selv kan genskabe fejlen.
*   Hvis det første mål ikke nås og programmørerne _ikke_ kan se fejlen opstå selv, så er det andet mål for en fejlrapport at beskrive hvad der gik galt. Beskriv alt detaljeret. Fortæl hvad du så og fortæl også hvad du forventede at se. Skriv fejlmeddelelserne ned _specielt_ hvis de indeholder tal.
*   Når din computer gør noget uventet _stop op_. Lad være med at gøre noget som helst før du er rolig og gør ikke noget du tror kan være risikabelt.
*   Du er velkommen til at prøve at diagnosticere problemet selv hvis du tror du kan, men hvis du gør skal du stadigvæk også rapportere alle symptomerne.
*   Vær parat til at stille yderligere information til rådighed hvis programmørerne har brug for det. Hvis de ikke havde brug for det ville de ikke bede om det. De er ikke overlagt besynderlige. Hav versionsnumre parat for de vil sandsynligvis skulle bruges.
*   Skriv klart. Sig hvad du mener og gør det på en måde der ikke kan misforstås.
*   Aller vigtigst: _Vær præcis_. Programmører kan godt lide præcision.

* * *

_Bemærk:_ Jeg har aldrig set et desmerdyr eller en antilope i virkeligheden. Min zoologi kan meget vel være upræcis.