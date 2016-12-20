# Jak efektywnie zgłaszać błędy

_autor: Simon Tatham, profesjonalny programista_

## Wstęp

Każdy, kto napisał program przeznaczony do powszechnego użytku prawdopodobnie otrzyma co najmniej jedno złe zgłoszenie błędu. Zgłoszenia, które nic nie mówią (,,To nie działa!''); zgłoszenia, które nie mają sensu, zgłoszenia, które nie zawierają wystarczających informacji; zgłoszenia, które zawierają błędne informacje. Zgłoszenia problemów, które okazują się być błędami użytkownika; zgłoszenia problemów, które okazują się błędami innych programów; zgłoszenia problemów, które okazują się awariami sieci.

Jest powód dla którego wsparcie jest uznawane za koszmarną robotę, tym powodem są złe zgłoszenia błędów. Jednakże nie wszystkie informacje o znalezionych błędach są niemiłe: kiedy nie zarabiam na życie zajmuję się wolnym oprogramowaniem i czasami otrzymuję cudownie jasne, pomocne i niosące odpowiednią dawkę informacji zgłoszenia błędów.

W tym eseju postaram się sprecyzować co składa się na dobre zgłoszenie błędu. Ideałem byłoby, gdyby każdy człowiek na świecie przeczytał ten esej przed zgłaszaniem komukolwiek jakichkolwiek błędów. Bez wątpienia chciałbym aby każdy zgłaszający mi błędy przeczytał ten tekst.

W skrócie, celem zgłoszenia błędu jest umożliwienie programiście zobaczenia na własne oczy błędnego działania programu. Możesz albo pokazać mu to osobiście, albo dać szczegółowe instrukcje odtworzenia błędu. Jeśli programiście uda się odtworzyć błąd, postara się samemu zebrać dodatkowe informacje potrzebne do poznania przyczyn. Jeśli nie uda mu się go odtworzyć, będzie musiał poprosić Ciebie o zebranie tych informacji dla niego.

W zgłoszeniu staraj się bardzo wyraźnie przedstawić właściwe fakty (,,Byłem przy komputerze i stało się to'') oraz swoje przypuszczenia (,,Myślę, że problemem może być to''). Jeśli chcesz, możesz pominąć przypuszczenia, ale absolutnie nie pomijaj faktów.

Zgłaszasz błąd ponieważ chcesz aby został naprawiony. Nie ma sensu przeklinanie programisty ani celowy brak chęci do współpracy: Twój problem może być winą programisty i być może masz rację złoszcząc się na niego, jednakże błąd zostanie naprawiony szybciej gdy dostarczysz wszystkich informacji, których potrzebuje. Pamiętaj również, że jeśli program jest darmowy oznacza to, że autor dostarcza go z uprzejmości, więc jeśli zbyt wielu ludzi będzie dla niego niemiłych, może przestać być uprzejmym.

## ,,To nie działa.''

Okaż programiście odrobinę wiary w jego inteligencję: jeśli program rzeczywiście wcale nie działa, on prawdopodobnie by to zauważył. A skoro nie zauważył, to znaczy, że u autora działa. Czyli albo robisz coś inaczej niż autor, albo Twoje środowisko jest inne niż jego. Autor potrzebuje informacji; dostarczenie tych informacji jest celem zgłoszenia błędów. Więcej informacji jest prawie zawsze lepsze od mniejszej ich ilości.

Autorzy wielu programów, w szczególności wolnego oprogramowania, publikują listy znanych błędów. Jeśli znajdziesz taką listę warto ją przeczytać aby sprawdzić, czy znaleziony przez Ciebie błąd jest już znany. Jeśli jest, raczej nie ma sensu zgłaszać go ponownie, lecz jeśli myślisz, że jesteś w stanie dostarczyć większej ilości informacji niż w pierwotnym zgłoszeniu, mimo wszystko możesz skontaktować się z autorem. Informacje, których wcześniej nie posiadał być może pomogą mu usunąć błąd z większą łatwością.

Ten esej jest pełny wskazówek. Żadna z nich nie jest regułą. Konkretni programiści mają swoją ulubioną formę zgłoszeń błędów. Jeśli do programu dołączone są wskazówki odnośnie zgłaszania błędów - przeczytaj je. Jeśli wskazówki dołączone do programu stoją w sprzeczności z zawartymi w tym eseju przestrzegaj tych z dokumentacji programu!

Jeśli nie zgłaszasz błędu, a tylko prosisz o pomoc w używaniu programu, powinieneś zaznaczyć gdzie szukałeś już odpowiedzi. (,,Czytałem rozdział 4 i punkt 5.2, lecz nadal nie wiem czy jest to możliwe.'') To pomoże autorowi dowiedzieć się gdzie ludzie spodziewają się znaleźć odpowiedź, aby mógł uczynić dokumentację łatwiejszą w użyciu.

## ,,Pokaż mi.''

Jedną z najlepszych metod zgłaszania błędów jest pokazanie ich programiście. Posadź go przed Twoim komputerem, uruchom jego program i pokaż gdzie ujawnia się błąd. Pozwól mu patrzeć jak uruchamiasz sprzęt, jak uruchamiasz program, jak pracujesz z programem i jak program reaguje na Twoje działania.

Autor zna swój program jak własną kieszeń. Wie którym częściom ufa, a które mogą mieć błędy. Wie intuicyjnie na co uważać. Zanim program zrobi coś jawnie bezsensownego autor może zobaczyć jakiś mały błąd wcześniej, który może dać mu wskazówkę. Jest w stanie obserwować wszystko co dzieje się z komputerem podczas testowej sesji i wybrać dla siebie ważniejsze kawałki.

To jednak może nie wystarczyć. Autor może uznać, że potrzebuje więcej informacji i poprosić o pokazanie tego samego jeszcze raz. Może poprosić o opowiedzenie mu całej procedury, aby mógł odtworzyć błąd ile razy zechce. Może chcieć zmienić trochę procedurę kilka razy, aby przekonać się czy problem występuje tylko w jednym przypadku, czy w całej rodzinie przypadków pokrewnych. Jeśli masz pecha autor może chcieć usiąść na kilka godzin z zestawem narzędzi programistycznych i naprawdę zająć się śledztwem. Najważniejszą rzeczą jest mieć programistę patrzącego na komputer w momencie ujawnienia się błędu. Zwykle, gdy widzi wydarzający się błąd, może od tego zacząć i podjąć próby jego naprawienia.

## ,,Pokaż mi jak pokazać to sobie samemu''

Jesteśmy w erze internetu. To era globalnej komunikacji. To era w której mogę wysłać swój program do kogoś w Rosji używając jednego przycisku, a on może wysłać mi komentarz z tą samą łatwością. Lecz jeśli on ma problem z moim programem nie może posadzić mnie przed swoim komputerem i zademonstrować. ,,Pokaż mi'' jest dobre kiedy jest możliwe, lecz często niewykonalne.

Jeśli musisz zgłosić błąd programiście, który nie może być obecny osobiście, celem pracy jest umożliwienie mu odtworzenia problemu. Chcesz aby programista uruchomił własną kopię programu, zrobił to samo co Ty i spowodował dokładnie taki sam błąd. Gdy jest w stanie zobaczyć problem na własne oczy, jest w stanie sobie z nim poradzić.

Opisz więc dokładnie co zrobiłeś. Jeśli jest to program graficzny opisz które przyciski i w jakiej kolejności naciskałeś. Jeśli jest to program uruchamiany przez wpisanie jakiejś komendy, napisz dokładnie jaką komendę wpisałeś. Jeśli tylko jest to możliwe powinieneś dołączyć dokładny zapis sesji pokazujący jakie komendy wpisałeś i co komputer na to odpowiedział.

Daj programiście wszelkie dane wejściowe o jakich jesteś w stanie pomyśleć. Jeśli program czyta dane z pliku, prawdopodobnie będziesz musiał przesłać kopię tego pliku. Jeśli program komunikuje się z innym komputerem przez sieć, prawdopodobnie nie możesz wysłać kopii tego komputera, ale możesz chociażby powiedzieć jakiego rodzaju jest to komputer i jakiego oprogramowania używa.

## ,,U mnie działa. Więc co jest nie tak?''

Jeśli dasz programiście długą listę danych wejściowych i swoich działań, a on odpali własną kopię programu i żaden błąd nie wystąpi oznacza to, iż nie dałeś wystarczająco dużo informacji. Możliwe, że błąd nie ujawnia się na każdym komputerze; systemy - Twój i autora - mogą się w jakiś sposób różnić. Możliwe również, że nie zrozumiałeś do czego dany program służy i patrzycie na ten sam widok, ale Ty myślisz, że wynik jest zły a autor wie, że jest on dobry.

Opisz więc również co się stało. Powiedz mu dokładnie co zauważyłeś. Powiedz dlaczego uważasz, że to co zobaczyłeś jest błędem oraz opisz to, co spodziewałeś się zobaczyć. Jeśli napiszesz ,,i wtedy się popsuło'' pominiesz bardzo ważne informacje.

Jeśli zobaczyłeś komunikaty o błędach przytocz programiście, dokładnie i z uwagą, jak one brzmiały. One są ważne! Na tym etapie programista jeszcze nie stara się rozwiązać problemu - na razie stara się go znaleźć. Dlatego musi wiedzieć dokładnie co poszło nie tak, a te komunikaty o błędach są najlepszym co może zrobić komputer aby Ci o tym powiedzieć. Zapisz komunikaty, jeśli nie masz innej łatwej możliwości ich zapamiętania. Nie ma sensu zgłaszać, że program wygenerował jakiś komunikat błędu, jeśli nie jesteś w stanie przytoczyć treści tego komunikatu.

W szczególności, jeśli komunikat o błędzie zawiera jakieś liczby, postaraj się aby dotarły one również do programisty. Nawet jeśli Ty nie znasz ich znaczenia nie znaczy to, że one go nie mają. Liczby zawierają wiele informacji zrozumiałych dla programisty i jest bardzo prawdopodobne, że będą zawierały jakąś ważną podpowiedź. Komputer nie zawsze jest w stanie opisać słowami na czym polega błąd, ale stara się jak może przekazać Ci ważne informacje - dlatego w komunikatach błędów czasem znajdują się te liczby.

Na tym etapie programista wykonuje pracę detektywa. Nie wie jeszcze co się stało ani nie może podejść wystarczająco blisko, aby przypatrzeć się samemu, więc szuka wskazówek, które mogą mu to rozjaśnić. Komunikaty błędów, niezrozumiałe ciągi liczb czy nawet niewytłumaczalne opóźnienia są tak ważne, jak odciski palców na miejscu zbrodni. Zatrzymaj je!

Jeśli używasz Uniksa program mógł wyprodukować zrzut pamięci (ang. core dump). Zrzut ten jest szczególnie dobrym źródłem wskazówek, więc go nie wyrzucaj. Z drugiej strony większość programistów nie lubi otrzymywać bez ostrzeżenia wielkich plików zrzutu pocztą elektroniczną, więc zapytaj zanim wyślesz taki plik komukolwiek. Miej również na uwadze, że plik zrzutu pamięci zawiera pełny zapis stanu w jakim znajdował się program: wszystkie ,,sekrety'' (być może program zajmował się właśnie jakimś osobistym listem, albo obrabiał poufne dane) mogą zostać zawarte w tym pliku.

## ,,Wtedy spróbowałem ...''

Jest wiele rzeczy, które możesz zrobić gdy pojawi się błąd. Wiele z nich może pogorszyć sytuację. Moja koleżanka ze szkoły przez pomyłkę usunęła wszystkie swoje dokumenty Worda i zanim poprosiła o pomoc spróbowała reinstalacji Worda, a potem uruchomiła defragmentację dysku. Żadna z tych czynności nie pomogła jej odzyskać plików, a tylko spowodowały takie zamieszanie na dysku, że żaden program do odzyskiwania danych nie był w stanie nic odzyskać. Gdyby tylko dała sobie spokój, być może miałaby szansę.

Tacy użytkownicy są jak przyparta do muru mangusta, która oparta o ścianę widząc pewną śmierć zaglądającą jej w oczy szaleńczo atakuje, ponieważ robienie czegokolwiek musi być lepsze niż nie robienie niczego. Takie zachowanie nie jest odpowiednie do rodzaju problemów generowanych przez komputery.

Zamiast być mangustą bądź antylopą. Gdy antylopa spotyka się z czymś nieprzewidzianym lub przerażającym - zatrzymuje się. Stoi jak słup soli próbując nie przyciągać uwagi, myśląc zarazem o najlepszym co może w danej chwili zrobić. (Gdyby antylopy miały linię wsparcia właśnie w tym momencie by telefonowała.) Gdy już zdecyduje co jest najbezpieczniejszą rzeczą w danych warunkach, po prostu to robi.

Gdy coś idzie nie tak, natychmiast przestań robić cokolwiek. Nie dotykaj żadnych przycisków. Popatrz na ekran, wychwyć wszystko co niestandardowe i zapamiętaj to albo zapisz. Potem np. ostrożnie zacznij naciskać ,,OK'' lub ,,Anuluj'' w zależności od tego, co wydaje sie bezpieczniejsze. Postaraj się wyrobić odruch - gdy komputer wykona coś nieprzewidzianego - zamieraj.

Jeśli uda Ci się wybrnąć z problemu, czy to zamykając błędny program, czy też przez restart komputera, dobrym pomysłem jest próba powtórzenia błędu. Programiści lubią problemy, które mogą odtworzyć więcej niż raz. Szczęśliwi programiści naprawiają błędy szybciej i efektywniej.

## ,,Wydaje mi się, że modulacja tachionowa jest źle spolaryzowana.''

Nie tylko nieprogramiści zgłaszają błędy w zły sposób. Niektóre spośród najgorszych zgłoszeń jakie widziałem pochodzą od programistów, a nawet od dobrych programistów.

Pracowałem kiedyś z innym programistą, który wciąż znajdował błędy we własnym kodzie i próbował je naprawiać. Czasami trafiał na błąd, którego nie mógł rozwiązać i prosił mnie o pomoc. ,,Co się stało?'' pytałem. Odpowiadał mówiąc co według niego musi zostać naprawione.

To działało, gdy jego opinia była słuszna. Znaczyło to, że wykonał już połowę roboty i mogliśmy ją we dwójkę dokończyć. Było to efektywne i użyteczne.

Ale całkiem często mylił się. Pracowaliśmy długi czas próbując ustalić czemu pewna konkretna część programu dawała nieprawidłowe wyniki dochodząc wreszcie do wniosku, że tak nie było, że przez pół godziny śledziliśmy kawałek doskonałego kodu, a rzeczywisty problem leżał zupełnie gdzie indziej.

Jestem pewien, że nie zachowałby się tak przy lekarzu. ,,Doktorze, potrzebuję recepty na hydrojojodynę''. Ludzie wiedzą, że nie tak należy rozmawiać z lekarzem. Opisujesz symptomy, właściwe dolegliwości, bóle, wysypki, gorączki, a diagnozę i sugestie co do dalszego postępowania pozostawiasz lekarzowi. Inaczej lekarz wyprosi Cię z diagnozą: hipohondryk - właściwie słusznie.

Tak samo jest z programistami. Dostarczenie własnej diagnozy czasem może być przydatne, ale zawsze opisz symptomy. Diagnoza jest nieobowiązkowym dodatkiem, ale na pewno nie alternatywą dla opisu symptomów. Tak samo wysłanie modyfikacji kodu źródłowego jest użytecznym dodatkiem do zgłoszenia błędu, lecz nie jego substytutem.

Jeśli programista poprosi o dodatkowe informacje nie zmyślaj ich! Ktoś kiedyś zgłosił mi błąd, a ja poprosiłem go o wykonanie komendy, o której wiedziałem, że nie ma prawa zadziałać. Zrobiłem tak, aby przekonać się, który z dwóch różnych komunikatów błędu ona wywoła. Poznanie tego komunikatu dałoby mi użyteczną wskazówkę. Ale on jej nie wykonał, tylko odpisał mi ,,Nie, to nie działa''. Przekonanie go, aby ją jednak wykonał zajęło mi trochę czasu.

Użycie własnej inteligencji aby pomóc programiście jest dobre. Nawet jeśli Twoje domysły są błędne, programista powinien być wdzięczny, że chociaż spróbowałeś uczynić jego życie łatwiejszym. Ale pamiętaj również o opisaniu symptomów, gdyż inaczej możesz to życie uczynić zdecydowanie trudniejszym.

## ,,To zabawne, zrobił to przed chwilą.''

Powiedz ,,nieregularny problem'' programiście i obserwuj jego twarz. Łatwe problemy, to te w których przez wykonanie prostej sekwencji czynności można uzyskać ujawnienie się błędu. Programista może wtedy powtarzać te czynności w ściśle kontrolowanych warunkach testowych i bardzo dokładnie oglądać wyniki. Zbyt wiele jednak problemów wygląda inaczej. Znajdą się programy, które będą ujawniały błędy raz w tygodniu, lub jeszcze rzadziej, albo nigdy, gdy uruchamiasz je przy programiście, natomiast zawsze gdy gonią Cię terminy.

Większość nieregularnych błędów tak naprawdę nie jest nieregularna. Większość z nich ma gdzieś zaszytą logikę. Niektóre z nich mogą wystąpić gdy maszynie brakuje pamięci, albo gdy inny program próbuje zmodyfikować kluczowy plik w nieodpowiednim momencie, albo mogą ujawiniać się tylko w pierwszej połowie każdej godziny! (Naprawdę taki widziałem.)

Jeśli więc jesteś w stanie odtworzyć błąd, ale programista nie, jest bardzo prawdopodobne, że wasze komputery w jakiś sposób się różnią i właśnie ta różnica jest przyczyną problemu. Miałem kiedyś program, którego okno zwijało się w małą kulkę w lewym, górnym rogu ekranu; siedziało tam i się dąsało. Ale tylko w rozdzielczości 800x600; zachowywało się normalnie na moim ekranie pracującym w 1024x768.

Programista będzie chciał poznać wszystko czego jesteś w stanie dowiedzieć się o problemie. Wypróbuj program na przykład na innej maszynie. Sprawdź dwa-trzy razy i przekonaj się jak często zawodzi. Jeśli błąd ujawnia się gdy wykonujesz jakąś poważną pracę, ale nie gdy próbujesz go zademonstrować, może to oznaczać, że długi czas pracy, albo duże pliki powodują problem. Postaraj się zapamiętać jak najwięcej szczegółów odnośnie tego co robiłeś gdy błąd się ujawnił i jeśli widzisz jakąś regularność - wspomnij o tym. Cokolwiek, co jesteś w stanie zauważyć może być pomocne. Nawet jeśli jest to tylko prawdopodobna zbieżność (jak np. ,,ma tendencję do częstszego wykładania się, gdy uruchomiony jest Emacs''), może nawet niedająca bezpośrednich wskazówek, ale mogąca pomóc programiście odtworzyć problem.

Najważniejsze dla programisty jest upewnienie się, czy ma do czynienia z prawdziwie nieregularnym problemem, czy raczej z zależącym od sprzętu. Będzie chciał poznać wiele szczegółów dotyczących Twojego komputera, aby mógł ustalić czym różni się od jego. Wiele z tych szczegółów będzie zależało od konkretnego programu, ale na pewno musisz być przygotowany na podanie numerów wersji. Wersji samego programu, ale i systemu operacyjnego i prawdopodobnie pozostałych programów związanych z problemem.

## ,,Więc, załadowałem dysk do Windows ...''

Jasne wyrażanie się jest niezbędne przy zgłaszaniu błędów. Jeśli programista nie może zrozumieć co miałeś na myśli, to równie dobrze mógłbyś nic nie pisać.

Powiadomienia o błędach otrzymuję z całego świata. Wiele z nich pochodzi od ludzi, dla których angielski nie jest językiem ojczystym i wielu z nich przeprasza za swoją kiepską znajomość tego języka. Ogólnie, zgłoszenia z przeprosinami za kiepski angielski są zwykle bardzo jasne i pomocne. Większość niejasnych zgłoszeń pochodzi od ludzi posługujących się angielskim na codzień, którzy zakładają, że ich zrozumiem nawet gdy nie będą się starać aby wyrażać się jasno czy precyzyjnie.

*   Bądź konkretny. Jeśli jest kilka dróg do jednego celu, powiedz której z nich użyłeś. ,,Otworzyłem'' może oznaczać ,,Kliknąłem na Otwórz'' lub ,,Nacisnąłem Alt+O''. Sprecyzuj co zrobiłeś. Czasem to ma znaczenie.
*   Bądź gadatliwy. Przekazuj raczej więcej niż mniej informacji. Jeśli powiesz za dużo programista może część zignorować. Jeśli powiesz za mało, będzie musiał zadawać dodatkowe pytania. Kiedyś otrzymałem powiadomienie o błędzie w postaci jednego zdania; za każdym razem gdy prosiłem o dodatkowe informacje zgłaszający odpowiadał kolejnym jednym zdaniem. Kilka tygodni zajęło mi dojście do kompletu użytecznych informacji.
*   Uważaj na zaimki. Nie używaj słów typu ,,to'' czy ,,to okno'' gdy nie jest pewne co mogą znaczyć. Rozważ taki przykład: ,,Uruchomiłem środowisko Foo. Pojawiło się okienko z błędem. Chciałem je zamknąć i się wyłożyło.'' Nie jest jasne co chciał zamknąć użytkownik, czy okienko błędu, czy całe środowisko. A to ma znaczenie. Zamiast tego mógbyś napisać ,,Uruchomiłem środowisko Foo. Pojawiło się okienko z błędem. Chciałem zamknąć okienko z błędem, ale środowisko się wyłożyło.'' Jest to dłuższa, zawierająca więcej powtórzeń wersja, jednakże jaśniejsza i trudniejsza do błędnego zinterpretowania.
*   Przeczytaj to co napisałeś. Jeszcze raz przeczytaj całe zgłoszenie i zastanów się, czy jest dla Ciebie jasne. Upewnij się, że opisałeś sekwencję czynności, która powinna spowodować wystąpienie błędu. Sprawdź ją jeszcze raz, aby upewnić się, że nie pominąłeś żadnego kroku.

## Podsumowanie

*   Podstawowym celem zgłoszenia błędu jest umożliwienie programiście zobaczenia go na własne oczy. Jeśli nie możesz osobiście mu tego pokazać, napisz dokładną instrukcję, aby mógł samemu spowodować wystąpienie błędu.
*   Na wypadek gdy programiście nie uda się zreprodukować błędu, drugą najważniejszą sprawą jest opisanie co zachowało się nie tak jak powinno. Opisz wszystko ze szczegółami. Opisz co zobaczyłeś, a co spodziewałeś się osiągnąć. Zapisz komunikaty o błędach, szczególnie jeśli zawierają jakieś liczby.
*   Gdy komputer zrobi coś nieoczekiwanego - zamieraj. Nie rób nic aż się uspokoisz. Absolutnie nie rób czegoś, o czym myślisz, że może być niebezpieczne.
*   Jeśli uważasz, że potrafisz, to postaraj się zdiagnozować problem samemu. Nawet jeśli to zrobisz, nie zapomnij opisać również symptomów.
*   Bądź gotów aby dostarczyć dodatkowych informacji, gdy autor Cię o to poprosi. Gdyby ich nie potrzebował, to by o nie nie pytał. Programiści nie grymaszą bez powodu. Miej w pogotowiu numery wersji, gdyż prawdopodobnie będą potrzebne.
*   Wyrażaj się jasno. Pisz co masz na myśli i upewnij się, że nie da się tego błędnie zinterpretować.
*   Przede wszystkim bądź precyzyjny. Programiści lubią precyzję.

* * *

_Wyjaśnienie_: Właściwie to nigdy nie widziałem ani mangusty ani antylopy. Moja wiedza zoologiczna może nie być ścisła.