# Cómo informar de fallos de forma efectiva

_por Simon Tatham, programador profesional y de software libre_

## Introducción

Cualquiera que haya escrito software para uso público probablemente haya recibido al menos un mal informe de fallo. Informes que no dicen nada ("¡No funciona!"); informes que no tienen sentido; informes que no dan información suficiente; informes que dan información _errónea_. Informes de problemas que acaban siendo un error del usuario; informes de problemas que acaban siendo un fallo del programa de un tercero; informes de problemas que acaban siendo fallos en la red.

Existe una razón por la cual el soporte técnico se ve como un empleo horrible, y esa razón son los malos informes de fallo. Sin embargo, no todos los informes de fallo son molestos: yo mantengo software libre, cuando no me estoy ganando la vida, y a veces recibo informes de fallos increíblemente claros, útiles e _informativos_.

En este ensayo intentaré dejar claro lo que hace bueno a un informe de fallo. Idealmente me gustaría que todo el mundo se leyera este ensayo antes de informar de un fallo a cualquiera. Ciertamente, me gustaría que todos los que vayan a informarme de fallos a _mí_ se lo leyesen.

En pocas palabras, el objetivo de un informe de fallo es permitir al programador ver el programa fallando ante sus ojos. Puedes mostrárselo en persona, o darle instrucciones cuidadas y detalladas de cómo hacer que falle. Si pueden hacer que falle, podrán intentar recolectar información extra hasta que averigüen la causa. Si no pueden hacer que falle, tendrán que pedirte que tú recolectes esa información en su lugar.

En los informes de fallo, intenta dejar muy claro qué son hechos reales ("Estaba con la computadora y ocurrió esto") y qué son especulaciones ("_Creo_ que esto puede ser el problema"). Excluye las especulaciones si quieres, pero no excluyas nunca los hechos.

Cuando informas de un fallo, lo haces porque quieres que el fallo se arregle. No tiene sentido blasfemar al programador o ser deliberadamente inútil: puede que sea culpa suya que tú tengas el problema, y puede que tengas razón al estar enfadado con ellos, pero el fallo se arreglará antes si les ayudas proporcionándoles toda la información que necesitan. Recuerda también que si el programa es gratuito, entonces el autor lo proporciona amablemente, de modo que si mucha gente fuera ruda con ellos quizás deban dejar de sentirse amables.

## "No funciona."

Dale al programador algo de crédito en cuanto a inteligencia básica: si el programa no funcionase en absoluto, se hubieran dado cuenta. Si no se han dado cuenta, es que en su caso funciona. Por tanto, o bien estás haciendo algo diferente de lo que ellos hacen, o tu entorno es diferente del suyo. Necesitan información; proporcionar esa información es el objetivo de un informe de fallo. Más información casi siempre es mejor que menos.

Muchos programas, particularmente programas gratuitos, publican una lista de fallos conocidos. Si puedes encontrar una lista de fallos conocidos, merece la pena leerla para ver si el fallo que acabas de encontrar ya es conocido o no. Si lo es, probablemente no merezca la pena informar de él nuevamente, pero si piensas que tienes más información que la que aparece en el informe de fallo, puede que quieras contactar con el programador de todos modos. Puede que sean capaces de arreglar el fallo más fácilmente si les das información que todavía no tenían.

Este ensayo está lleno de consejos. Ninguno de ellos es una regla absoluta. Programadores concretos tienen formas concretas en las que les gusta que se les informe de fallos. Si el programa viene con su propio conjunto de consejos para informar de fallos, léelos. Si los consejos que vienen con el programa contradicen los consejos presentes en este ensayo, ¡sigue los que vienen con el programa!

Si no estás informando de un fallo sino simplemente pidiendo ayuda para utilizar el programa, deberías indicar en qué otros sitios has buscado ya la respuesta a tu pregunta. ("Miré el capítulo 4 y la sección 5.2 de la ayuda pero no encontré nada que me dijera si esto es posible.") Esto permitirá que el programador sepa dónde espera la gente encontrar la respuesta, de forma que pueden hacer que la documentación sea más fácil de usar.

## "Muéstrame."

Una de las mejores maneras de informar de un fallo es mostrarlo al programador. Sitúalos delante de tu ordenador, lanza su software, y demuestra aquello que funciona mal. Deja que miren cómo arrancas la máquina, que miren cómo ejecutas el software, que miren cómo interactúas con el software y que miren lo que el software realiza como respuesta a tus entradas.

Conocen su software como la palma de su mano. Saben en qué partes confiar, y saben qué partes pueden tener más fallos. Saben intuitivamente lo que tienen que buscar. Cuando el software haya hecho algo obviamente erróneo, puede que hayan reparado en algo anterior _sutilmente_ erróneo que pueda darles una pista. Pueden observar todo lo que el computador hace durante la ejecución de prueba, y pueden decidir lo que es importante por sí mismos.

Quizás esto no sea suficiente. Quizás decidan que necesitan más información, y te pidan que les muestres lo mismo una vez más. Puede que te pidan que les guíes en el proceso, de forma que puedan reproducir el fallo por sí mismos todas las veces que sean necesarias. Puede que intenten variar el proceso algunas veces más, y así conocer si el problema ocurre sólo en un caso o en una familia de casos relacionados. Si no tienes suerte, quizás necesiten sentarse durante un par de horas con un conjunto de herramientas de desarrollo y empezar a investigar _de verdad_. Pero lo más importante es que el programador esté mirando el computador cuando algo falla. Una vez que puedan ver el problema, normalmente podrán seguir solos a partir de ese punto para intentar arreglarlo.

## "Enséñame a mostrar por mí mismo."

Ésta es la era de Internet. Es la era de las comunicaciones globales. Es la era en la que puedo enviar mi software a alguien de Rusia pulsando un botón, y él puede enviarme sus comentarios de forma igualmente sencilla. Pero si tiene un problema con mi programa, _no puede_ hacer que yo esté presente cuando falla. "Muéstrame" es bueno cuando puedes, pero muchas veces no puedes.

Si tienes que informar de un fallo a un programador que no puede estar presente personalmente, el objetivo del ejercicio es hacer que sean capaces de _reproducir_ el problema. Quieres que el programador ejecute su propia copia del programa, haga lo mismo que tú, y haga que falle de la misma manera. Cuando no pueden ver que el problema ocurre delante de sus ojos, no pueden hacer nada con él.

Así que diles exactamente lo que hiciste. Si es un programa gráfico, diles qué botones pulsaste y en qué orden los pulsaste. Si es un programa que se ejecuta escribiendo una orden, múestrales de forma precisa la orden que usaste. Cuando sea posible, debes proporcionar una transcripción de la sesión, mostrando las órdenes que tecleaste y lo que la computadora mostró como respuesta.

Dale al programador toda la información que se te ocurra. Si el programa lee de un fichero, probablemente necesites enviarles una copia del fichero. Si el programa habla con otro computador a través de una red, probablemente no puedas enviarles una copia de ese computador, pero puedes al menos decir qué clase de computador es y, si es posible, qué software ejecuta.

## "A mí me funciona. ¿Qué está mal?"

Si le das a un programador una larga lista de entradas y acciones y ellos lanzan su propia copia del programa y no ocurre nada malo, entonces es que no les has dado información suficiente. Posiblemente el fallo no ocurre en todos los computadores; tu sistema y su sistema puede diferir de algún modo. Quizás hayas malentendido lo que el programa supuestamente hace, y ambos estáis mirando exactamente la misma pantalla y tú piensas que está mal y ellos saben que está bien.

Así que describe también lo que ocurrió. Diles exactamente lo que viste. Diles por qué piensas que lo que viste está mal; aún mejor, diles exactamente lo que tú esperabas ver. Si dices "y entonces falló", estás dejando fuera información muy importante.

Si viste mensajes de error entonces dile al programador, de forma clara y precisa, cuáles eran. ¡_Son_ importantes! En este momento, el programador no está intentando arreglar el problema: sólo están intentando encontrarlo. Necesitan saber qué ha ido mal, y esos mensajes de error son el mayor esfuerzo del computador para decírtelo. Anota los errores si no tienes otra forma más sencilla de recordarlos, pero no merece la pena informar de que el programa generó un error a menos que puedas indicar cuál era el mensaje de error.

En particular, si el mensaje de error contiene números, _asegúrate_ de informar de ellos al programador. Aunque tú no puedas encontrarles sentido no significa que no lo tengan. Los números contienen toda clase de información que puede ser leída por un programador, y probablemente contengan pistas vitales. Los números en los mensajes de error están ahí porque el computador está demasiado confundido como para informar del fallo con palabras, pero está intentando hacerlo lo mejor posible para darte la información importante.

En este punto, el programador está a efectos prácticos realizando el trabajo de un detective. No saben lo que ha ocurrido, y no pueden estar lo bastante cerca como para verlo por ellos mismos, así que están intentando encontrar pistas que les hagan ver el problema. Los mensajes de error, las incomprensibles cadenas de números, e incluso los retardos inesperados son todos tan importantes como las huellas dactilares en la escena de un crimen. ¡Guárdalos!

Si usas Unix, el programa puede producir un volcado de memoria. Los volcados de memoria son una fuente de pistas particularmente buena, así que no los elimines. Por otra parte, a la mayoría de programadores no les gusta recibir ficheros gigantes por correo electrónico sin una advertencia, así que pregunta antes de enviar un volcado a nadie. También, ten en cuenta que los volcados de memoria contienen un registro del estado completo del programa: cualquier "secreto" presente (quizás el programa estuviera manejando un mensaje personal, o trabajando con datos confidenciales) puede aparecer en el fichero del volcado.

## "Y entonces intenté..."

Hay un montón de cosas que puedes hacer cuando aparece un fallo o un error. Muchas de esas cosas empeoran el problema. Una amiga mía en la escuela borró accidentalmente todos sus documentos de Word, y antes de pedir ayuda a un experto intentó reinstalar el Word y luego ejecutar el desfragmentador de disco. Ninguna de esas acciones ayudó a recuperar sus ficheros, y gracias a ambas el disco se dispersó de tal manera que ningún programa de recuperación hubiese podido hacer nada. Si no hubiese tocado nada, puede que hubiera tenido una oportunidad.

Usuarios como éste son como una mangosta atrapada en una esquina: con su espalda contra la pared y viendo la muerte inminente ante sus ojos, ataca salvajemente, porque hacer algo tiene que ser mejor que no hacer nada. Esto no se adapta bien al tipo de problemas que producen los computadores.

En lugar de ser una mangosta, sé un antílope. Cuando un antílope se enfrenta a algo inesperado o terrorífico, se para. Permanece completamente parado e intenta no atraer la atención, mientras se detiene a pensar y calcular qué es lo mejor que puede hacer. (Si los antílopes tuvieran una línea de atención técnica, probablemente llamarían a ella en ese momento.) Entonces, una vez que ha decidido qué es lo más seguro que puede hacer, lo hace.

Cuando algo va mal, inmediatamente deja de hacer _nada_. No toques ningún botón en absoluto. Mira la pantalla e intenta encontrar cosas fuera de lo normal, y recuérdalo o anótalo. Entonces quizás empieza cautelosamente a pulsar "Aceptar" o "Cancelar", lo que te parezca más seguro. Intenta desarrollar un reflejo - si el computador hace algo inesperado, detente.

Si logras salir del problema, bien cerrando el programa afectado o bien reiniciando la computadora, sería bueno intentar hacer que el problema ocurra de nuevo. A los programadores les gustan los problemas que pueden reproducir más de una vez. Los programadores felices arreglan los fallos antes y de forma más eficiente.

## "Creo que el modulador de taquiones tiene la polarización incorrecta."

No sólo son los no-programadores los que producen malos informes de fallos. Algunos de los peores informes de fallos que he visto vienen de programadores, e incluso de buenos programadores.

Una vez trabajé con otro programador que no paraba de encontrar fallos en su código e intentaba arreglarlos. De vez en cuando encontraba un fallo que no era capaz de arreglar, y me llamaba para que le ayudase. "¿Qué ha pasado?", le preguntaba. Él me respondía diciéndome su opinión sobre lo que necesitaba repararse.

Esto funcionaba bien cuando su opinión era correcta. Significaba que ya había hecho la mitad del trabajo y así podíamos terminarlo los dos juntos. Era eficiente y útil.

Sin embargo, muchas veces se equivocaba. Trabajábamos un tiempo intentando averiguar por qué una cierta parte del programa producía datos incorrectos, y eventualmente descubríamos que no los producía, y que habíamos estado media hora investigando un trozo de código que funcionaba perfectamente, y que el problema estaba en otra parte.

Estoy seguro de que tú no harías eso con un doctor. "Doctor, necesito que me prescriba hidroyoyodina." La gente sabe que no debe hacer eso con un doctor: le describes los síntomas, las molestias y achaques y dolores y erupciones y fiebres, y dejas que el doctor haga el diagnóstico del problema y decida qué hacer al respecto. En otro caso el doctor te tomará por hipocondriaco y lunático, y con razón.

Ocurre lo mismo con los programadores. Proporcionar tu propio diagnóstico puede que a veces sea útil, pero siempre establece los síntomas. El diagnóstico es un extra opcional, y no una alternativa a describir los síntomas. Igualmente, enviar modificaciones del código para arreglar el problema es un suplemento útil en un informe de fallo, pero no un sustituto adecuado para el mismo.

Si un programador te pide información extra, ¡no te la inventes! Una vez alguien me informó de un fallo, y le pedí que ejecutara una cierta orden que yo sabía que fallaría. Le pedí que lo probase porque quería saber cuál de dos errores posibles surgiría. Conocer cuál era una pista vital. Pero no lo intentó - sino que me respondió diciendo "No, eso no va a funcionar". Me llevó un tiempo persuadirle de que lo intentara de verdad.

Usar tu inteligencia para ayudar al programador está bien. Incluso si tus deducciones son incorrectas, el programador debería estar agradecido de que al menos hayas _intentado_ hacerle la vida más fácil. Pero informa de los síntomas también, o quizás se la compliques.

## "Vaya, lo hacía hace un momento."

Dile "fallo intermitente" a un programador y fíjate la cara que ponen. Los problemas fáciles son aquellos en los que la realización de una secuencia simple de acciones hacen que surja el problema. El programador puede repetir esa secuencia de acciones en un entorno de pruebas cerrado y observable y ver lo que ocurre con gran detalle. Demasiados problemas no funcionan así: habrá programas que fallarán una vez a la semana, o una vez cada mucho tiempo, o nunca fallarán cuando los pruebes delante del programador pero sí cuando una fecha límite está a la vuelta de la esquina.

La mayoría de los fallos intermitentes no son verdaderamente intermitentes. La mayoría de ellos tienen alguna lógica en alguna parte. Algunos pueden ocurrir cuando la máquina se está quedando sin memoria, otros pueden ocurrir cuando otro programa intenta modificar un fichero crítico en el momento equivocado, y algunos pueden ocurrir ¡sólo en la primera media hora de cada hora! (Una vez vi uno de éstos).

También, si puedes reproducir el fallo pero el programador no puede, podría ser porque tu computador y su computador son diferentes en algo y ese algo es lo que provoca el fallo. Una vez tuve un programa cuya ventana se enrollaba en una pequeña bola en la esquina de la pantalla, se quedaba ahí y _se enfurruñaba_. Pero sólo hacía eso en pantallas de 800x600; en mi pantalla de 1024x768 estaba bien.

El programador querrá saber todo lo que puedas contarle del problema. Pruébalo en otra máquina, quizás. Pruébalo dos o tres veces y mira la frecuencia con la que falla. Si falla cuando estás trabajando en algo serio pero no cuando estás intentando demostrarlo, puede que sean los tiempos grandes de ejecución o ficheros grandes lo que lo hagan fallar. Intenta recordar todos los detalles que puedas acerca de lo que estabas haciendo cuando el programa falló, y si encontraste algún tipo de patrón, menciónalo. Cualquier información que puedas proporcionar será útil. Incluso si es sólo probabilística (como "falla con más frecuencia si estoy ejecutando el Emacs"), puede que no proporcione pistas directas acerca de la causa del problema, pero puede que ayude al programador a la hora de reproducirlo.

Más importante, el programador querrá estar seguro de si es un auténtico fallo intermitente o un fallo específico de esa máquina. Querrán conocer un montón de detalles acerca de tu computador, para intentar saber cómo difiere del suyo. Muchos de esos detalles dependerán del programa en particular, pero algo que deberías estar listo para proporcionar son los números de versión. El número de versión del propio programa, el número de versión del sistema operativo, y probablemente de cualquier otro programa que intervenga en el problema.

## "Entonces cargué el disco en Windows..."

Escribir de forma clara es esencial en un informe de fallo. Si el programador no puede entenderte, quizás sea mejor no decir nada.

Recibo informes de fallos de muchas partes del mundo. Muchos de ellos de personas que no hablan inglés nativamente, y muchos de esos se disculpan por su pobre nivel de inglés. En general, los informes con disculpas por el pobre nivel de inglés son en realidad muy claros y útiles. La mayoría de informes confusos provienen de hablantes nativos de inglés que suponen que les entenderé aunque no hagan ningún esfuerzo por ser claros o precisos.

*   _Sé específico_. Si puedes hacer lo mismo de dos maneras, di cuál usaste. "Seleccioné Cargar" puede significar "Pulsé sobre Cargar" o "Pulsé Alt+L". Di cuál usaste. A veces importa.
*   _Se prolijo_. Da más información en lugar de menos. Si dices muchas cosas, el programador puede ignorar parte de ellas. Si dices pocas, tienen que hacerte más preguntas. Una vez recibí un informe de fallo de una sola frase; cada vez que preguntaba más información, el informador respondía con otra frase suelta. Me llevó varias semanas obtener un volumen de información útil, porque respondía con una frase corta de cada vez.
*   _Ten cuidado con los pronombres y los verbos sin sujeto_. No uses referencias como "la ventana", cuando no está claro lo que significa. Considera el siguiente ejemplo: "Lancé la AplicaciónCualquiera. Apareció una ventana con una advertencia. Intenté cerrarla y cascó." No está claro lo que el usuario intentó cerrar. ¿Intentó cerrar la ventana de advertencia o la ventana de AplicaciónCualquiera? Hay una diferencia. En lugar de eso, podría decir "Lancé la AplicaciónCualquiera, la cual mostró una ventana de advertencia. Intenté cerrar la ventana de advertencia y AplicaciónCualquiera cascó." Esto es más largo y repetitivo, pero es más claro y más difícil de malinterpretar.
*   _Lee lo que has escrito_. Léete el informe a ti mismo e intenta ver si _tú_ crees que es claro. Si listas una secuencia de acciones a realizar para provocar el fallo, intenta seguirlas tú mismo para comprobar si has omitido algún paso.

## Resumen

*   El primer objetivo de un informe de fallo es permitir que el programador vea el fallo por sí mismo. Si no puedes hacer que el programa falle delante de ellos, dale instrucciones detalladas para que ellos mismos puedan hacer que falle.
*   Si esto no surte efecto, y el programador _no puede_ verlo fallar por sí mismo, el segundo objetivo del informe de fallo es describir lo que falló. Describe todo en detalle. Describe lo que viste, y lo que esperabas ver. Toma nota de los mensajes de error, _especialmente_ cuando contengan números.
*   Cuando el computador haga algo inesperado, _detente_. No hagas nada hasta que estés tranquilo, y no hagas nada que creas que es peligroso.
*   Por todos los medios, intenta diagnosticar el problema tú mismo si crees que puedes, pero si lo haces, informa también de los síntomas igualmente.
*   Prepárate para proporcionar información extra si el programador la necesita. Si no la necesitasen no preguntarían por ella. No es que estén siendo retorcidos. Ten los números de versión preparados, porque probablemente harán falta.
*   Escribe de manera clara. Di lo que quieres decir, y asegúrate de que no se puede malinterpretar.
*   Por encima de todo, _sé preciso_. A los programadores les gusta la precisión.

* * *

_Advertencia:_ nunca he visto en realidad una mangosta o un antílope. Mi zoología puede ser inexacta.