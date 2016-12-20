# Jak správně hlásit chyby

Originál [How To Report Bugs Effectively](http://www.chiark.greenend.org.uk/~sgtatham/bugs.html) (c) 1999 Simon Tatham  
Překlad verze z 1\. června 2004

## Úvod

Každý, kdo někdy psal software, pravděpodobně dostal nějaké špatné chybové hlášení. Buďto nicneříkající ("Je to rozbitý!"), nebo nesmyslné, nebo neinformativní, nebo _chybné_. Nebo se ukáže, že je to chyba uživatele; nebo nějakého jiného programu; nebo nefunkční sítě.

Hlavní důvod, proč je práce v uživatelské podpoře tak hrozná, jsou špatná chybová hlášení. Nicméně ne všechna chybová hlášení jsou nepříjemná: sám vyvíjím software, a občas dostávám krásně čistá, jasná, informativní hlášení.

V tomto článku se pokusím jasně vyložit, jak hlásit chyby dobře. V ideálním případě si to přečte úplně každý ještě předtím, než někomu začne hlásit chyby; každopádně bych rád, aby si to přečetli ti, kteří hlásí chyby _mě_.

Stručně řečeno, smyslem chybového hlášení je ukázat programátorovi na vlastní oči, jak a kde jeho program selže. To se dá ukázat buďto osobně, nebo pomocí pečlivých, detailních instrukcí o tom, jak dovést program k chybě. Pokud se programátorovi podaří dovést takto program k chybě, pokusí se najít další příznaky a odhalit příčinu chyby. Pokud se mu to nepodaří, budete to za něj muset odhalovat vy.

Snažte se v chybových hlášeních rozlišit fakta ("udělal jsem tohle a stalo se toto") od spekulací ("myslím, že tohle je špatně"). Spekulace můžete klidně vynechat, ale fakta vynechat nesmíte.

Když někomu hlásíte chybu, děláte to proto, že chcete, aby ji opravil. Je zbytečné se rozčilovat: možná, že programátor udělal chybu, tím vám způsobil problémy, a vy máte právo být naštvaní; ale chyba bude opravena tím rychleji, čím více informací programátorovi poskytnete. Pamatujte také na to, že pokud je program zdarma, poskytuje vám ho vlastně autor ze své dobré vůle. Pokud se na něj budou lidé rozčilovat, dobrá vůle ho možná přejde.

## "Je to rozbitý!"

Přiznejte programátorovi jistou inteligenci: kdyby ten program vůbec nefungoval, asi by si toho všiml. Pokud si něčeho takového nevšiml, asi mu ten program funguje. Čili: buď děláte něco jinak, nebo v jiném prostředí. To právě potřebuje programátor vědět; to je smyslem chybového hlášení. A více informací je v tomto případě lépe než méně.

U mnoha programů - speciálně u free software - je publikován seznam dosud odhalených chyb. Pokud takový seznam existuje i pro váš program, stojí za to si ho přečíst; třeba už se o té chybě ví. V tom případě nemá cenu ji hlásit znovu. Pokud nicméně máte další informace (oproti původnímu hlášení), můžete programátora kontaktovat znovu: možná bude s novými informacemi snazší chybu opravit.

Tento článek je plný takovýchto doporučení. Žádné z nich není absolutním pravidlem. Mnozí programátoři mají svůj oblíbený způsob, jak dostávat chybová hlášení. Pokud je k programu přiložen návod, jak hlásit chyby, přečtěte si ho. Pokud se tam tvrdí něco jiného než v tomto článku, řiďte se tím, co je uvedeno v návodu pro váš konkrétní program!

Pokud nehlásíte chybu, ale prostě se jen ptáte na radu, uveďte při tom, kde už jste hledali ("Pročetl jsem v dokumentaci kapitolu 4 a odstavec 5.2, ale nic jsem o tom nenašel."). Pak bude programátor vědět, kde lidé očekávají odpověď - což mu umožní vylepšit dokumentaci.

## "Ukaž."

Nejlepší způsob, jak ohlásit chybu, je přímo ji programátorovi ukázat. Postavte ho před svůj počítač, spusťte jeho program, a ukažte, kde přesně selže. Ať vidí, jak spouštíte počítač, jak spouštíte program, jak program používáte, jak přesně program reaguje na vaše příkazy.

On ten program zná jako svoje boty. Ví, kterým částem může věřit, a kde by mohly být chyby. Ví, na co si dát pozor. Ve chvíli, kdy program zjevně selže, už si třeba všimne nějaké maličkosti, která předcházela, a to mu napoví. Uvidí všechno, co se během vašeho testu děje, a vybere si z toho to podstatné.

Třeba to nebude stačit. Třeba vás požádá, ať chybu reprodukujete ještě jednou. Třeba vás požádá o důkladný slovní komentář, aby pak mohl chybu sám reprodukovat kolikrát bude chtít. Provede ten samý test s malými změnami a uvidí, jestli se program takto chová v tom jediném případě, nebo i při jiných konfiguracích. Když budete mít smůlu, bude si možná potřebovat na pár hodin sednout, vytáhnout nádobíčko, a důkladně se v tom pohrabat. Nejdůležitějsí ale je, že je přímo u toho, když program selže. Jakmile to jednou uvidí, většinou může rovnou začít pracovat na opravě.

## "Ukaž si sám.""

Žijeme v době internetu a globální komunikace. Stiskem klávesy mohu svůj software poslat známému z Ruska, a on mi stejně snadno pošle svůj komentář. Přesto ale, pokud má s mým programem potíže, nebudu zrovna stát u jeho monitoru. V tom případě mi chybu předvést nemůže.

Pokud nemůže být programátor osobně přítomen, musíte mu sdělit, jak chybu _reprodukovat_. Musí být schopen spustit svoji kopii programu, ve svém prostředí, postupovat stejně jako vy, a dojít ke stejné chybě. Pak ji uvidí na vlastní oči.

Sdělte mu tedy, co přesně jste udělali. Pokud je to grafický program, řekněte, které čudlíky jste stiskli, a v jakém přesně pořadí. Pokud spouštíte příkaz z příkazové řádky, přesně jej ocitujte. Jakmile je to možné, zašlete přesný záznam své interakce s programem: co jste napsali, jak program reagoval.

Sdělte programátorovi vše, co by mohl potřebovat. Pokud program načítá nějaký soubor, pošlete kopii toho souboru. Pokud program interaguje s jiným počítače, asi nebudete posílat kopii počítače, ale řekněte, co je to za počítač a co na něm běží za programy.

## "Mě to funguje ..."

Pokud zašlete programátorovi dlouhý seznam příkazů a reakcí na ně, a on spustí svoji vlastní kopii, provede přesně totéž, a k žádné chybě nedojde, pak jste mu nedali dost informací. Možná program selhává jen na některých počítačích; jeho a vaše prostředí se v něčem liší. Možná se pletete v tom, co má program přesně dělat. Koukáte oba přesně na totéž, ale vy si myslíte, že je to chyba, a on ví, že je to správně.

Řekněte tedy, proč takové chování programu považujete za chybu. Nebo lépe, řekněte přímo, jakou reakci byste od programu v takové situaci očekávali. Pokud řeknete jen "a pak se to rozbilo", pak vynecháváte podstatnou věc.

Pokud program sám produkuje nějaké chybové hlášky, řekněte to. Ocitujte je přesně, jsou důležité! V této fázi se programátor ještě nesnaží chybu opravit, snaží se ji teprve najít. Snaží se zjistit, co přesně se pokazilo, a chybové hlášky programu samotného jsou tím nejlepším vodítkem. Pokud nemáte jinou možnost, sami si chybovou hlášku opište. Je zbytečné prográmatorovi sdělovat, že "program ohlásil chybu", pokud nevíte jakou.

Pokud má chybová hláška svoje číslo, řekněte ho. Pokud vám ta čísla nic neříkají, neznamená to, že neříkají nic ani nikomu jinému. V číslech je obsažena spousta informací, kterým bude programátor rozumět, a leccos mu napoví. Ta čísla jsou tam proto, že program je příliš zmaten na to, aby se vyjádřil slovně; dělá co může, aby vám něco důležitého sdělil.

Programátor teď vyšetřuje. Neví, co se přesně stalo, nebyl u toho, hledá stopy. Chybové hlášky a nesrozumitelné chuchvalce čísel jsou pro něj otisky prstů na místě činu. Nesmažte je!

Pokud používáte UNIX, možná po programu zůstal <tt>core dump</tt>. To je soubor, který obsahuje spoustu informací o stavu programu v okamžiku chyby, jakási černá skříňka - nezahazujte ji! Nikdo nicméně nechce dostávat poštou obrovské soubory, proto se nejdříve zeptejte, než core dump pošlete. Uvědomte si také, že core dump obsahuje - spolu s ostatními informacemi o stavu programu - i veškerá "citlivá" data, které jste programu poskytli.

## "Tak jsem zkusila ..."

Pokud se vyskytne nějaká chyba, lze udělat mnoho různých věcí, a většina z nich to jenom zhorší. (Jednou na škole si kamarádka omylem smazala všechny wordovské dokumenty, a dříve než cokoli jiného reinstalovala Word a spustila defrag. To bylo samozřejmě k ničemu, ale místo na disku si zpřeházela tak, že už z toho žádný Undelete nedostal vůbec nic. Kdyby to nechala být, tak měla šanci.)

Takoví uživatelé jsou jako fretka zahnaná do kouta: zády ke zdi a tváří v tvář jisté smrti začne bezhlavě útočit, protože to přeci musí být lepší než nedělat nic. To u programů nefuguje.

Nebuďte fretka, buďte antilopa: když narazí na něco neočekávaného nebo děsivého, ztuhne. Zůstane naprosto klidná, snaží se nebudit žádnou pozornost, stojí a přemýšlí, co má dělat. (A kdyby měly antilopy linku technické podpory, tak by tam zavolala.) Jakmile přijde na to, co je potřeba udělat, udělá to.

Pokud se něco pokazí, přestaňte pracovat. Na nic nesahejte. Projděte obrazovku, všimněte si všech nesrovnalostí, a poznamenejte si je. Teprve potom odpovězte stiskem nějakého tlačítka. Vyviňte si takový reflex pro situace, kdy počítač udělá něco neočekávaného.

Pokud se vám podaří se problému nějak zbavit, třeba ukončením programu nebo rebootem počítače, pokuste se k chybě dojít znovu. Programátoři mají rádi problémy, které se dají reprodukovat. A spokojení programátoři opravují chyby rychleji a lépe.

## "Máš tu laserovou modulaci špatně polarisovanou!"

Špatná chybová hlášení nepřicházejí jen od neprogramátorů. Ta nejhorší, která jsem viděl, pocházela od programátorů, dokonce od dobrých programátorů.

Jednou jsem pracoval s programátorem, který ve svém kódu stále nacházel chyby, a snažil se je opravovat. Občas se mu to nedařilo a zavolal mi. "Co je špatně?" zeptal jsem se. Odpověděl mi, co by bylo potřeba - podle jeho názoru - opravit.

To fungovalo docela dobře, pokud byl jeho názor správný - půlku už měl tedy vlastně hotovou, a spolu jsme zvládli zbytek. Bylo to rychlé a užitečné.

Docela často se ale mýlil. Hledali jsme v kusu programu, odkud se berou ta chybná data, až jsme zjistili, že odnikud; půl hodiny jsme zkoumali zcela korektní kód, problém byl úplně jinde.

Přitom u doktora by něco takového učitě neudělal. "Pane doktore, potřebuju recept na Hydroyoyodyn!" - každý ví, že takhle se to nedělá; vy popíšete příznaky, bolesti a vyrážky, a diagnózu provede a léčbu předepíše doktor. (V opačném případě vás prostě diagnostikuje jako hypochondra nebo cvoka; a to nejspíš zcela správně.)

S programátory je to stejné: vaše vlastní diagnóza může někdy pomoci, ale hlavně uveďte příznaky. Vlastní diagnóza je jaksi navíc, není to náhrada. Stejně tak zaslat opravu chybného kódu je užitečné plus, ale nenahrazuje to popis chyby.

Pokud si programátor vyžádá další informace, nepodceňujte to. Jednou jsem dostal chybové hlášení, a požádal jsem uživatele ať spustí příkaz, o kterém jsem věděl, že jistě nebude fungovat - chtěl jsem vědět _kterou_ chybovou hláškou (ze dvou možných) program odpoví. To by mi velmi pomohlo. On to ale nezkusil - jenom mi poslal "Ne, to nefunguje". Nějaký čas jsem ho přesvědčoval, ať to skutečně vyzkouší.

Pomáhat programátorovi vlastním rozumem je jistě hezké. I když se třeba mýlíte, měl by vám být vděčný, že se mu snažíte usnadnit život. Každopádně ale uvádějte hlavně příznaky, protože jinak mu život spíše komplikujete.

## "To je zvláštní, teď to fungovalo"

Řekněte programátorovi "taková občasná chyba ..." a sledujte, jak mu spadne čelist. Problémy, při kterých jednoduchá posloupnost úkonů vyvolá chybu, jsou snadné. Programátor může totéž provést znovu, pomalu, za ostře sledovaných testovacích podmínek, a detailně se podívat, co se děje. Často je to ale horší: chyba nastane třeba jednou za týden, nebo jednou za uherský rok, nebo nikdy (případně nikdy, když ji chcete programátorovi předvést), ale vždycky, když máte zítra odevzdávat hotový program.

Většina "občasných chyb" nejsou občasné chyby. Mají nějakou vnitřní logiku - nastávají třeba když dojde paměť, když _jiný_ program změní nějaký kritický soubor, nebo nastávají vždy jen v první polovině hodiny! (To jsem viděl.)

Pokud se Vám daří chybu reprodukovat, ale programátorovi ne, může to znamenat, že se vaše počítače liší v něčem, co právě tu chybu způsobuje. Napsal jsem kdysi program, jehož okno se občas "zarolovalo" do levého horního rohu a tam trucovalo. To ale jen při rozlišení 800x600; na mém monitoru 1024x768 se to nikdy nestalo.

Programátora bude zajímat všechno, co o tom problému víte. Zkuste třeba to samé na jiném počítači. Zkuste to dvakrát nebo třikrát: dopadne to stejně? Pokud k chybě dochází při skutečné práci, ale nikoli při reprodukci chyby, může to být tím, že při práci máte otevřenou spoustu velkých souborů. Pamatujte si co nejvíce detailů o tom, co jste přesně udělali, než program selhal; pokud v tom vidíte nějakou zákonitost, řekněte to. Cokoli se může hodit. I když to bude jen statistický údaj ("děje se to častěji, když mám puštěný Emacs"), který neposkytuje přímou nápovědu, může to programátorovi pomoci chybu reprodukovat.

A co je nejdůležitější, programátor se bude chtít ujistit, zda běží skutečně o "náhodnou" chybu nebo je chyba závislá na počítači. Bude chtít vědět spoustu detailů o vašem počítači, aby je porovnal se svým. Mnoho detailů bude záviset na tom kterém programu, ale rozhodně si připravte čísla verzí: verzi programu, verzi operačního systému, a verze souvisejícíh programů.

## "Tak jsem to načetl ve Windows ..."

Vyjádřit se jasně je v chybovém hlášení zásadní věc. Pokud programátor nepochopí, co jste chěli říct, jako byste neposlali nic.

Sám dostávám chybová hlášení z celého světa. Spoustu z nich píší lidé, pro které angličtina není mateřským jazykem, a mnozí se za svou chatrnou angličtinu omlouvají. Taková hlášení jsou většinou naprosto jasná a velmi užitečná. Ta nejzmatenější přicházejí od rodilých mluvčí, patrně s předpokladem, že jim budu rozumět, i když se o to nebudou nikterak snažit.

*   _Buďte přesní._ Pokud se dá jedna věc udělat dvěma způsoby, řekněte, který jste použili. "Vybral jsem <tt>Load</tt>" může znamenat "kliknul jsem na <tt>Load</tt>" nebo "stisknul jsem <tt>Alt-L</tt>". A na tom rozdílu může záležet.
*   _Nešetřete slovy._ Sdělte raději více než méně. Pokud řeknete příliš, programátor si z toho může vybrat. Pokud řeknete málo, bude vám muset sám napsat o další detaily. Jednou jsem dostal chybové hlášení sestávající z jediné věty. Když jsem se ptal dále, odpověděl uživatel vždy zase jednou větou. Trvalo to týdny, protože jsem informace dostával po jednotlivých větách.
*   _Opatrně se zájmeny._ Neříkejte "to" nebo "okno", pokud není jasné, co tím myslíte. Například: "Spustil jsem Vrlakadizátor. Naběhlo chybové okno, zavřel jsem to, a spadlo to." Zavřel to okno, nebo celý program? To je rozdíl. Lepší je: "Spustil jsem Vrlakadizátor. Naběhlo chybové okno. Když jsem pokusil to okno zavřít, Vrlakadizátor spadnul." Je to delší, ale jasnější.
*   _Přečtěte si, co jste napsali._ Než zprávu odešlete, sami si ji přečtěte. Pokud popisujete posloupnost příkazů, která reprodukuje chybu, zkuste to nejdříve sami provést přesně tak, jak píšete. Třeba jste něco vynechali.

## Shrnutí

*   Smyslem chybového hlášení je umožnit programátorovi spatřit chybu na vlastní oči. Pokud u toho nemůže osobně být, sdělte mu podrobně, jak chybu reprodukovat.
*   Pokud se programátorovi nedaří chybu reprodukovat, popište příznaky chyby. Popište všechno detailně. Popište, co jste viděli. Řekněte, co jste očekávali. Vypište doslovně chybové hlášky, obzvláště pokud obsahují číselné údaje.
*   Provede-li počítač něco neočekávaného, ustaňte v práci. Nedělejte nic, dokud nebudete vědět co. Obzvláště nedělejte nic nebezpečného.
*   I když se pokusíte chybu diagnostikovat sami (což je v pořádku), hlavně popište příznaky chyby.
*   Buďte připraveni poskytnout programátorovi další informace. Kdyby je nepotřeboval, neptal by se; nedělá to proto, aby vás otravoval. Připravte si čísla verzí, budete je potřebovat.
*   Pište jasně. Ať je jasné, co jste chtěli říct, ať je vaše sdělení zcela jednoznačné.
*   A především, vyjadřujte se přesně. Programátoři to mají rádi.

* * *

## Závěr

Fretku ani antilopu jsem nikdy neviděl. Za svou zoologii neručím.