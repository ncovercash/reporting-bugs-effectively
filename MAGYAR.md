# Hogyan írjunk hatékony hibajelentést

_írta: Simon Tatham, profi és szabad programokat készítő programozó_

_Magyarra fordította: Varga Csaba (csaboka kukac gmail pont com)_

## Bevezető

Aki írt valaha tömeges használatra szánt programot, az valószínűleg kapott már legalább egy rossz hibajelentést. Ez lehet egy semmitmondó jelentés ("Nem megy!"); értelmetlen jelentés; túl kevés információt tartalmazó jelentés; olyan jelentés, ami _hibás_ információt tartalmaz. Szólhat olyan problémáról, ami valójában felhasználói hiba; olyanról, amit más program hibája okoz; vagy olyanról, ami valójában hálózati hiba.

Jó oka van annak, hogy a technikai segítségnyújtást sokan szörnyű munkának tartják, és ez az ok a rossz hibajelentés. Persze nem minden hibajelentés rossz: Fizetős programok mellett ingyeneseken is dolgozom, és néha ragyogóan világos, hasznos és _informatív_ hibajelentéseket is kapok.

Ebben az esszében megpróbálom világosan leírni, mitől lesz jó egy hibajelentés. A legjobb az lenne, ha mindenki végigolvasná, aki valaha is hibát akar bejelenteni. Legalább azt szeretném elérni, hogy mindenki, aki _nekem_ akar hibajelentést küldeni, végigolvassa.

Dióhéjban, a hibajelentés célja, hogy a programozó saját maga lássa, ahogy a program hibázik. Megmutathatod neki személyesen, vagy elmagyarázhatod aprólékosan, hogyan idézheti elő a hibát. Ha sikerül előidéznie a hibát, megpróbál majd információt gyűjteni a hiba okáról. Ha viszont nem sikerül előidéznie a hibát, téged kell majd megkérnie, hogy ezt az információt összegyűjtsd neki.

A hibajelentésekben mindig világosan válaszd szét, mi biztos tény ("A gépem előtt ültem és ez történt"), és mi találgatás ("_Szerintem_ ez és ez a hiba oka"). Ha gondolod, a találgatást kihagyhatod, de soha ne hagyd ki a tényeket.

A hibát azért jelented, mert szeretnéd, ha kijavítanák. Nincs értelme a programozót szidni, vagy szándékosan hátráltatni: lehet, hogy tényleg az ő hibája, de lehet, hogy te rontottál el valamit. Lehet, hogy jogosan vagy dühös rá, de a hibát hamarabb ki fogja javítani, ha segítesz neki és megadod az információt, amit kér. Ha a program ingyenes, ne felejtsd el, hogy a szerző szívességet tesz azzal, hogy dolgozik rajta; ha túl sok ember gorombáskodik vele, lehet hogy később nem lesz ilyen nagylelkű.

## "Nem megy."

Tiszteld meg azzal a programozót, hogy nem nézed teljesen hülyének: ha a program tényleg egyáltalán nem menne, valószínűleg már észrevette volna. Mivel még nem vette észre, valószínűleg nála működik. Tehát vagy valamit másképp csinálsz, mint ő, vagy a környezet különbözik az övétől. Információra van szüksége; a hibajelentés célja az, hogy ezt az információt megadd neki. A több információ majdnem mindig jobb a kevesebbnél.

Sok program, főleg a szabad programok esetében létezik nyilvános hibalista. Ha ezt a hibalistát sikerül megtalálnod, érdemes elolvasnod, mert ebből kiderül, a hibádról tudomásuk van-e a készítőknek. Ha a hiba már ismert, valószínűleg nem érdemes újra bejelenteni; ha viszont úgy érzed, te több információt tudsz szolgáltatni, mint ami a hibalistában van, akkor érdemes lehet mégis kapcsolatba lépni a fejlesztőkkel. Lehet, hogy könnyebben ki tudják javítani a hibát, ha új információt tudsz szolgáltatni róla.

Ez az esszé tanácsok gyűjteménye. Egyik tanács sem kőbe vésett szabály. A programozótól is függ, milyen hibajelentésekkel boldogul könnyebben. Ha a programhoz mellékeltek saját hibajelentési tanácsokat, akkor azokat is olvasd el. Ha az ottani utasítások ellentmondanak az ittenieknek, a programhoz mellékelteket vedd figyelembe!

Ha nem hibát jelentesz be, csak segítséget szeretnél kérni, mindig mondd el, hol próbáltál utánanézni a válasznak. ("A 4\. fejezet 5.2-es részében kerestem, de nem találtam utalást rá, hogy ez lehetséges-e.") Így a programozó tudni fogja, hol keresik az emberek a válaszokat, és javíthat a dokumentáció színvonalán.

## "Mutasd meg!"

A legeslegjobb módszer a hibajelentésre az, ha a programozó szeme előtt idézed elő a hibát. Hívd oda a géped elé, indítsd el a programját, és mutasd meg neki, mi romlik el benne. Hadd nézze, ahogy elindítod a gépet, futtatod a programot; hadd lássa, hogyan kezeled a programot és a program mit válaszol a műveletekre.

Ő úgy ismeri a programját, mint a tenyerét. Tudja, melyik rész megbízható és melyikben lehetnek hibák. Ösztönösen tudja, mire figyeljen. Mire oda jutsz, hogy a program valamit teljesen rosszul csinál, ő már korábban észrevehetett valami _apró_ hibát, ami nyomra vezeti. Mindent megfigyelhet, amit a számítógéped csinál, és maga keresheti meg a fontos momentumokat.

Ez nem mindig elég. Lehet, hogy több információra lesz szüksége, és megkér, hogy ismételd meg az egészet elölről. Megkérhet, hogy magyarázd el lépésről lépésre, mit csináltál, hogy később majd akárhányszor elő tudja idézni saját maga. Lehet, hogy megpróbálja ugyanazt a dolgot kis változtatásokkal, hogy kiderüljön, csak egy esetben fordul-e elő a hiba, vagy több hasonló esetben is. Ha nincs szerencséd, lehet hogy pár órára a géped elé ül pár fejlesztőeszközzel és elkezd _komolyan_ nyomozni a hiba után. A legfontosabb azonban az, hogy a programozó figyelje a gépedet, amikor valami elromlik. Ha már látja a problémát "élesben" megtörténni, általában van honnan elindulnia a javításhoz.

## "Mutasd meg, hogy idézhetem elő!"

Az Internet és a világot átszelő kommunikáció korában élünk. Olyan kor ez, amikor egyetlen gombnyomással elküldhetem a programomat valakinek Oroszországba, és ő ugyanilyen könnyen küldheti nekem vissza az észrevételeit. Ha viszont gondja van a programommal, _nem_ tudok odamenni a gépéhez, hogy saját szememmel lássam a hibát. A "mutasd meg" nagyszerűen működik, de gyakran lehetetlen.

Ha a programozó személyesen nem lehet jelen, a hibajelentés célja az, hogy segítsen a programozónak _megismételni_ a hibát. A lényeg, hogy a programozó a saját gépén futtassa a programot, ugyanazt csinálja vele, amit te csináltál, és ugyanúgy előhozza a hibát, ahogy nálad jelentkezett. Ha már a saját szemével látja, tud majd boldogulni vele.

Ezért aztán mondd el, pontosan mit csináltál. Ha a program grafikus, mondd el, melyik gombokat nyomtad le, és milyen sorrendben. Ha a program használatához parancsot kell begépelni, mutasd meg pontosan milyen parancsot gépeltél be. Amikor csak lehetséges, küldd el a munkamenet teljes naplóját, vagyis azt, hogy mit írtál be és erre milyen kimenetet adott a gép.

Adj meg a programozónak minden segítséget, ami eszedbe jut. Ha a program egy fájlból olvas, valószínűleg el kell küldened a fájl másolatát. Ha a program egy másik géppel kommunikál a hálózaton, nem tudod a gépet elküldeni, de elmondhatod, milyen számítógép, és (ha tudod), hogy milyen programok futnak rajta.

## "Nálam megy. Mi a gond?"

Ha részletesen leírod a programozónak, mit csináljon, ő elindítja a saját példányát, elvégzi a műveleteket és semmi hiba nem jelentkezik, akkor nem szolgáltattál elég információt. Lehet, hogy a hiba nem minden számítógépen jelentkezik; a te rendszered valamiben különbözhet a programozóétól. Lehet, hogy félreértetted, mit csinál a program, így aztán mindketten ugyanazt a képernyőt nézitek, csak szerinted az rossz, ő pedig tudja, hogy jó.

Ezért aztán írd le azt is, mi történt. Mondd el, mit láttál pontosan. Mondd el, szerinted miért rossz az, amit láttál; vagy még jobb, ha pontosan elmondod, mire számítottál, mit fogsz látni. Ha csak annyit mondasz: "és akkor elromlott", fontos információt hallgatsz el.

Ha hibaüzenetet láttál, mondd el a programozónak figyelmesen és pontosan, hogy mi volt az. Az üzenetek _fontosak_! A programozó még nem próbálja kijavítani a problémát, most még csak keresi. Tudnia kell, mi romlott el, és a számítógéped hibaüzenetekkel igyekszik ezt elmondani. Írd le valahová az üzenetet, ha nem tudod megjegyezni; semmi értelme azt mondani, hogy a program hibaüzenetet írt ki, ha nem tudod magát az üzenetet is elküldeni.

Fontos, hogy ha a hibaüzenetben vannak számok, _mindenképp_ küldd el a számokat is a programozónak. Attól még, hogy számodra értelmetlennek tűnnek, nem azok. A számokban rengeteg olyan információ lehet, amit a programozó megért és nyomra vezethet. A számok azért vannak a hibaüzenetekben, mert a számítógép túlságosan összezavarodott és nem tudja szavakban kifejezni a hibát, de azért igyekszik ezt a fontos információt eljuttatni hozzád valamilyen formában.

Ebben az esetben a programozó gyakorlatilag nyomozómunkát végez. Nem tudja, mi történt, és nem tudja a saját szemével megnézni, ahogy elromlik, így hát nyomokat keres, amikkel megtalálhatja a hibát. A hibaüzenetek, érthetetlen számsorok, sőt még a váratlan lassulások is olyan fontosak, mint egy ujjlenyomat egy bűntény színhelyén. Tartsd hát meg őket!

Ha Unix-ot használsz, a program készíthetett memóriamentést (core dump). A memóriamentések nagyon sok nyomot tartalmaznak, ne dobd el őket! A legtöbb programozó viszont nem szeret figyelmeztetés nélkül óriási memóriamentéseket kapni e-mailben, ezért mindig kérdezz rá, mielőtt elküldöd. Azt se felejtsd el, hogy a memóriamentés a program teljes állapotát tartalmazza: bármilyen "titok" (pl. a magánlevél, amit éppen olvastál vagy a bizalmas adatok, amiken dolgoztál) bekerülhetett.

## "Aztán megpróbáltam ..."

Rengeteg dolgot tehetsz, amikor egy hibába botlasz. Ezek közül sok csak tovább ront a helyzeten. Az egyik iskolai barátom véletlenül letörölte az összes Word dokumentumát; mielőtt szakértő segítségét kérte volna, megpróbálta újratelepíteni a Wordöt, aztán megpróbálta töredezettség-mentesíteni a meghajtót. Egyik sem segített visszahozni a fájlokat, viszont eléggé összekavarták a meghajtó adatait ahhoz, hogy semmilyen visszatörlő program se tudja visszahozni őket. Ha nem nyúlt volna hozzá, még lett volna esélye.

Az ilyen felhasználó olyan, mint a sarokba szorított mongúz: nem látja a kiutat, és a biztos halál nevet az arcába, így kétségbeesett támadásba kezd, hiszen valamit csinálni biztosan jobb, mint tétlenül várni. Ez a hozzáállás nem igazán működik a számítógépes problémákra.

Ne légy mongúz, legyél inkább antilop. Ha az antilop valami váratlannal vagy ijesztővel találkozik, nem mozdul. Teljes mozdulatlanságba dermed és próbálja nem magára vonni a figyelmet, közben azon gondolkodik, mi lenne most a legjobb lépés. (Ha az antilopoknak lenne technikai segítségvonaluk, akkor most épp őket hívná.) Amikor végül eldönti, mi a legbiztonságosabb lehetőség, azt választja.

Ha valami elromlik, azonnal hagyj abba _mindent_. Ne nyúlj egyik gombhoz se. Nézz a képernyőre, keress meg minden szokatlant, majd jegyezd meg vagy írd le őket. Azután esetleg megpróbálhatsz óvatosan "OK"-t vagy "Mégsem"-et nyomni, attól függ, melyik tűnik biztonságosabbnak. Próbálj meg egy reflexet kialakítani - ha a számítógép bármi váratlant csinál, azonnal állj meg.

Ha végül sikerül kezelni a problémát az érintett program bezárásával vagy a számítógép újraindításával, jó ötlet megpróbálni újra előhozni a hibát. A programozók szeretik az olyan problémákat, amiket többször elő tudnak idézni. A boldog programozók gyorsabban és hatékonyabban javítják a hibákat.

## "Szerintem a tachionmodulátor rosszul van polarizálva"

Nem csak a programozáshoz nem értők írnak rossz hibajelentéseket. A legrosszabb hibajelentések egy részét programozóktól kaptam, néha még jó programozóktól is.

Egyszer dolgoztam egy másik programozóval, aki folyton hibákat talált a saját kódjában és megpróbálta kijavítani őket. Időnként olyan hibába botlott, amit nem tudott megoldani, és ilyenkor áthívott, hogy segítsek. "Mi a baj?", kérdeztem én. Ő válaszképpen elmondta, hogy szerinte melyik részt kell kijavítani.

Ez jól működött, amikor helyes volt a megérzése. Ilyenkor ő már el is végezte a munka felét, és közösen be tudtuk fejezni a maradékot. Ez hatékony és hasznos volt.

Azonban nagyon gyakran tévedett. Egy ideig együtt kerestük, a program egy adott része miért produkál hibás adatokat, és végül rájöttünk, hogy nem is hibásak az adatok. Fél órát töltöttünk azzal, hogy egy tökéletes kódrészletben hibát találjunk, miközben a gond valahol máshol volt.

Gondolom nem csinálnád ugyanezt egy orvossal. "Doktor úr, írjon fel nekem Hydroyoyodyne-t!" Ilyet nem mondasz egy orvosnak: elmondod a tüneteket, hogy hol fáj, hogy hol viszket, hogy hol van kiütés vagy hogy van-e lázad, és az orvos dolga eldönteni, hogy mi a baj és hogy lehet megoldani. Ha nem ezt tennéd, az orvos hipochondriásnak vagy bolondnak nézne, teljesen jogosan.

A programozókkal ugyanez a helyzet. A saját diagnózisod néha segíthet, de mindig mondd el a tüneteket is. A diagnózis egy plusz lehetőség, de nem helyettesítheti a tünetek leírását. Hasonlóképpen, a hibát javító kódrészlet hasznos kiegészítője a hibajelentésnek, de nem helyettesítheti azt.

Ha a programozó további információt kér, ne próbáld magadtól kitalálni a választ! Valaki egyszer jelentett nekem egy hibát, és megkértem, hogy próbáljon ki egy programot, amiről tudtam, hogy nem fog működni. Azért kértem meg, mert tudni akartam, a két lehetséges hibaüzenet közül melyiket adja vissza. A hibaüzenet fontos nyom lett volna. De a felhasználó nem próbálta meg - csak annyit válaszolt, hogy "Nem, ez nem menne". Beletelt egy időbe, mire rávettem, hogy azért csak próbálja meg.

A saját intelligenciáddal segíteni a programozót kedves dolog. Még ha rosszak is a következtetéseid, a programozó hálás lehet, hogy _megpróbáltad_ megkönnyíteni az életét. De azért mondd el a tüneteket is, különben lehet, hogy még jobban megnehezíted az életét.

## "Ez vicces, egy perccel ezelőtt még csinálta."

Az "időszakos hiba" kifejezéstől minden programozónak borsódzik a háta. A könnyű problémák azok, amiknél egy egyszerű cselekvéssor hibát okoz. A programozó megismételheti a lépéseket a saját tesztkörnyezetében és részletesen végigkövetheti, mi történik. Sok probléma egyszerűen nem ilyen: a program csak hetente egyszer romlik el, vagy csak szökőévente egyszer; esetleg sose romlik el, ha a programozó látja, de mindig elromlik a határidő előtt egy nappal.

A legtöbb időszakos hiba valójában nem is időszakos. Általában van mögöttük valami logika. Lehet, hogy akkor jön elő, ha a gépen már kevés a szabad memória, vagy akkor, ha a program pont rosszkor próbál módosítani egy kritikus fájlt, esetleg mindig csak az óra első felében. (Igen, ilyet is láttam már.)

Ha te elő tudsz hozni egy hibát, de a programozó nem, akkor az is lehet, hogy valamiben különbözik a kettőtök gépe, és ez a különbség okozza a problémát. Egyszer láttam egy olyan programot, ami egy kis labdává húzódott össze a képernyő bal felső sarkában, úgy maradt és _duzzogott_. Ezt csak 800x600-as képernyőn csinálta; az én 1024x768-as monitoromon semmi baja nem volt.

A programozó mindent tudni akar majd, amit ki tudsz deríteni a problémáról. Esetleg próbáld ki más gépen. Próbáld ki kétszer vagy háromszor, hogy kiderüljön, milyen gyakran romlik el. Ha csak akkor romlik el, ha épp komoly munkát végeznél vele, de akkor sohasem, ha épp megmutatnád a programozónak, lehet, hogy a hosszú futásidő vagy a nagy fájlok okozzák a bajt. Próbálj meg minél több részletet megjegyezni arról, mit csináltál, amikor elromlott, és ha szabályosságokat látsz, említsd meg őket. Bármi, amit tudsz, segíthet valamit. Még ha csak valószínűségeket tudsz is mondani (pl. "gyakrabban omlik össze, ha az Emacs fut"), ha nem is segít hozzá közvetlenül az okhoz, segíthet a programozónak, hogy megismételje a hibát.

Fontos, hogy a programozó tudni akarja majd, tényleg időszakos hibáról van-e szó, vagy gépfüggő hibáról. Rengeteg részletet kérhet majd a gépedről, hogy rájöhessen, miben különbözik az övétől. Ezeknek a részleteknek a nagy része az adott programtól függ, de arra mindenképp számíts, hogy verziószámokat fog kérni. A program verziószámát, az operációs rendszer verziószámát és minden olyan egyéb program verziószámát, ami kapcsolatos a problémával.

## "Aztán betöltöttem a lemezt a Windowsomba..."

A világos fogalmazás létfontosságú egy hibajelentésnél. Ha a programozó nem érti, mit akarsz mondani, felesleges volt egyáltalán hozzászólni.

A világ minden tájáról kapok hibajelentéseket. Sokat nem angol anyanyelvű emberek írnak, és sokan elnézést kérnek a hibás angolságukért. Általában az ilyen elnézést kérő levelek nagyon világosak és hasznosak szoktak lenni. A leghomályosabb jelentéseket olyan angol anyanyelvű emberektől kapom, akik szerint én akkor is megértem őket, ha meg se próbálnak világosan vagy pontosan fogalmazni.

*   _Légy pontos_. Ha kétféleképpen lehet csinálni valamit, mondd meg, melyiket használtad. "A Load-ot választottam" jelentheti azt, hogy "a Load gombra kattintottam", vagy azt, hogy "lenyomtam az Alt-L kombinációt". Mondd el, melyik volt. Néha számít.
*   _Légy részletes_. Inkább több információt szolgáltass, mint kevesebbet. Ha túl sok mindent mondasz, a programozó kihagyhatja a lényegtelen részeket. Ha túl keveset mondasz, vissza kell majd kérdeznie. Volt olyan, hogy egymondatos hibajelentést küldött valaki; akárhányszor több információt kértem, mindig egy-egy mondatban válaszolt. Több hétbe került, mire elég információt sikerült szereznem, mert mondatonként kellett kicsikarnom.
*   _Figyelj oda a névmásokra_. Ne mondd azt, hogy "az", és ne mondj olyanokat, hogy "az ablak", ha nem egyértelmű, mire vonatkozik. Például nézzük ezt: "Elindítottam a FooApp-ot. Feldobott egy figyelmeztető ablakot. Megpróbáltam bezárni és erre összeomlott." Nem világos, hogy mit próbált a felhasználó bezárni: a figyelmeztető ablakot vagy az egész FooApp-ot. Nem mindegy. Ehelyett mondd azt, "Elindítottam a FooApp-ot, ami feldobott egy figyelmeztető ablakot. Megpróbáltam bezárni a figyelmeztető ablakot, és erre a FooApp összeomlott." Így hosszabb és több az önismétlés, de világosabb és nehezebb félreérteni.
*   _Olvasd vissza, amit írtál_. Olvasd el újra a jelentést, és gondold át, hogy _szerinted_ érthető-e. Ha egy cselekvéssort küldesz, ami a hiba előidézéséhez kell, próbáld meg saját magad végigcsinálni, így kiderül, ha kihagytál egy lépést.

## Összefoglalás

*   A hibajelentés elsődleges célja, hogy a programozó saját szemével láthassa a hibát. Ha nem tudod személyesen megmutatni neki, küldj részletes utasításokat, hogy elő tudja saját maga idézni.
*   Ha az elsődleges cél nem érhető el, és a programozó _nem tudja_ saját szemével megnézni a hibát, a hibajelentés másodlagos célja annak a leírása, hogy mi romlott el. Írj le mindent részletesen. Írd le, mit láttál, és szerinted mit kellett volna látnod. Írd le a hibaüzeneteket is, _főleg_ hogyha számok is vannak bennük.
*   Ha a számítógéped valami váratlan dolgot csinál, _állj meg_. Ne csinálj semmit, amíg meg nem nyugodtál, és ne csinálj olyasmit, ami szerinted veszélyes lehet.
*   Ha képes vagy rá, próbáld meg kitalálni a hiba okát, de ettől függetlenül mindig küldd el a tüneteket is.
*   Készülj fel rá, hogy további információt szolgáltass a programozónak, ha szüksége van rá. Ha nem lenne rá szüksége, nem kérdezné meg. A programozók szándékosan nem szoktak kellemetlenkedni. Legyenek kéznél a verziószámok, valószínűleg szükség lesz rájuk.
*   Írj világosan, ne légy félreérthető.
*   Mindenképpen _légy pontos_. A programozók szeretik a pontosságot.

* * *

_Figyelem:_ A valóságban soha nem láttam se mongúzt, se antilopot. Lehet, hogy nem pontosak az álattani ismereteim.