# Fehlerberichte - wie Sie Softwarefehler melden sollten

von _Simon Tatham, Berufsprogrammierer und Programmierer freier Software_

## Einleitung

Jeder, der Software für die Allgemeinheit geschrieben hat, wird wahrscheinlich schon einmal einen schlechten Fehlerbericht erhalten haben. Nichts sagende Berichte ("Es geht nicht!"), Berichte, die keinen Sinn ergeben, Berichte, die einem nicht genug Informationen geben, Berichte, die einem _falsche_ Informationen geben. Berichte von Problemen, die sich schließlich als Fehlbedienung durch den Benutzer herausstellen, oder bei denen das Problem bei einem anderen Programm liegt oder die auf Netzwerkfehler zurückzuführen sind.

Es gibt einen Grund, warum die Arbeit für eine Anwenderhotline als Horror angesehen wird und dieser Grund sind schlechte Fehlerberichte. Andererseits sind nicht alle Fehlerberichte unangenehm. Wenn ich nicht gerade meinen Lebensunterhalt verdiene, so entwickle und pflege ich freie Software und manchmal erhalte ich wunderbar klare, hilfreiche, _informative_ Fehlerberichte.

In dieser Anleitung werde ich versuchen, Ihnen klarzumachen, was einen guten Fehlerbericht ausmacht. Meine Idealvorstellung wäre es, dass jeder diese Anleitung liest, bevor er irgendwem irgendwelche Fehlerberichte schickt. Auf alle Fälle hätte ich es gerne, dass Leute, die _mir_ Fehlerberichte senden, das hier lesen.

Kurz gefasst ist das Ziel eines Fehlerberichts, es dem Programmierer zu ermöglichen, zu sehen, wie das Programm Fehler macht. Entweder können Sie es ihm persönlich zeigen oder ihm sorgfältige und genaue Informationen geben, wie er es dazu bringt, den Fehler zu machen. Wenn er das schafft, so wird er versuchen weitere Informationen zu sammeln, bis er die Ursache kennt. Wenn er das nicht schafft, so muss er sie bitten die Informationen für ihn zu sammeln.

Versuchen Sie genau auseinander zu halten, was die tatsächlichen Vorkommnisse waren („Ich war am Rechner und dies und das passierte.“) und was Ihre Interpretationen und Spekulationen sind („Ich _denke_ es könnte an Folgendem liegen ...“). Wenn Sie es nicht wünschen, so brauchen Sie Ihre Spekulationen nicht mitzuteilen, aber bitte beschreiben Sie alle tatsächlichen Vorkommnisse.

Wenn Sie einen Fehler melden, dann weil Sie ihn repariert haben wollen. Es macht keinen Sinn, den Programmierer zu verfluchen oder absichtlich möglichst wenig hilfreich zu sein: Es mag der Fehler des Programmierers sein, dass Sie ein Problem haben und Sie ärgern sich möglicherweise vollkommen zu Recht über ihn, aber der Fehler wird schneller behoben werden, indem Sie ihm dadurch helfen, dass Sie ihm alle Informationen geben, die er braucht. Übrigens: Wenn es sich um freie Software handelt, haben Sie sie diese aufgrund der Nettigkeit des Autors bekommen. Wenn zu viele Leute sich ihm gegenüber ungehobelt aufführen, lässt diese Nettigkeit vielleicht nach.

## „Es geht nicht.“

Gehen Sie davon aus, dass der Programmierer kein Volltrottel ist: Wenn das Programm überhaupt nicht funktionieren würde, so wäre es ihm aufgefallen. Da das nicht der Fall ist, wird es bei ihm wohl gehen. Also tun Sie etwas anders oder die Arbeitsumgebung bei Ihnen ist anders. Er braucht Information; diese Information zur Verfügung zu stellen ist der Zweck eines Fehlerberichts. Mehr Information ist immer besser als weniger.

Von vielen Programmen, insbesondere von freien, gibt es eine veröffentlichte Liste der bekannten Fehler. Wenn Sie solch eine Liste finden können, so sollten Sie sie lesen um festzustellen ob der von Ihnen gefundenen Fehler darauf schon vorkommt. Wenn er schon bekannt ist, so ist er es wahrscheinlich nicht wert, dass Sie ihn wieder berichten,. Wenn Sie aber meinen, Sie haben mehr Informationen als in der Fehlerliste schon vorhanden, wäre es vielleicht günstig, den Programmierer trotzdem zu benachrichtigen. Er kann den Fehler möglicherweise eher beheben, wenn Sie ihm Informationen geben, die er noch nicht hatte.

Diese Anleitung beschreibt einige Richtlinien. Keine von ihnen ist eine eiserne Regel. Verschiedene Programmierer haben verschiedene Vorlieben wie man Fehler berichten soll. Wenn das Programm seine eigenen Richtlinien hierfür mitbringt, so lesen Sie sie diese und wenn sie dem widersprechen, was hier steht, richten Sie sich nach den Richtlinien die Sie mit dem Programms erhielten!

Wenn Sie keinen Fehler berichten sondern nur um Hilfe zur Programmbedienung bitten, sollten Sie sagen, wo Sie schon überall nach einer Antwort gesucht haben. („Ich habe Kapitel 4 durchgelesen und den Abschnitt 5.2, konnte aber nichts finden, was darauf hindeutet ob das möglich ist oder nicht.“) Dadurch erfahren die Programmierer, wo die Anwender die Antwort auf ihre Fragen erwarten und sie können die Dokumentation besser gestalten.

## „Zeigen Sie es mir.“

Eine der besten Methoden einen Fehler zu berichten ist, ihn dem Programmierer zu zeigen. Zitieren Sie ihn zu Ihrem Rechner, starten Sie das Programm und zeigen Sie, was schief ging. Lassen Sie ihn den Start ihres Rechners beobachten, wie Sie das Programm bedienen, was Sie genau tun und wie das Programm darauf reagiert.

Programmierer kennen ihre Software wie ihre Westentaschen. Sie wissen, welche Teile am vertrauenswürdigsten sind und welche am wahrscheinlichsten aussetzen. Sie wissen intuitiv, wonach sie Ausschau zu halten haben. Schon lange vor dem Zeitpunkt, zu dem das Programm offensichtlichen Unfug macht, ist ihnen vielleicht ein subtiler Fehler aufgefallen, der einen wertvollen Hinweis liefert. Sie können alles, was der Rechner während des Testlaufs macht, beobachten und diese wichtigen Details selbst herausfinden.

Vielleicht reicht das aber noch nicht. Möglicherweise wollen sie mehr Informationen und bitten Sie, ihnen das Ganze noch einmal vorzuführen. Oder Sie wollen von Ihnen, dass Sie ihnen dabei zusehen und Anleitung geben, so dass sie selbst den Fehler erzeugen können, so oft sie das wollen. Vielleicht versuchen sie den genauen Ablauf einige Mal zu ändern, um zu sehen, ob das Problem nur ein einem speziellen Fall von vielen ähnlichen auftritt. Wenn Sie Pech haben, belegen sie vielleicht ihren Computer einige Stunden mit Beschlag, um mit Hilfe spezieller Entwicklerwerkzeuge dem Problem _richtig_ zu Leibe zu rücken. Aber das Wichtigste ist, dass die Programmierer es sehen, wenn der Computer Unsinn macht. Sobald sie das Problem sehen, können sie von diesem Anhaltspunkt aus meist daran arbeiten es zu beheben.

## „Zeigen Sie mir, wie ich es mir selbst zeigen kann.“

Wir haben das Zeitalter des Internets und der weltweiten Kommunikation. Heutzutage kann ich meine Software mit einem Knopfdruck nach Russland schicken und der Empfänger kann mir genauso leicht seine Kommentare senden. Wenn er aber ein Problem mit meinem Programm hat kann ich mich _nicht_ vor seinen Rechner stellen, während der Fehler passiert. „Zeigen Sie es mir“ ist eine gute Devise, wenn das geht, aber oft geht es nicht.

Wenn sie einen Fehlerbericht für einen Programmierer verfassen, der nicht anwesend sein kann, so versuchen Sie es ihm zu ermöglichen, den Fehler _nachzuvollziehen_. Ihr Ziel ist, dass der Programmierer seine Kopie des Programms laufen lässt, die selben Dinge macht, wie Sie und es bei ihm auf die selbe Weise schief geht. Wenn er das Problem vor seinen eigenen Augen sieht, kann er sich dessen annehmen.

Teilen Sie alles, was sie tun, ganz exakt mit. Wenn es ein Programm mit einer graphischen Benutzeroberfläche ist, teilen Sie mit, welche Knöpfe Sie gedrückt haben und in welcher Reihenfolge. Wenn Sie einen Befehl eingegeben haben, sagen Sie, was Sie genau getippt haben. Wenn möglich erstellen Sie ein genaues Skript aller Dinge, die Sie getan haben und wie der Computer darauf reagierte.

Geben Sie den Programmierern alle Informationen, die Sie haben. Wenn das Programm aus einer Datei liest, müssen Sie wahrscheinlich eine Kopie der Datei zur Verfügung stellen. Wenn das Programm in einem Netzwerk auf einen anderen Computer zugreift so können Sie zumindest sagen, welche Art von Computer das ist und – falls Sie es wissen – welche Programme darauf laufen.

## „Bei mir geht's. Wo ist das Problem?”

Wenn Sie den Programmierern eine lange Liste Ihrer Eingaben und der Ausgaben des Rechners geben, aber bei deren Computer alles funktioniert, so haben Sie noch nicht genug Informationen zur Verfügung gestellt. Vielleicht tritt das Problem nicht bei jedem Rechner auf. Deren System und das Ihre unterscheiden sich vielleicht teilweise. Möglicherweise haben Sie die Funktionsweise des Programms missverstanden und sie sehen alle dieselbe Anzeige, nur sind Sie der Auffassung, dass sie falsch ist und die Programmierer wissen, dass es stimmt.

Beschreiben Sie also auch genau, was geschah. Sagen Sie ihnen, was Sie sehen. Sagen Sie ihnen, warum Sie das, was Sie sehen für falsch halten, besser noch beschreiben Sie genau, was sie eigentlich zu sehen erwarteten. Wenn sie einfach sagen „und das hat nicht funktioniert”, haben Sie eine wichtige Information ausgelassen.

Wenn Fehlermeldungen erscheinen, so sagen Sie den Programmierern genau und detailliert, welche das waren. Diese Meldungen _sind_ wichtig! Zu diesem Zeitpunkt versuchen die Programmierer noch gar nicht den Fehler zu beheben, sondern nur herauszufinden, was der Fehler eigentlich ist. Sie müssen erfahren, was falsch lief und diese Meldungen sind der beste Versuch des Rechners, Ihnen das mitzuteilen. Schreiben Sie die Fehler auf, wenn Sie sich sonst nicht daran erinnern können, aber es macht keinen Sinn einen Fehler zu berichten, wenn Sie nicht sagen können, wie die Fehlermeldung lautete.

Insbesondere, wenn die Fehlermeldung eine Nummer ausgibt, geben Sie diese Nummer an den Programmierer _weiter_. Nur dass Sie in ihr keinen Sinn erkennen können, heißt nicht, dass sie keinen Sinn macht. Nummern enthalten alle Arten wichtiger Informationen die ein Programmierer verstehen kann, und es ist wahrscheinlich, dass sie wichtige Hinweise enthalten. Fehlermeldungen haben Nummern, weil der Computer zu verwirrt ist, den Fehler in Worten zu berichten, aber er versucht das Beste zu tun, um Ihnen irgendwie diese Information zu vermitteln.

Zu diesem Zeitpunkt ist Programmieren im Wesentlichen Detektivarbeit. Die Programmierer wissen nicht, was passierte und sie kommen nicht nahe genug an das Problem heran, um es selbst zu beobachten, also suchen Sie nach Hinweisen, die sie auf die richtige Spuren führen können. Fehlermeldungen, unverständliche Aneinanderreihungen von Nummern und auch unerwartetes Stocken des Programms sind alles Fingerabdrücke am Tatort des Verbrechens. Bewahren Sie sie auf!

Wenn Sie Unix verwenden, hat das Programm möglicherweise einen Core Dump erzeugt. Core Dumps sind eine besonders nützliche Quelle von Hinweisen, also werfen Sie sie nicht weg. Andererseits mögen es die meisten Programmierer nicht, wenn sie ohne Vorwarnung riesige Core Dateien geschickt bekommen, also fragen Sie bitte, bevor Sie sie jemandem zusenden. Außerdem sollten Sie wissen, dass die Core Datei eine komplette Aufzeichnung des Stands des Programms enthält: Alle möglichen „Geheimnisse” befinden sich in der Core Datei (möglicherweise hat das Programm gerade eine persönliche Nachricht transportiert oder vertrauliche Daten bearbeitet).

## „Dann habe ich noch versucht”

Es gibt eine Menge Dinge, die Sie tun können, wenn eine Fehler oder eigentümliches Verhalten auftritt. Etliche dieser Dinge verschlimmern das Problem. Eine Schulfreundin löschte versehentlich all ihre Word Dokumente und bevor sie einen Experten rief, versuchte sie Word neu zu installieren und dann führte sie Defrag aus. Nichts davon war hilfreich dabei, ihre Dateien wiederzubeleben und sie sortierte damit ihre Festplatte so um, dass kein Undelete Programm auf der Welt mehr in der Lage gewesen wäre irgendetwas zu retten. Hätte sie nichts getan, so hätte sie eine Chance gehabt.

Anwender reagieren wie eine in die Ecke gedrängte Manguste. Mit dem Rücken zur Wand und dem sicheren Tod ins Auge blickend greift sie wie wildgeworden an, weil etwas zu tun besser sein muss, als nichts zu tun. Das ist keine gute angepasste Reaktion auf die Art von Problemen, die Computer verursachen.

Anstatt wie eine Manguste sollten Sie sich wie eine Antilope verhalten. Wenn eine Antilope etwas Unerwartetem, Furchteinflößendem gegenübersteht, so rührt sie sich nicht vom Fleck. Sie bleibt vollkommen unbeweglich und versucht keine Aufmerksamkeit auf sich zu ziehen, während sie nachdenkt, was zu tun wohl das Beste sei. (Wenn Antilopen telefonische Produktunterstützung hätten, würden sie zu diesem Zeitpunkt telefonieren.) Dann, sobald sie sich entschieden hat, was das Sicherste ist, tut sie es.

Wenn etwas schief läuft, hören Sie sofort auf _irgendetwas_ zu tun. Fassen Sie überhaupt keine Taste mehr an. Schauen Sie sich die Bildschirmausgabe an, suchen Sie nach allem, was außergewöhnlich aussieht und merken Sie es sich oder schreiben Sie es auf. Dann können Sie möglicherweise vorsichtig dazu übergehen, „OK” oder „Abbrechen” zu drücken, was immer Ihnen am Sichersten erscheint. Versuchen Sie, dieses Verhalten in Fleisch und Blut übergehen zu lassen – wenn der Computer etwas Unerwartetes tut, rühren Sie sich nicht.

Wenn Sie es schaffen, sich aus der misslichen Lage zu befreien, sei es durch Schließen des Programms oder durch Neustart Ihres Computers, wäre es eine gute Sache zu versuchen, den Fehler nochmals auftreten zu lassen. Programmierer mögen Probleme die sie öfter als einmal erzeugen können. Glückliche Programmierer beheben Fehler schneller und effektiver.

## „Vermutlich ist die Polarisierung der Tachyonenmodulation falsch”

Es ist nicht so, dass nur Nicht-Programmierer schlechte Fehlerberichte schreiben. Einige der fürchterlichsten Fehlerberichte die ich je gesehen habe kamen von Programmierern und noch dazu von guten Programmierern.

Ich hatte einen Kollegen, der häufig Fehler in seinem Code fand und sie zu reparieren versuchte. Wenn er auf einen Fehler stieß, den er nicht beheben konnte, rief er mich zu Hilfe. „Was funktioniert nicht?”, fragte ich. Er antwortete indem er mir seine augenblickliche Meinung schilderte, was das Problem verursacht habe.

Das funktionierte wunderbar, wenn seine augenblickliche Meinung richtig war. Er hatte dann schon die halbe Arbeit getan und wir waren in der Lage es gemeinsam zu Ende zu bringen. Es war effizient und nützlich.

Aber oft lag er auch falsch. Wir versuchten dann einige Zeit herauszufinden, warum ein bestimmter Teil des Programms falsche Daten erzeugte, nur um schließlich zu erkennen, dass er das gar nicht tat. Wir hatten eine halbe Stunde einwandfrei funktionierenden Code untersucht und das wirkliche Problem lag ganz wo anders.

Ich bin mir sicher, bei einem Arzt würde er das nicht tun. „Herr Doktor, ich denke ich habe Parkinson”. Die Leute wissen, dass man sich einem Arzt gegenüber nicht so verhält. Man beschreibt die Symptome, die tatsächlichen Beschwerden, das Unwohlsein und die Probleme, die Schmerzen und Ausschläge und das Fieber und überlässt dem Arzt die Diagnose, was dies verursacht. Andernfalls hält Sie der Arzt für einen Hypochonder oder einem Spinner und das nicht zu Unrecht.

Genauso verhält es sich mit Programmierern. Es mag manchmal hilfreich sein, wenn Sie Ihre eigene Diagnose anführen, aber listen Sie immer auch die Symptome auf. Die Diagnose ist etwas Zusätzliches und keine Alternative zum Angeben der Symptome. Auch das Senden einer Änderung für den Code um das Problem zu beheben ist eine nützliche Zusatzangabe aber kein angemessener Ersatz für eine Fehlerbeschreibung.

Wenn die Programmierer um Zusatzinformationen bitten, so erfinden Sie diese nicht einfach! Einmal berichtete mir jemand einen Fehler und ich bat ihn ein Kommando auszuprobieren, von dem ich wusste, dass es nicht funktionieren würde. Ich wollte wissen, welche von zwei möglichen Fehlermeldungen er erhalten würde. Dieses Wissen konnte mir einen wichtigen Hinweis geben. Aber er versuchte es nicht, sondern schrieb mir nur zurück, „Nein, das wird nicht gehen.” Ich brauchte etliche Zeit, bis ich ihn überzeugt hatte, es wirklich auszuprobieren.

Es ist wunderbar, wenn Sie Ihre Intelligenz dazu benutzen wollen, dem Programmierer zu helfen. Auch wenn Ihre Schlüsse falsch sind, sollte der Programmierer dankbar sein, dass Sie wenigstens _versucht_ haben, sein Leben zu erleichtern. Aber berichten Sie auch die Symptome, sonst könnte es passieren, dass Sie es stattdessen erschweren.

## „Ist ja lustig. Gerade eben hat’s noch nicht funktioniert”

Sie brauchen nur „sporadisch auftretender Fehler” zu sagen und schon bekommt jeder Programmierer ein langes Gesicht. Die Fehler, die durch eine einfache Folge von Handlungen hervorgerufen werden können, sind leicht. Der Programmierer kann die Handlungen unter gut kontrollierten Bedingungen wiederholen und im Detail beobachten, was geschieht. Zu viele Probleme sind aber nicht von dieser Art: Es gibt Programme, die einmal in der Woche ausfallen oder alle heiligen Zeiten oder nie, wenn man sie in Anwesenheit eines Programmierers verwendet, aber immer wenn ein Abgabetermin näher rückt.

Die meisten sporadisch auftretenden Fehler treten nicht wirklich zufällig auf. Meistens gibt es irgendwo ein verborgenes System. Manche treten auf, wenn dem Rechner der Speicher ausgeht, manche wenn ein anderes Programm im falschen Augenblick eine wichtige Datei verändert und manche nur in der ersten halben Stunde jeder vollen Stunde. (So etwas ist mir tatsächlich begegnet.)

Wenn Sie den Fehler auftreten lassen können, der Programmierer aber nicht, so kann es darin liegen, dass ihre Rechner verschieden sind und diese Verschiedenheit das Problem verursacht. Ich hatte einmal ein Programm, dessen Fenster sich sich zu einem Fleck in der linken oberen Bildschirmecke zusammenzog, sich dort festbiss und einem _auf die Nerven ging_. Aber das tat es nur bei einer Bildschirmauflösung von 800x600; auf meinem 1024x768 Monitor funktionierte es problemlos.

Die Programmierer werden alles wissen wollen, was Sie über das Problem herausfinden konnten. Versuchen Sie es etwa auch auf einem anderen Computer. Versuchen Sie es zwei- oder dreimal, um zu erfahren, wie oft es fehlschlägt. Wenn es schief geht, wenn Sie ernsthaft arbeiten, aber nicht, wenn Sie versuchen das Problem zu zeigen, könnte es sein, dass lange Laufzeit oder die Bearbeitung großer Dateien die Ursache ist. Versuchen Sie sich an so viel Details, dessen was Sie taten, als es fehlschlug, wie nur möglich zu erinnern und wenn Sie meinen, darin eine Regelmäßigkeit zu erkennen, so sagen Sie es bitte. Alles was sie sagen können, kann von Nutzen sein. Selbst wenn es nur eine ungefähre Ahnung ist (wie etwa „es scheint eher abzustürzen, wenn Emacs läuft”). Es ist vielleicht kein direkter Hinweis auf das Problem, aber es könnte dem Programmierer helfen es nachzuvollziehen.

Vor allem werden die Programmierer sicher wissen wollen, ob sie es mit einem Fehler zu tun haben, der nur sporadisch oder nur auf bestimmten Computern auftritt. Sie werden viele Details über Ihren Computer wissen wollen, um herauszufinden, worin er sich von ihrem unterscheidet. Welche Details gewünscht werden, wird stark vom verwendeten Programm abhängen, aber auf jeden Fall sollten Sie die Versionsnummer angeben., sowohl die Versionsnummer des Programms, als auch die Versionsnummer des Betriebssystems und wahrscheinlich die Versionsnummern von allen anderen Programmen, die mit dem Problem zu tun haben.

## „Dann bin ich in die Diskette reingegangen . . .”

Sich klar auszudrücken ist das Wichtigste bei einem Fehlerbericht. Wenn die Programmierer nicht wissen, was sie meinen, hätten Sie genauso gut gar nichts sagen können.

Ich bekomme Fehlerberichte von überall her in der Welt. Viele Berichterstatter haben nicht Englisch als Muttersprache und von diesen entschuldigen sich viele für ihr schlechtes Englisch. Im Großen und Ganzen sind die Fehlerberichte mit den Entschuldigungen für schlechtes Englisch ziemlich klar und nützlich. Die meisten schwammigen Fehlerberichte kommen von Englischsprachigen, die annehmen, dass ich sie schon verstehen werde, auch wenn sie keinerlei Anstrengung unternehmen, klar und genau zu schreiben.

*   _Seien Sie genau_. Wenn man etwas auf zwei verscheiden verschiedene Arten machen kann, dann sagen Sie, wie Sie es gemacht haben. „Ich habe es geöffnet” kann heißen „Ich habe auf Öffnen geklickt” oder „Ich habe STRG-O gedrückt”. Sagen Sie, was Sie taten. Manchmals ist es wichtig.

*   _Seien Sie geschwätzig_. Führen Sie lieber zu viel, als zu wenig Informationen an. Wenn Sie zu viel sagen, kann der Programmierer einiges unberücksichtigt lassen. Wenn Sie zu wenig sagen, muss er auf Sie zukommen und Sie ausfragen. Einmal erhielt ich einen Fehlerbericht, bestehend aus einem einzigen Satz. Jedes mal, wenn ich zurückfragte, bekam ich als Antwort einen weiteren einzigen Satz. Ich brauchte mehrere Wochen, um so viel Information zu sammeln, dass es mir weiterhalf, da die Information nur satzweise eintröpfelte.

*   _Seien Sie vorsichtig mit Pronomen_. Benutzen Sie nicht Worte wie „es” oder „das Fenster”, wenn es nicht klar ist, was gemeint ist. Betrachten Sie folgendes Beispiel: „Ich startete die FooApp Anwendung. Sie brachte in einem Fenster eine Warnung. Ich versuchte sie zu schließen und sie stürzte ab.” Es ist nicht klar, was der Anwender zu schließen versuchte. Versuchte er die Warnung zu schließen oder die ganze FooApp Anwendung? Das macht einen Unterschied. Stattdessen könnte man schreiben „Ich startete die FooApp Anwendung, welche eine Warnung in einem Fenster brachte. Ich versuchte die Warnung zu schließen und die FooApp Anwendung stürzte ab.” Das ist länger und enthält Wiederholungen aber auch klarer und nicht so leicht misszuverstehen.

*   _Lesen Sie, was Sie schreiben_. Lesen Sie sich den Bericht selbst vor und beurteilen Sie, ob es für _Sie_ klar ist. Wenn Sie eine Liste von Handlungen erstellt haben, die das Fehlverhalten heraufbeschwören, so gehen Sie sie einmal selbst durch, um herauszufinden, ob Sie nicht einen Schritt vergessen haben.

## Zusammenfassung

*   Das Hauptziel eines Fehlerberichts ist, es, den Programmierern, den Fehler mit den eigenen Augen sehen zu lassen. Wenn sie nicht da sind und das nicht geht, so sollten Sie genaue Anweisungen geben, wie sie den Fehler hervorrufen können.

*   Falls das nicht klappt und die Programmierer den Fehler _nicht_ nachvollziehen können, ist das zweite Ziel, genau zu beschreiben, was schief ging Beschreiben Sie jedes Detail. Beschreiben Sie, was Sie sahen und auch, was Sie zu sehen erwarteten. Schreiben Sie die Fehlermeldungen auf, _insbesondere_ dann, wenn sie Nummern enthalten.

*   Wenn Ihr Computer etwas Unerwartetes tut, tun Sie _nichts_. Tun Sie überhaupt nichts, bis Sie ruhig sind und tun Sie nichts, was Sie für gefährlich halten.

*   Versuchen Sie ruhig, das Problem selbst zu diagnostizieren, wenn Sie das für möglich halten, aber Sie sollten trotzdem auch immer die Symptome des Ausfalls berichten.

*   Geben Sie weitere Informationen heraus, wenn die Programmierer danach fragen. Wenn sie sie nicht brauchen würden, würden sie nicht fragen. Sie führen sich nicht absichtlich komisch auf. Halten Sie Versionsnummern bereit, weil sie wahrscheinlich gebraucht werden.

*   Schreiben Sie klar. Sagen Sie, was Sie meinen und stellen Sie sicher, dass es nicht falsch verstanden werden kann.

*   Und vor allem, _seien Sie genau_. Programmierer mögen Genauigkeit.

* * *

_Warnhinweis:_ Ich habe nie eine Manguste oder eine Antilope beobachtet. Meine zoologischen Ausführungen sind möglicherweise nicht korrekt.