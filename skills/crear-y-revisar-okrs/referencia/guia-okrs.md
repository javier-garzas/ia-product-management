<!--
  Base de conocimiento de la skill `crear-y-revisar-okrs`.
  Guía escrita por Javier Garzás · edición 233gradosdeTI · v1.0 (abril 2021).
  LICENCIA PROPIA (distinta a la del repo): esta guía se publicó bajo
  Creative Commons Reconocimiento-NoComercial-SinObraDerivada 4.0 (CC BY-NC-ND).
  Se incluye aquí por su autor como material de referencia.
  © 233gradosdeTI / Javier Garzás. Texto original conservado íntegro
  (solo convertido de EPUB a Markdown; se han omitido las imágenes).
-->

> **📖 Base de conocimiento** de la skill [`crear-y-revisar-okrs`](../SKILL.md).
> Guía de **Javier Garzás** · edición **233gradosdeTI** · v1.0 (abril 2021).
>
> ⚠️ **Licencia propia:** esta guía se publicó bajo **CC BY-NC-ND 4.0** (Reconocimiento-NoComercial-SinObraDerivada), **distinta** de la del resto del repositorio (CC BY-NC-SA). Se incluye aquí **por su autor** como material de referencia. © 233gradosdeTI / Javier Garzás.

---

GUÍA DE OKRs

Esta obra está bajo una licencia de Creative Commons [Reconocimiento-NoComercial-SinObraDerivada 4.0 Internacional](http://creativecommons.org/licenses/by-nc-nd/4.0/)

[Esta no es una licencia de Cultura Libre.](https://creativecommons.org/freeworks)

v 1.0 - abril 2021

De la edición: 233gradosdeTI

MARCAS COMERCIALES: las marcas de los productos citados en el contenido de este libro (sean o no marcas registradas) pertenecen a sus respectivos propietarios.

Se ha puesto el máximo empeño en ofrecer al lector una información completa y precisa. Sin embargo, 233gradosdeTI no asume ninguna responsabilidad derivada de su uso, ni tampoco por cualquier violación de patentes ni otros derechos de terceras partes que pudieran ocurrir. Esta publicación tiene como objeto proporcionar unos conocimientos precisos y acreditados sobre el tema tratado. Su venta no supone para el editor ninguna forma de asistencia legal, administrativa ni de ningún otro tipo. En caso de precisarse asesoría legal u otra forma de ayuda experta, deben buscarse los servicios de un profesional competente.

Reservados todos los derechos de publicación en cualquier idioma. Según lo dispuesto en el Código Penal vigente ninguna parte de este libro puede ser reproducida, grabada en sistema de almacenamiento o transmitida en forma alguna ni por cualquier procedimiento, ya sea electrónico, mecánico, reprográfico, magnético o cualquier otro, sin autorización previa y por escrito de 233gradosdeTI: su contenido está protegido por la Ley vigente que establece penas de prisión y/o multas a quienes intencionadamente reprodujeren o plagiaren, en todo o en parte, una obra literaria, artística o científica.

La infracción de los derechos mencionados puede ser constitutiva de delito contra la propiedad intelectual (art. 270 y siguientes del Código Penal).

Y todos los nombres, tanto de personas como de lugares, de seres y estares\... son pseudónimos, suficientemente ofuscados para guardar la confidencialidad

Versión 1.0

------------------------------------------------------------------------

Sobre el autor, Javier Garzás

Cursé estudios postdoctorales y fui investigador invitado en la Universidad Carnegie Mellon (Pittsburgh, EE. UU), investigando en Agilidad. Soy doctor, Ph.D., en informática, calificado cum laude por unanimidad e Ingeniero en Informática (premio extraordinario).

He sido programador, jefe de proyectos, consultor, director de informática (CIO), diseñador de muchos UMLs, etc., he pasado por casi todas las dedicaciones del desarrollo software.

Pionero en España en agilidad, mi primer proyecto ágil en empresa fue en 2001 (con eXtreme Programming).

Desde hace años, me dedico a ayudar a organizaciones, a que trabajen mejor (en tiempo, con productividad, agilidad, calidad y felicidad).

Hasta la fecha, a lo largo de mi carrera profesional he trabajado para, o en, más de 100 empresas (en España, Colombia, Chile, Venezuela y EEUU) entre las que están algunas como:

- Ingeniería -- Aeronáutica -- Automoción -- Software Crítico: GMV -- División de Control de Satélites, FICOSA, CESA (Sistemas Aeronáuticos).
- Retail: Inditex, Pull and Bear, Leroy Merlin
- Constructoras: Ferrovial.
- Aseguradoras y Sector Financiero: Ocaso, Banco Santander, BBVA, Aegon, Produban, Cajasur, Mapfre, ING.
- Operadoras: Telefónica, Vodafone
- Información y Comunicaciones: El Mundo, Wolters Kluwer.
- Tecnologías de la Información: Velneo, Vintegris, Indra, Freepik.

- ERPs: DANTIA, VisualTrans
- Consultoras: Accenture, Altran Innovación S.L, Viewnext, Ibermática, Bilbomática, Dantia.
- Sector Energético: PVH Storage.
- Administración Pública: Dirección General de Tráfico, Ministerio de Administraciones Públicas (MAP), Informática de la Comunidad de Madrid (ICM), Sistemas Técnicos de Loterías (STL), Agencia Tributaria (AEAT), LANTIK, Informática de la Seguridad Social, Catastro, Informática del Gobierno Vasco (EJIE).
- Otros Organismos Públicos: ONCE
- Alimentación: DIA, S.A.
- Deporte: F. C. Barcelona, Federación Española de Fútbol.
- Transporte: Pullmantur.
- Certificadoras: AENOR, EQA.

Además, soy profesor de la Universidad Rey Juan Carlos.

En lo que refiere a certificaciones, muchas, algunas de ellas: Certified Management 3.0 Practitioner (y co-owner de la propia Management 3.0), Scrum Master certificado por Jeff Sutherland (co-creador de Scrum), Advanced Agile certificado por Alistair Cockburn (uno de los padres de la agilidad), Certificado DAD (Disciplined Agile delivery) por Scott Ambler (creador del modelo), etc.

Te dejo mis redes para estar en contacto:

- twitter:   [\@jgarzas](https://twitter.com/jgarzas?lang=en)
- web:   [www.javiergarzas.com](http://www.javiergarzas.com) , blog en el que escribo desde hace más de 10 años
- Instagram: [https://www.instagram.com/javiergarzas/](https://www.instagram.com/javiergarzas/)
- YouTube: [http://youtube.com/c/JavierGarzas](http://youtube.com/c/JavierGarzas)
- LinkedIn: [es.linkedin.com/in/jgarzas](https://es.linkedin.com/in/jgarzas)

Libros relacionados

Si no estás familiarizado con Scrum, o con la Agilidad en general, te recomiendo leer antes estos libros, podrás encontrarlos en: [233gradosdeti.com/publicaciones-233/](http://233gradosdeti.com/publicaciones-233/)

[23 Historias de Equipos Ágiles.](http://233gradosdeti.com/publicaciones-233/23-historias-equipos-agiles/)

[Peopleware y Equipos Ágiles.](http://233gradosdeti.com/publicaciones-233/peopleware-equipos-agiles-y-management-3-0/)

[Gestión de](http://233gradosdeti.com/publicaciones-233/libro-gestion-de-proyectos-agil/) [proyectos](http://233gradosdeti.com/publicaciones-233/libro-gestion-de-proyectos-agil/) [ Ágil.... y las experiencias de más de 12 años de proyectos ágiles.](http://233gradosdeti.com/publicaciones-233/libro-gestion-de-proyectos-agil/)

------------------------------------------------------------------------

Índice

------------------------------------------------------------------------

# 1. ¿Qué son los OKR?

Los OKR (Objectives and key results) nos hablan de establecer un objetivo, «lo que queremos lograr» y los «resultados clave», que son «cómo pretendemos lograrlo».

Los OKR no son sólo un objetivo, también deben incluir una forma de medir ese logro.

Su beneficio es que los OKR ayudan a las organizaciones a establecer objetivos, más o menos ambiciosos y luego centrarse en cómo lograr los resultados.

Aunque pueda parecer obvio, conviene dejar claro las dos grandes partes de un OKR:

- El objetivo, lo que se pretende obtener, normalmente es cualitativo.
- El resultado clave, cómo sabemos si lo hemos logrado, y, normalmente, es cuantitativo.

Va un ejemplo...

Objetivo:

- Vamos a liberar una versión, un producto mínimo viable, del producto que sea impresionante.

Resultados clave:

- 70% de los actuales usuarios descargan la nueva versión
- Obtenemos 800 «me gusta»

## 1.1 De dónde vienen

Como siempre, los OKR son algo bastante viejuno, se habla de que vienen ya de los 70.

El concepto fue creado por Andy Grove. De hecho, el tema es tan antiguo que hay un   [«supuesto» vídeo](https://www.youtube.com/watch?v=1ht_1VAF6ik&t=1s)   de Andy Grove dando una clase de OKRs en los años 70 (digo lo de «supuestamente» por que no tengo total confirmación de la fecha del vídeo).

Y quien los hizo populares fue John Doerr, uno de los primeros inversores en Google.

Y luego, cuenta la leyenda, que los OKR se convirtieron en un framework importante para Google, LinkedIn, Twitter, Dropbox, Spotify, AirBnB, Uber (como no hemos trabajado en ninguna de las anteriores, esto lo dejo en un «cuenta la leyenda»).

## 1.2 OKR vs KPIs

Hay por ahí un montón de ideas que son parecidas, aunque no iguales a los OKR, como los KPI, GQM, etc.

Vamos con un clásico: OKR vs KPIs

Los KPIs (Key Performance Indicator) refieren, como indica su nombre, a resultados del proceso. Ejemplos:

- Número de Historias completadas en el Sprint
- Número de correctivos por mes
- etc.

Los OKR miden... el resultado. Y el resultado está relacionado con lo que en el mundo Ágil llamamos valor, con los usuarios, negocio, etc.

El KPI suele estar más relacionado con el equipo, mientras que el OKR es más de la empresa, de la organización, del departamento.

Más adelante entraremos en más detalle sobre este tema.

## 1.3 Los OKR materializan mejor la idea de entrega de valor

En Agilidad siempre hemos hablado del valor. Que todo debe aportar valor, que el valor es lo importante, etc. Si bien es cierto que se ha trabajado menos que la eficiencia, la mejora del proceso, la velocidad, eliminación de desperdicio, etc.

Ambas cosas son esenciales, el valor (la eficiencia) y la eficacia.

Y aquí es donde los OKR ocupan un papel importante en el mundo Ágil, dan un mayor soporte a la mejora de la eficacia, potenciar el valor.

También es interesante recordar que, aparte de los OKR, y con menos fama, hay más «paradigmas» trabajando en este punto del valor, como «Build the Trap», el HDD, etc.

## 1.4 Que los Objetivos sean ambiciosos: OKRs que buscan llegar al techo y ORKs que buscan llegar a la Luna

La idea es que los KR, los resultados clave, sean difíciles, ambiciosos, aunque no imposibles. Una manera de trabajar esto es con los llamados objetivos «Moonshot» y «Roofshot».

Se les suele llamar Moonshot o «lanzamiento a la Luna» a aquellos Objetivos de un OKR que son casi imposibles, pero que buscan motivación, sacarnos de nuestra zona de confort.

Los Roofshot (lanzamiento al techo) son de objetivos alcanzables, más llevaderos.

También puedes poner el mismo objetivo pero cambiar la ambición del «resultado clave», poniendo resultados Moonshot o Roofshot.

Intenta moverte entre objetivos Moonshot y Roofshot, que tengas de ambos, cosas ambiciosas y objetivos más modestos.

------------------------------------------------------------------------

# 2. Creando buenos «resultados clave»

## 2.1 Los «resultados clave» no son... tareas

El resultado clave debe ser eso... un resultado (y no una tarea a completar) y, además, el consejo generalizado, lo que mejor nos funciona, es que esté más cercano a un «qué» que a un «cómo».

Vamos a poner un ejemplo facilote que todo el mundo entienda. Imagina que ponemos un OKR para un blog X y que el objetivo del OKR es «que este blog sea muy útil para sus lectores» (es cualitativo, subjetivo y de cara a aportar valor a los usuarios).

Podríamos pensar que un «resultado clave» es... «publicar 5 posts a la semana», pero eso realmente es una tarea (más que un resultado), no tengo claro que «publicar 5 posts a la semana» me acerque al objetivo de que «que este blog sea muy útil para sus lectores»

¿No sería mejor que pongamos un «resultado clave» del tipo a «aumentar el tráfico por semana en un 5%»?

Publicar 5 posts a la semana está muy lejos del objetivo. Además, «aumentar el tráfico por semana en un 5%» nos deja la puerta abierta a muchas opciones, entre ellas, tanto puede ser publicar 5 posts a la semana como optimizar posts antiguos para que posicionen mejor en Google.

Así que recuerda: el KR (del OKR), habla de «resultados».

Así que... evita hacer KRs Tipo «check list» de tareas. Piensa en resultados.

## 2.2 Lo ideal es que los resultados clave los pongan los equipos

Por otro lado, deberíamos, como no, volver aquí también a fomentar la [auto-organización](https://www.javiergarzas.com/2015/07/equipos-auto-organizados-iii-arma-poderosa-pero-tambien-peligrosa-si-no-se-usa-bien.html) .

Ya sabes, eso que es tan de equipo Ágil de que se determine el «qué» y los que saben pongan el «cómo».

La opción más auto-organizada es que alguien de negocio, los managers de la empresa, los Stakeholders, etc., fijen los «objetivos» del OKR y los equipos los «resultados clave».

## 2.3 Una opción menos auto-organizada

Pero, también es cierto, que hay equipos menos maduros. O equipos que, simplemente, no quieren entrar en los «resultados clave».

Hay equipos menos creativos, o que quizá han pasado demasiado tiempo bajo estructuras clásicas de gestión y recibiendo órdenes de «jefes de proyecto».

Equipos que, simplemente, [no quieren ser equipos auto-organizados](https://www.javiergarzas.com/2020/06/no-queremos-ser-equipos-auto-organizados.html) .

Si este es el caso, opción menos auto-organizada (que debería ser temporal), es que si alguien externo al equipo va a fijar los resultados clave debería mantenerlos los más cerca del «qué» que del «cómo», evitando listas de tareas y, aunque en menor medida, potenciando la auto-organización de los equipos.

# 3. Puntuando los «resultados clave»

## 3.1 ¿Cómo vas a medir ese resultado clave? Busca la objetividad

Continuando con el ejemplo facilote del blog X, imagina que ponemos un OKR para el blog  y que el objetivo del OKR es «que este blog sea muy útil para sus lectores» (que, como ya mencionamos, tiene buena pinta porque es cualitativo, subjetivo y de cara a aportar valor a los usuarios).

Y ahora decidimos que un resultado clave es «mayor número de usuarios recurrentes», vale, OK, pero... ¿cómo vamos a medir eso luego? ¡Es súper subjetivo ese resultado clave!

Como ya he mencionado antes, evita fijar resultados clave tan subjetivos, así que en vez de «mayor número de usuarios recurrentes» usa, por ejemplo, resultados clave del tipo a «un 5% más de usuarios recurrentes durante el trimestre».

Los objetivos suelen ser más subjetivos, pero los resultados clave deberían ser mucho más objetivos.

De nuevo, esto refuerza el uso de resultados clave del tipo a «aumentar el tráfico por semana en un 5%». Si en vez del anterior pongo «que los visitantes al blog se lleven una buena experiencia», pues va a ser difícil de puntuar.

## 3.2 Dejar claro cómo vais a puntuar los OKR

Una manera típica de hacerlo es puntuar cada KR, cada resultado clave, entre 0 y 1 (también hay quien lo hace entre 0 y 10). Si usas ese sistema de puntuación, cero sería fracaso máximo y 1 éxito total.

Como casi todo el mundo se ha basado en cómo hace uso Google de los OKR (de dejo [un vídeo que es un clásico](https://www.youtube.com/watch?v=mJB83EZtAjc)  en lo que refiere a referencias sobre OKRs), casi todo el mundo ha tomado su (supuesta) manera de medirlos, que es esa de entre 0 y 1, entendiendo que obtener un 0,7 es una buena puntuación (lo de 0,7 también viene de Google).

Dejar un margen entre 0,7 y 1 deja un lugar para los resultados excelentes, más allá de obtener buenas puntuaciones.

## 3.3 La puntuación del «resultado clave» es gradual... no binaria

Si usas una escala de puntuación entre 0 y 1, usando decimales por medio, y siempre puntúas con ceros o unos... algo raro está pasando.

Si salen muchos 1, una razón es que tus resultados clave son tareas, tipo check list, del tipo a se hacen o no se hacen.

Si salen muchos 0... deberíais plantearos qué está pasando, qué sentido tiene estar poniendo resultados clave que o son imposibles o no nos interesa trabajarlos.

## 3.3 Algunos consejos más: temporalidad, número y no los hagas a nivel de persona

Unos cuantos consejos más.

En lo que refiere a la temporalidad, típicamente, una temporalidad razonable para revisar los OKR es de manera trimestral, después de ese periodo se puntúan.

Otra cosa es el número de resultados clave por objetivo, que, aunque esto es opinable, por defecto, lo típico es que debe rondar entre 3 y 7.

Y, por último, por favor... no creéis OKR a nivel de persona, siempre a nivel de equipos.

# 4. Los buenos objetivos

## 4.1 Los mejores objetivos son inspiradores y cualitativos

Intenta que los objetivos del OKR sean retadores y lo más motivadores posible.

Los objetivos ojalá os salgan inspiradores y, además, cualitativos (que no con números o medibles directamente). Que los cualitativos funcionan mejor en esto de ser motivadores.

Por ejemplo, compara el objetivo de «comprender las necesidades del cliente» vs «detectar un 30% más de necesidades del cliente». El primero no lleva acompañado un número, no es necesario tener métricas numéricas para los objetivos, déjalas para los resultados clave.

## 4.2 El objetivo describe el resultado deseado

Pues eso, que cuando describas el objetivo este debe estar describiendo, cualitativamente, el resultado deseado.

En inglés hay dos palabras que explican esto muy bien pero que son difíciles de traducir: Outcome y Output.

El objetivo del OKR debiera ser más un Outcome, que vendría a ser algo que queremos cambiar en el mundo, un problema que tienen los usuarios y que queremos resolver.

Mientras que «resultado clave» es más un Output, que viene a ser lo que producimos, la salida, una de las muchas maneras de afrontar la resolución de los problemas que cuentan los objetivos.

------------------------------------------------------------------------

## 4.3 Los objetivos se piensan para un tiempo limitado

Y que ese tiempo no sea muy largo. Y que sea conocido.

La idea de Time-Box, de toda la vida, la que tantas veces usamos en modelos Ágiles, pero ahora... con el OKR.

Siempre hay que poner una temporalidad.

Y entre las temporalidades que por ahí usa el mundo, la más usada, si te vale de referencia, es el trimestre (los «quarter» que se dice in english).

# 5. Ampliando los OKR con MOKRs y CFRs

## 5.1 MOKRs... Misión + OKR

Los MOKR son una ampliación, concreción, orientación, añadida al tradicional concepto de OKR, donde la «M» viene de «Misión» y se pone antes de la O, de «Objetivo», para responder a la fundamental pregunta de... «cuál es el propósito de nuestra organización».

La idea es tener clara la Misión y alinear los OKR en función de esta.

Los OKR pueden variar mucho más en el tiempo, mientras que la Misión es más perdurable.

Si los OKR suelen revisarse de manera trimestral, la Misión va mucho más allá y, en nuestro caso, nos ayuda a garantizar que los OKR están alineados a la misión estratégica a largo plazo de la organización.

## 5.2 OKRs más CFRs

CFR es el acrónimo de «Conversations, Feedback, and Recognition».

En el que probablemente sea el libro más famoso sobre OKRs, el de John Doerr, « [Measure What Matters](https://amzn.to/3wgwgFn) », sugiere que los OKR deberían combinarse con CFRs.

Los CFRs son un «sistema de creación» de OKRs, buscan el qué motiva tener esos OKR, conversar para crearlos, ajustarlos y sobre cómo se han desarrollado y proponen hacerlo mediante...

- Conversaciones, intercambios de información.
- Retroalimentación, comunicación bidireccional, comunicación entre partes para evaluar el progreso.
- Reconocimiento.

Los CFR evitan caer en que la respuesta a si se ha logrado un OKR sea del tipo a «si o no».

# 6. El ritmo Spotify (Spotify Rhythm) como alternativa a los OKR

Puede sonar un poco forzado, en lo que refiere a meterlo en esta guía (ya que el Spotify Rhythm es un modelo aparte, aunque relacionado), pero me ha parecido meterlo por darle una continuidad al tema.

Antes de empezar, voy con unos «disclaimers»...

- El primero, hay muy poca información sobre este modelo, así que he tenido que «rascar» mucho, ver varias veces lo poco que hay, así probablemente meta alguna interpretación mía, etc.
- Segundo, tómalo como ideas, muy probablemente este modelo haya ya evolucionado y, sobre todo, recuerda, [no caigas en el error de copiar el modelo ágil de Spotify](https://www.javiergarzas.com/2018/06/no-caigas-error-copiar-modelo-agil-spotify.html) .

## 6.1 El ritmo Spotify (Spotify Rhythm)

El ritmo Spotify (Spotify Rhythm) viene a ser la estrategia de Spotify para mantener «alineada a la compañía» para crear su «planificación estratégica».

Quien más popularizó esta estrategia ha sido Henrik Kniberg (al que [entrevisté en mi blog hace años](https://www.javiergarzas.com/2013/11/entrevista-henrik-kniberg.html) ).

La «publicidad» del modelo y la mayoría de información disponible vienen de él y de algún post en el blog de Spotify.

## 6.2 Dejando de usar los OKR

En 2014 Spotify dejó de usar los OKR. Según se cuenta en la información que hay disponible, los usaron un tiempo y vieron que no les encajaban del todo (la de abajo es una diapositiva de Kniberg).

Te dejo alguna referencia sobre las críticas a los OKR por parte de Spotify, [como esta](https://hrblog.spotify.com/2016/08/15/our-beliefs/)  o [esta otra](https://www.slideshare.net/peterantman/growing-up-with-agile-how-the-spotify-model-has-evolved) . Y, así, sintetizando, estas son algunas de las razones por las que decidieron dejar de usarlos:

- Eran demasiado pesados
- Estresantes
- Lentos
- Están muy centrados en el cómo y no en el «por qué»

Así que, desde modelos como OKRs, derivaron a su propio modelo, el que llaman Spotify Rhythm.

## 6.3 La taxonomía utilizada para la «planificación estratégica»

Como puedes ver en la captura de abajo, el modelo trata diferentes niveles de abstracción a la hora de estructurar el alineamiento y la estrategia.

Fuente: [https://www.slideshare.net/peterantman/growing-up-with-agile-how-the-spotify-model-has-evolved](https://www.slideshare.net/peterantman/growing-up-with-agile-how-the-spotify-model-has-evolved)

Vamos a darle un pequeño repaso a los niveles:

- Creencias de la compañía, el concepto de creencias (que es diferente al de valores) podría considerarse el nivel más alto y, por lo tanto, las hipótesis más fuertes.
- Estrella del Norte («North Star»). Una North Star (o True North) marca una visión del futuro (una métrica, cercana al por qué), y es utilizada para establecer la dirección. Se pueden tomar decisiones en función de si moverán a la organización hacia (o lejos) la Estrella del Norte.
- Los objetivos de 2 años se pueden considerar como los resultados que nos deben llevar hacia la Estrella del Norte.
- Apuestas de la empresa, son las «grandes apuestas», «grandes proyectos» e «iniciativas entre organizaciones».

Para definir esas apuestas Spotify se inventó un modelo llamado DIBB, que muestra las relaciones entre Datos (Data), Intuiciones (Insight), Creencias (Beliefs) y Apuestas (Bets). Que se complementa con algo está implícito en el propio nombre de «Spotify Rhythm»: la cadencia con la que se ejecuta el proceso.

Como resumen, y como se comenta en [alguna referencia](https://availagility.co.uk/2016/07/11/strategy-deployment-and-spotify-rhythm/) , el Spotify Rhythm proporciona claridad sobre cómo responder estas preguntas:

- ¿A dónde te diriges? estrella del Norte
- ¿Cómo imaginas el camino? Objetivos a 2 años (resultados)
- ¿Sabes cómo llegarás allí? Apuestas de empresa (estrategias)
- ¿Sabes cómo vas a hacer un seguimiento del progreso? DIBB (resultados)

## 6.4 Cómo definir las «apuestas» usando el marco DIBB

DIBB viene de «Data Insight Belief Bet». Y, básicamente, es una plantilla que contiene cuatro columnas:

- Data, es con qué datos contamos, qué datos tenemos. Ejemplo (que copio directamente de los datos que hay sobre todo esto de Spotify), «la gente usa más el móvil que el PC para acceder a nuestra aplicación» o «tenemos 20 bugs de media cada mes».
- Intuiciones (Insight), que son las sensaciones que nos dan los datos. Ejemplo, «los móviles están desplazando a los PC como principal medio para escuchar música en la web» o «no estamos probando demasiado bien nuestros desarrollos».
- Creencias (Belief), la creencia es, respecto a los anteriores, «el lugar que nosotros queremos ocupar en el mundo». Ejemplo, «necesitamos estar preparados y ser los primeros en aplicaciones móviles para escuchar música» o «necesitamos que nos conozcan por lo fiables que son nuestras aplicaciones, no por lo contrario».
- Apuestas (Bet). Sabiendo dónde queremos estar... qué vamos a hacer al respecto. Ejemplo, «vamos a formar a un equipo de desarrolladores en aplicaciones móviles», «vamos a crear una infraestructura para el desarrollo móvil» o «vamos a incrementar el número de pruebas de integración».

## 6.5 Visualizando las apuestas en un tablero Kanban

Dicho lo anterior, según la información que he podido recopilar, las apuestas se visualizan en un tablero «Kanban» a nivel de empresa, con 3 columnas «Ahora -- Siguiente -- Más adelante» (Now, Next, Later).

Ahora «el truco» es que las diferentes partes, divisiones, equipos, etc., de la empresa visualizan el tablero de «apuestas» y crean las suyas propias que se alinean con las apuestas de mayor nivel.

Y esos equipos, partes, divisiones, etc., son responsables ellos mismos de decidir la mejor manera de contribuir a resolver las apuestas. Auto-organización.

## 6.6 Los tableros de apuestas y los DIBB son el contexto... y son los equipos auto-organizados los que ponen el cómo resolverlos

La idea es que los equipos puedan colaborar de manera efectiva y seguir siendo autónomos para minimizar decirles qué hacer, que vean el contexto y profundicen en cómo contribuir a resolver las apuestas.

Sin contexto, la autonomía y la auto-organización no funciona bien, y sin contexto los equipos pueden ir en diferentes direcciones y chocar entre ellos.

## 6.7 El ritmo en tres niveles, diferentes escalas de tiempo

En este modelo hay diferentes cadencias a diferentes niveles de la empresa.

Primero, el tablero de apuestas se puede cambiar en cualquier momento, si bien, al menos, hay una revisión cada trimestre.

Luego, por divisiones, hay revisiones cada 6 semanas.

Y, finalmente, los equipos hacen sus sprints, que contemplan las apuestas, y que son de entre 1 y 2 semanas.

# 7. Cinco problemas típicos usando OKRs

## 7.1 Los errores más comunes al usar OKRs

He hecho una recopilación de los errores más típicos a la hora de usar OKRs y que, en mi experiencia, son:

1. Empezar con fuerza y... olvidarse de ellos: Desperdicio en vena , el típico de [empezar algo y no terminarlo](https://www.javiergarzas.com/2019/03/el-desperdicio-de-los-tiempos-de-espera-en-video.html) , o terminarlo mucho después. [El "efecto novedad" es poderoso para hacernos arrancar](https://www.javiergarzas.com/2017/02/peligro-del-efecto-novedad-cuando-se-quiere-cambio.html) , pero la constancia es la clave del éxito.
2. Objetivos imposibles: Esto es cuando alguien, que generalmente no es quien tiene que lograr el objetivo, se viene arriba y pone un objetivo que roza lo imposible de manera obvia. Esto conlleva mucha desmotivación para aquellos que deben luchar por lograrlo, ya que desde el principio saben que no lo van a poder conseguir.
3. Objetivos demasiado fáciles: Contrario al anterior, en ocasiones me encuentro objetivos que son obvios, facilones , tan fáciles que tampoco motiva luchas por ellos. Este caso suele darse cuando «los jefes» no se han involucrado mucho en la creación del objetivo ni en los OKR.
4. Resultados clave que nadie sabe cómo medir: Este es un tema del que hablamos en el capítulo 3 de esta guía , pero que aún así quería que no faltara en esta lista de 5 errores frecuentes, porque no podía faltar.
5. Copiar a otros: Al igual que nos pasaba con aquello de copiar el modelo ágil de Spotify , pues lo mismo aquí, copiando lo que dice Google y otros tantos. Tienes que empezar basándote en otros, pero buscando tu propia adaptación, si te quedas solo en copiar a otros perderás todo lo especial que tiene tu caso concreto y que, seguramente, es único.

------------------------------------------------------------------------

# 8. La matriz TASTE

La matriz X, o matriz TASTE, o matriz Hoshin Kanri, es una plantilla (aunque hay varias versiones) para visualizar la alineación de una organización.

Lo de TASTE, aunque en inglés viene a se algo así como «sabor», es un acrónimo, que viene de los siguientes:

- T, que viene de «True North» ( estrella del norte), la orientación, la visión, el destino, el impacto.
- A, que viene de «Aspirations», aspiraciones, los resultados que esperamos lograr, en línea con la «True North». Hablamos aquí de aspiraciones a largo plazo.
- S, que viene de «Strategy», la estrategia. En este caso, frente al anterior, hablamos de medio plazo.
- T, que viene de, «Tactics», las acciones coherentes que tomamos. Estos son los experimentos que realizaremos para probar nuestra hipótesis.
- E, que viene de «Evidence», las evidencias, los resultados que indican progreso. Datos para saber que va por buen camino.

Con los anteriores se forma una matriz, como la que que te dejo más abajo (la imagen es de availagility.co.uk)

# 9. Los OKR no son suficientes para guiar la estrategia de una organización

He escuchado mucho que los OKR son una herramienta para guiar la estrategia de una organización, si bien los OKR, por sí solos son... una herramienta para fijar objetivos.  

Veamos entonces cosas, obvias (o, quizá, no parece que tan obvias), que no tiene los OKRs, que necesitamos para guiar la estrategia:

- Por sí solos, los OKR no son una herramienta altamente sólida para fijar cosas como la misión, la visión, etc. Sí, ya sabes, esas «cosas» tan necesarias en la definición y ejecución de una estrategia.
- Por sí solos, los OKR no tratan el proceso para la definición de los objetivos y los resultados clave.
- Normalmente, aunque no necesariamente, los OKRs tienen un alcance trimestral, y en la definición y ejecución de una estrategia es también necesario tener una visión a más largo plazo.
- Por sí solos, los OKR, tampoco hablan de algún mecanismo para ajustar los Objetivos, e, incluso, el detectar si es necesario ajustarlos.

- Por sí solos, los OKR, tampoco contemplan cualquier tipo de planificación por escenarios.

Por todo lo anterior, sin querer perdernos en terminología, hay que tener cuidado con llamar «framework» a los OKR, más que nada porque se pudiera obviar que nos hacen falta muchas más cosas para llevar una estrategia.

Los OKR son una herramienta (entre otras) para fijar una estrategia... sí. Pero por sí solos no son suficientes.

# 10. No confundas los OKR con los KPI (y tampoco elimines los KPI)

## 10.1 Un OKR no es KPI

En mi opinión es quizá uno de los errores más frecuentes, en vez de crear OKRs tener métricas o, una versión específica de ellas, que son los conocidos como KPIs (Key Performance Indicators).

Los KPIs son el rendimiento de algo que ya existe, pero no ayudan a avanzar para lograr un objetivo. Los KPIs nos dicen cómo está la situación ahora. Los OKRs marcan el camino de futuro.

Si trabajas en un modelo ágil, puede que además uses Scrum, incluso complementándolo con Kanban, hay muchos KPIs típicos:

- Velocidad (por favor, medida en Historias de Usuario, no en Puntos Historia)
- Número de defectos
- Errores en la estimación
- Cycle Time
- Lead Time
- etc.

No me quiero ir del tema, pero recuerda que los anteriores pueden ser sólo PI (Performance Indicators, indicadores de rendimiento) o ser KPI (Key Performance Indicators, indicadores de rendimiento CLAVE). Que no todo PI es KPI y eso tenéis que decidirlo vosotros.

[Haciendo una analogía](https://www.perdoo.com/resources/when-implementing-okr-get-your-kpis-in-place-first/) , si organización es un coche, el destino hacia donde vas es el objetivo final de su organización (la misión y la visión) y sus OKRs construyen su hoja de ruta hacia ese objetivo. Pero, mientras conduces tienes que mirar el cuadro de mandos del coche,  para asegurarse de que llevas gasolina, la velocidad a la que vas, etc.

Así que los  OKR  buscan cambiar algo, guiar, los KPI medir lo que ya existe.

## 10.2 Necesitamos KPIs y necesitamos OKRs

Uno no sustituye al otro y ambos son necesarios. Sin OKRs no tenemos claro a dónde ir ni cuánto queda, sin KPIs no tenemos datos para «conducir».

Al igual que no tiene sentido conducir un coche sin un cuadro de indicadores que nos digan la velocidad, la gasolina que queda, etc., no tiene sentido tener OKRs sin KPIs. Y los KPIs son un profundo «input» para los OKR.

Así que es muy probable que algunos OKR, concretamente el KR, tomen como entrada algunos KPI. E, igualmente, también puede pasar que tengas KRs sin KPI.

# 11. Cuidado con las jerarquías de OKRs (que pueden ser Lado Oscuro)

Por ponerte en situación, es muy típico, en sitios medianos, y en grandes aún más, que tengamos OKRs a diferentes niveles: nivel de la organización, nivel de departamento (área o divisiones), nivel de equipo, etc. Esto es muy típico.

Y en principio está bien salvo que, cómo no, lo llevemos al Lado Oscuro, lo típico.

## 11.1 ¿Dónde están los riesgos y dónde la podéis liar con las jerarquías de OKRs?

El principal problema está cuando creas un árbol de OKRs, en el que los KR de los OKR de nivel superior se convierten en las O (los Objetivos) del siguiente nivel.

Si hacéis lo anterior, probablemente, pase...

1. Que las jerarquías te lleven a tener decenas de OKRs y KRs: Lo de tener muchos OKR es un PROBLEMA, hay que tener pocos OKR y, a su vez, pocos KR.   Otro problema derivado de convertir KRs de nivel superior en Os (Objetivos) de OKRs de nivel inferior es que acabas de crear malos Objetivos.
2. No crees Objetivos cuantitativos por herencia de un KR superior:   Sí, porque, los Objetivos son cualitativos e inspiradores y los KR son cuantitativos y medibles, entonces, obviamente, un Objetivo no puede convertirse en un KR, sino tendríamos Objetivos cuantitativos, en vez de cualitativos.
3. Te estás cargando la auto-organización
4. Y por último, por si era poco, si en vez de inspirar a un equipo a crear sus propios OKRs, e INSPIRARLOS dándoles un OKR de nivel superior, si en vez de eso les dejamos cerrado el Objetivo de su OKR, para que solo creen los KR... nos hemos cargado todo grado de auto-organización.

# 12. La Métrica de la Estrella del Norte y los OKR

A la hora de crear OKRs siempre hablamos de que deben venir inspirados por la visión, la misión, el para qué, etc. Cierto.

Pero dado que los anteriores muchas veces suelen ser algo etéreos (en algunos sitios me cuesta mucho partir de la misión visión para crear OKR, porque ya había en «la web» de la empresa una misión - visión etérea, abstracta, y muchas veces abandonada, hasta el punto de que genera mucha confusión a la hora de ser la entrada a la creación de OKRs), hay algo que ayuda a complementar esas «inspiraciones» a la hora de crear OKRS... la métrica de la Estrella del Norte.

La métrica de la Estrella del Norte, sin soltarte mucho el rollo, es la métrica que guía toda la energía de una organización. Y, típicamente, suele haber una métrica, máximo dos métricas, de la Estrella del Norte, precisamente para focalizar a todo el grupo en una única dirección.

La métrica de la Estrella del Norte es algo muy de estrategia (no algo operativo, no del día a día, no tareas, no KPIs). Vamos con algunos ejemplos populares y de países lejanos, pero que se entienden bien (y, además, no son confidenciales y no nos metemos en problemas):

- La métrica de la Estrella del Norte de Spotify cuentan que es «Tiempo que dedican los usuarios a escuchar»
- La métrica de la Estrella del Norte de Airbnb cuentan que es el «Número de noches reservadas»
- La métrica de la Estrella del Norte de Facebook cuentan que son los «Usuarios activos mensuales»

Podríamos pensar, y es sensato, que la métrica de la Estrella del Norte es un OKR de alto nivel, quizá el OKR de mayor nivel de abstracción, el de Organización, aquel OKR que inspira a OKRS de menor nivel. Podría tener sentido.

Pero dado que la métrica de la Estrella del Norte es de carácter más estratégico, hay algo que la diferencia de los OKRS: que suele tener un alcance temporal mayor, de incluso años.

La métrica de la Estrella del Norte varía menos en el tiempo, a diferencia del típico alcance trimestral de los OKRs.

## 12.1 Eligiendo la Estrella del Norte

En términos generales, hay [seis categorías de métricas de North Star](https://future.a16z.com/north-star-metrics/) :

1. Ingresos
2. Crecimiento de clientes
3. Crecimiento del consumo (por ejemplo, más música escuchada, más habitaciones reservadas, más mensajes enviados)
4. Crecimiento de la participación (por ejemplo, usuarios activos)
5. Eficiencia de crecimiento (por ejemplo, gastos frente a ingresos)
6. Experiencia de usuario (por ejemplo, cómo de satisfechos están los usuario)

Y hay, de manera general, dos preguntas clave para sacar nuestra Estrella del Norte:

- ¿Qué métrica sería la que, de crecer, más aceleraría hoy el crecimiento de nuestro negocio? Esto, obviamente, depende mucho del modelo de negocio.
- ¿Para qué usan/compran los clientes nuestro producto/servicio? Aquí buscamos analizar qué lleva a una compra y potenciarlo.

Y por terminar esta parte, una buena métrica de la Estrella del Norte, debería...

- Impulsar el crecimiento de la organización

- Aportando valor al cliente
- Siendo medible y fácil de medir.
- Y siendo una métrica que produce un efecto, un resultado, en los usuario, a través de nuestro producto/servicio, crea un efecto fuera de las fronteras de nuestra empresa

Así que ojito con...

## 12.2 La Estrella del Norte... ¿Es siempre beneficio económico?

Muchas veces... sí. Pero no siempre es la mejor idea, razones:

- Nos aleja de pensar a medio largo plazo.
- Es poco inspirador para los equipos y para la gente que está más apasionada por el producto/servicio que hacemos que por los ingresos.
- Puede ser una Estrella del Norte demasiado simplista y que marque poco la estrategia.

Estratégicamente tener una métrica de la Estrella del Norte basada en dinero no es la mejor opción, ya que nos enfoca en obtener dinero del cliente más que en crear algo que aporte valor, que no siempre es lo mismo.

# 13. Inspirando OKRs con BHAG

Hay varios frameworks que nos están ayudando en matizar estrategias más a largo plazo y que inspiren los OKRs, como la estrella del norte , que busca esa idea de único objetivo de alto nivel de abstracción, que raro es que varíe y que ayuda a centrar y definir el futuro. Y en una línea similar tenemos el BHAG , que yo llevo un tiempo usando en varios sitios y que aquí te lo resumo por si te puede ayudar.

Fueron Jim Collins (el famoso autor de [ Good to Great](https://www.amazon.es/gp/product/0066620996/ref=as_li_qf_sp_asin_tl?ie=UTF8&camp=3626&creative=24790&creativeASIN=0066620996&linkCode=as2&tag=wwwjaviergarz-21) ) y Jerry Porras quienes acuñaron por primera vez el término BHAG en su libro « [Built to Last: Success Habits of Visionary Companies](https://amzn.to/3wfTaN4) » (del año 94).

BHAG es el acrónimo de «Big Hairy Audacious Goal» (la traducción sería algo así como... objetivo grande, audaz y peludo) y su propósito es fijar un objetivo MUY MUY MUY altamente retador, a muy largo plazo, 10 o más años.

Prácticamente, el BHAG está buscando un sueño para la organización, que alinee, motive y haga pensar a muy largo plazo (y que inspire a nuestros OKRs trimestrales).

Ejemplos de libro... Poner al hombre en la Luna (NASA) o poner u n ordenador en cada casa (Microsoft). Ejemplos REALES, míos, de sitios, «cambiar el sector de xxx convirtiéndolo en yyy», «que todos los usuarios de xxxx en 10 años usen yyyy», «ocupar el puesto de xxxx como líder de yyyy», etc. (lo de las xxxx e yyys es por aquello de la confidencialidad).

El BHAG nos ayuda a imaginar el futuro de manera ambiciosa y es un muy buen complemento a la estrella del norte .

Ah, y por si aún tienes dudas de las diferencias entre OKRs y BHAG, los OKRs hablan de objetivos a corto plazo (típicamente trimestrales), mientras que el BHAG trata un objetivo a muy largo plazo.

# 14. Las reuniones de Check-In

Como supongo sabes, y si no pues te lo cuento, típicamente, solemos hacer un evento anual, más orientado a tratar el objetivo genérico del año, el evento trimestral, al final del «quarter», para ver cómo han ido los OKR previos (una retro de OKRs) y planificar los siguientes y, a lo que vamos hoy....  un seguimiento quincenal (a veces hay quien lo hace semanal), de no más de 30 min (yo te recomiendo time-box de 10 min.), que se suele llamar «Check-In» de OKRs.

La MINI reunión de Check-In de OKR es una reunión RÁPIDA, de máximo 10 minutos, a lo Daily, en la que el equipo (o a quién aplique) reflexiona sobre el avance de los OKR.

Lo que buscamos es evitar crear un OKR y acordarnos de él el día antes de su evaluación final (típicamente, al final del trimestre).

## 14.1 La estructura de un Check-In

Hay muchas maneras de estructurar un Check-In de OKRs, pero típicamente estos son los 3 temas que trato:

1. Estado actual del OKR

&nbsp;

1. ¿Vemos el cumplimiento del OKR... con optimismo o pesimismo?
2. Métrica actual de los KR

&nbsp;

2. Micro Retro...

&nbsp;

1. ¿Qué hemos hecho bien en pro del OKR?
2. ¿Qué tenemos que mejorar?

&nbsp;

3. ¿Nuevas acciones la próxima quincena?

Ah, ¿por qué me gusta que sea quincenal? porque los que trabajáis de manera ágil podéis aprovechar la retro para meter dentro la reunión de Check-In de OKR.

# 15. Diez Anti-Patrones de OKR

He hecho una selección de los que más veo que se repiten...

1. Convertir todo lo que hay que hacer en OKR
2. Tener KRs que no se pueden medir o se miden de manera subjetiva
3. Revisar el OKR sólo al final del trimestre
4. Dejar la creación del OKR para los últimos días del trimestre
5. Demasiados OKRs o demasiados KR
6. Los OKRs se crean desde arriba sin participación de los equipos
7. Tener OKRs personales... y no tener de equipo
8. Asociar OKRS a subidas salariales
9. El Objetivo del OKR es cuantitativo
10. Tener tareas en vez de KRs

------------------------------------------------------------------------

# 16. Uniendo el mundo Ágil con el mundo OKR

Sí, mucha gente, en charlas, YouTube, etc., menciona la palabra Ágil al exponer sobre OKRs. Sí, pero con muy poca profundidad.

Sabemos que hay OKRs a diferentes niveles, desde alto nivel, muy de negocio a niveles inferiores. Y sabemos que frameworks como Scrum trabajan a nivel muy operativo, muy de «micro gestión».

Hay mucho dicho sobre OKRs y mucho dicho sobre Agilidad... pero no tanto sobre el uso de ambos de manera combinada.

Y con la moda que hay de OKRs, no estaría de más madurar este punto para aprovecharlos en los muchos equipos que trabajan desde hace años bajo una cultura Ágil.

Te voy a dejar dos áreas donde estamos trabajando, desde hace ya tiempo y de manera profunda, la unión del mundo OKR con el mundo Ágil. Te las voy a mencionar, por si te es útil seguir por ese camino.

## 16.1 OKRs y su influencia en el equipo Ágil

En el mundo Ágil los equipos son básicos. Esos equipos de los que tantas veces te he hablado.

Pero si esos equipos son multifuncionales, auto-organizados, pequeños, con un objetivo común (en el mundo OKR, afortunadamente, [es bastante popular](https://plai.team/blog/individual-okr)  la recomendación de evitar OKRs aplicados a personas, uno de los grandes destructores de equipos) en búsqueda de la eficacia y la eficiencia... ¿no deberíais alinear de alguna manera OKRs con los anteriores?

## 16.2 OKRs y su influencia en el Product Backlog

Sabiendo que los OKRs, principalmente en su «O», vienen de negocio, están relacionados con el negocio... ¿no deberíais alinear epics / el product backlog de los equipos con los OKRs? (y de manera más explícita a lo que se acostumbra).

El tema no es nuevo, aunque esté muy maduro, puedes encontrar [por la web](https://medium.com/@scrumdesk/the-product-backlog-must-be-connected-with-objectives-and-key-results-777928e433d2)  más ideas de cómo conectar los OKR con artefactos como el Product Backlog, típico en equipos Scrum.
