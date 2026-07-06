<!--
  Guia BDD y Gherkin - Javier Garzas / javiergarzas.com.
  Incluida en este repositorio por su autor.
  Licencia: CC BY-NC-SA 4.0 (la misma que el repo).
  Texto convertido desde el documento original (sin imagenes).
-->

# Guía BDD y Gherkin

> **📖 Guía** de la sección [Guías](README.md), por **Javier Garzás** — [javiergarzas.com](https://www.javiergarzas.com).
> Licencia **CC BY-NC-SA 4.0** (como el repositorio). Complementa a las skills [`crear-historias-de-usuario`](../skills/crear-historias-de-usuario/) y [`crear-spec-sdd`](../skills/crear-spec-sdd/), que usan criterios de aceptación en Gherkin.

---

1. Nuestra idea con esta guía

2. BDD en una página

2.1. El proceso de fuera a dentro

2.2. Los talleres de especificación conjuntos: los tres amigos

2.3. El lenguaje común

2.4. Cucumber es una herramienta para la colaboración

3. Gherkin

3.1. Colaboración en un desarrollo tradicional

3.2. Colaboración en un desarrollo ágil con BDD

4. Las Features

4.1. Descripción de la Feature

4.2. ¿Es lo mismo una Feature que una historia de usuario?

5. Cucumber

5.1. Steps Definitions

5.2. Expresiones regulares

6. Los Scenarios

6.1. Given

6.2. When

6.3. Then

6.4. And y But

6.5. Background

6.6. Scenario Outline with Examples

6.7. Paso de argumentos

6.7.1. Cadenas de varias líneas

6.7.2. Tablas de datos

6.8. Etiquetas

6.9. Comentarios

7. Buenas prácticas

7.1. Las Feature deben probar partes o funcionalidades de una aplicación y no la aplicación al completo

7.2. Usar el mismo idioma que los clientes

7.3. Organizar las Feature

7.4. Usar etiquetas

7.5. Escribir Scenarios lo más independientes posible

7.6. Evitar el uso de conjunciones en un mismo Step

7.7. Escribir una narrativa

7.8. Given, When, Then (pasado, presente, futuro)

7.9. Usar los Background de manera coherente

7.10. Estilo imperativo vs estilo declarativo

8. Anexo I: Tidy Gherkin

9. Referencias

# 1. Nuestra idea con esta guía

Debe de haber centenares de cosas escritas sobre BDD (Behavior Driven Development) y sí… esta es una más, con las características especiales de estar en español y estar escrito y pensado para aquellos que desconocen el tema BDD por completo, para en poco tiempo “saber de qué va” esto, sacar la idea principal de por qué esto del BDD es importante y por qué cada vez se habla más de ello.

Hemos escrito esta guía de supervivencia, y hemos sido muy estrictos en que no sea muy extensa, para que sea una lectura rápida, y porque después de años trabajando en proyectos ágiles la comunicación entre la parte técnica (desarrollo y tester) y la parte de negocio (Product Owner, stakeholders) suele ser uno de los mayores retos a conseguir.

En ocasiones, la comunicación entre negocio, desarrollo y Testing se asemeja a una situación de supervivencia, empezando porque el lenguaje de los stakeholders no es el mismo que los desarrolladores, que hace enfrentarnos a una situación tremendamente adversa, y de ahí el título de esta guía y su filosofía.

Frente a una situación de supervivencia, conocer lo imprescindible, técnicas probadas, concretas y prácticas que nos ayuden… esa será la clave de nuestro éxito. Y eso es lo que encontrarás en esta guía, una ayuda para sobrevivir, para seguir adelante, utilizando lo imprescindible y utilizando la agilidad.

Aunque hay multitud de recursos en la web sobre Testing Ágil y en concreto BDD usando Cucumber y Gherkin, en esta guía encontrarás sintetizada la técnica ágil de los puntos historia.

Por último, antes de empezar, recuerda que lo más importante frente a una situación de adversidad son dos cosas: **tu actitud frente a los problemas y tu preparación previa**. Esta guía será tu herramienta imprescindible para la segunda. El resto depende de ti.

Y no olvides que todo lo que aquí te contamos no implica que tú debas hacerlo exactamente de la misma forma. Experimenta. Prueba. De hecho, probablemente nosotros mismos hagamos las cosas de una manera diferente según la situación. La fuerza y lo duro de los marcos ágiles es que tienes que adaptarlos a tu situación específica.

# 2. BDD en una página

*“BDD en un tweet: El uso de ejemplos en multiples niveles para crear un conocimiento compartido y terminar con la incertidumbre, creando software que importa.”*

*-- Dan North*

Las primeras ideas sobre BDD vienen de hace ya años, de allá por 2003, y aunque hoy han sido etiquetadas por muchos sólo dentro del área del Testing, deberíamos tener presente que todo esto no sólo es, ni exclusivamente nació, para el Testing. Behavior-Driven Development ​​o BDD realmente es un proceso de desarrollo software de mayor alcance, más allá del Testing, que realmente nació para evitar los históricos problemas que conllevan las malas y diferentes interpretaciones de las necesidades de negocio (requisitos, historias, etc.) (Hellesøy, A. 2014).

Dan North, el creador de Behavior-Driven Development o BDD, explica que BDD es una metodología de “fuera hacia dentro”, porque comienza desde “fuera” explicando los requisitos de negocio, el comportamiento esperado de aquello que se programará, y desde ahí va profundizando, identificando características que cumplen esos requisitos.

Por otro lado, BDD busca disponer de un lenguaje común para unir la parte técnica y la de negocio, y que sea desde ese lenguaje común desde donde arranque el Testing y el desarrollo.

La idea en BDD es 2.1) dar soporte a un proceso (BDD), 2.2) que apoye en talleres de especificación conjuntos, 2.3) proporcionar un lenguaje común entendible por personas sin conocimientos técnicos (Gherkin), y 2.4) poder disponer de una herramienta que proporcione una fuente única con el comportamiento esperado para el software a desarrollar (Cucumber u otros).

## 2.1. El proceso de fuera a dentro

Fue al propio proceso al que Dan North le llamó BDD y Gojko Adzic le dio otro nombre: Especificación con ejemplos. Al proceso, también se le conoce como “desarrollo de fuera a dentro”  (outside-in software development).

Se llama “de fuera a dentro” porque el desarrollo comienza desde la funcionalidad hacia dentro, hacia el sistema, la funcionalidad guía al desarrollo. Los programadores ejecutan los escenarios que describen cómo se espera que se comporte funcionalmente el sistema con Cucumber, y ello les dice lo que hay que implementar.

Similar a la idea de TDD, pero Cucumber se sitúa en un nivel de abstracción más alto, más cerca del dominio, del negocio, de las necesidades funcionales y más lejos de clases y métodos.

Y para ello, para esa descripción “de fuera a dentro” es muy recomendable hacer uso de un lenguaje común.

## 2.2. Los talleres de especificación conjuntos: los tres amigos

En inglés le llaman así, "los tres amigos", en español queda un poco raro, pero en cualquier caso todo esto viene a que en la definición de una necesidad (requisito, historia, etc.) siempre deben participar “tres amigos”: la persona de negocio, el programador y el tester. 

Los tres especifican con ejemplos cómo el software deberá comportarse y lo escriben en escenarios Gherkin (ver sección 3).

Figura 1. Los tres amigos

## 2.3. El lenguaje común

En BDD se describe funcionalmente el sistema utilizando “**Features”** que contienen “**Scenarios**”, ejemplos concretos de cómo se comportará dicha funcionalidad una vez implementada. Los Scenarios a su vez están formados por “**Steps**” (siguiendo la estructura Given, When y Then) que guiarán a los desarrolladores y testers.

La idea que propone BDD es usar un mismo lenguaje para potenciar la comunicación y colaboración entre desarrolladores, testers y roles no técnicos, o de negocio. 

Bajo el marco de BDD existen varios lenguajes, siendo el más popular Gherkin, si bien hay otros como Behat (es un framework de desarrollo de código abierto basado en comportamiento para PHP) (Behat).

Gherkin es el lenguaje utilizado por Cucumber pero que también se puede utilizar con herramientas como JBehave (JBehave), Lettuce (herramienta para BDD basada en Cucumber para Python) (Lettuce), entre otras.

Figura 2. Estructura de una Feature

## 2.4. Cucumber es una herramienta para la colaboración

La idea que dio origen a Cucumber era la de combinar las “pruebas de aceptación automatizadas”, los “requisitos funcionales” (historias de usuario, etc.) y la “documentación”, todo ello en un formato entendible (Gherkin) por personas sin conocimientos técnicos (Product Owners, negocio, etc.).

Cuando en 2008 se creó Cucumber (Cucumber Backgrounder), lo hizo para proporcionar ese (a) lenguaje común entendible por personas sin conocimientos técnicos (Gherkin), (b) dar soporte a un proceso (BDD) y (c) ser una herramienta que proporcione una fuente única con el comportamiento esperado para el software a desarrollar.

Por ello, el hacer uso de Cucumber es para mucho más que contar con una ayuda para automatizar pruebas. Y esto lo puedes ver claramente en las dos actividades que siempre deben acompañar a Cucumber: los talleres de especificación (tres amigos) y el proceso de “fuera a dentro”.

Cuando Cucumber se usa únicamente como una herramienta para automatizar pruebas y sin la participación de negocio… pierde su valor (ver sección 3).

Cuando se escriben los Scenarios en Gherkin después de haber implementado el software, pierde todas las ventajas.

Las características de Cucumber en Gherkin deben escribirse antes que el código de la aplicación y nacen con los requisitos de software. Cucumber es una herramienta de colaboración, como ya hemos comentado, busca un entendimiento común de las necesidades, basado en la colaboración de tres roles: negocio, desarrollo y Testing.

# 3. Gherkin

“*Hay dos formas de escribir programas sin errores. Solo la tercera funciona.*”

\-- Alan J. Perlis

Gherkin es un lenguaje muy simple, técnicamente es un DSL (Domain Specific Language o Lenguaje de Dominio Específico) muy cercano al lenguaje natural (Gherkin). Usar este lenguaje es de gran ayuda para stakeholders, negocio, desarrollo y testers, ya que proporciona una forma sencilla de escribir necesidades, documentación viva (ya que luego se va a poder ejecutar) y pruebas que puedan ser entendidas por todos.

La idea del lenguaje Gherkin es contar **cómo se comporta** **el software** sin entrar en detalles de implementación. El objetivo de Gherkin es disponer de un lenguaje que sea fácil de leer para todas las partes, técnicos y negocio, que permita a todos tener un entendimiento común que diga qué hay, qué tiene que hacer y cómo debe comportarse una funcionalidad a implementar, y testear, 

La comunicación entre el Product Owner con desarrollo y testers es fundamental (como se ve en la Figura 3) si no se quiere malgastar tiempo. Si desde el primer momento existe una buena comunicación entre ellos, se evitará que haya malentendidos, que los desarrolladores implementen código innecesario o necesidades no requeridas por negocio y como consecuencia que el sistema no se adecue a lo que el cliente quiere.

Figura 3. Colaboración de todo el equipo

## 3.1. Colaboración en un desarrollo tradicional

Cuando hablamos de la comunicación y colaboración entre diferentes roles en un desarrollo tradicional, en cascada, tenemos algo como se muestra en la Figura 4.

En primer lugar, los **stakeholders** comunican en una conversación sus necesidades a un **analista de negocio** quien escribe estas necesidades o requisitos en un documento. Luego los **desarrolladores** traducen estos requisitos en código y los **testers** traducen los requisitos a casos de prueba. Finalmente, una persona con el rol de **documentador técnico** traducirá el código en documentación técnica y funcional, y finalmente se le entregará a los stakeholders.

Figura 4. Comunicación en un desarrollo en cascada

Como se ve en la Figura 4, es una comunicación orientada a documentación, además, los stakeholders no ven el resultado hasta que se les entrega al final, pudiendo así entregar algo que no pedían debido a la falta de comunicación y entendimiento entre todas las partes implicadas.

## 3.2. Colaboración en un desarrollo ágil con BDD

Sin embargo, cuando hablamos de comunicación y colaboración en un desarrollo ágil con BDD (Figura 5), en primer lugar, los **stakeholders** y **Product Owner** tienen una conversación sobre las necesidades de negocio, y el Product Owner con ayuda de los **desarrolladores** y **testers** traducen estas necesidades a historias escritas en Gherkin, a las que vamos a llamar **Features** (ver sección 4). 

Estas Features guían al desarrollador en la implementación del código correspondiente a esa necesidad y actúan como tests automatizados. Finalmente estos tests automatizados proporcionan feedback y ayudan a documentar la aplicación.

Además, se va entregando incrementos a los stakeholders para que puedan ver el progreso de lo que pedían, aumentando así la comunicación y colaboración entre todo el equipo y disminuyendo el riesgo de hacer lo que el cliente no pide o no necesita.

Figura 5. Comunicación en un desarrollo ágil con BDD

A lo largo de la guía veremos las ventajas de usar Gherkin y esta filosofía de trabajo frente a un desarrollo tradicional en cascada.

# 4. Las Features

*"These days we do not program software module by module; we program*

*software by feature by feature."* 

*--Mary Poppendieck*

Las **Features** escritas en Gherkin se pueden escribir, hasta día de hoy, en unos 60 idiomas (Gherkin Languages) aproximadamente para facilitar la comunicación entre negocio, desarrollo y testers. Si no se especifica el idioma, Cucumber tomará por defecto el inglés. 

|  |
| :-: |
| Si quieres usar un idioma específico, en la primera línea de la Feature, tendrás que poner \*\*\\\#language: \\\<código idioma\\\>\*\*, por ejemplo, en español \*\*\\\#language: es\*\*. Si no se pone nada, Gherkin por defecto asume que se va a escribir en inglés. Usando el lenguaje que hablen los clientes, será más fácil la comunicación con ellos. Para obtener información sobre los idiomas que abarcan basta con ejecutar en la línea de comandos: \*\*$ cucumber\*\* \*\*--i18n help\*\* Y se puede saber cuáles son las palabras clave de un idioma en particular usando el comando: \*\*$ cucumber --i18n \\\<código del idioma\\\>\*\* Si queremos saber las palabras claves en español por ejemplo: \*\*$ cucumber --i18n es\*\* |

Veamos un primer ejemplo en la siguiente figura.

Figura 6. Ejemplo de una Feature

Cada Feature empieza con la palabra clave “**Feature:**” (si se utiliza Gherkin en inglés). Después de “Feature:” se escribe una descripción donde se indica de qué trata la prueba que se va a implementar.

Las Features en Gherkin se escriben en ficheros de texto plano con la extensión “.feature”, por lo que te vale un simple bloc de notas para crearlas, aunque existen herramientas un poco más elaboradas, como Tidy Gherkin (ver Anexo I), que es una extensión de Chrome, y ayuda a escribir las Feature más cómodamente usando el navegador y a traducir el escenario escrito en Gherkin en el esqueleto de un caso de prueba (o Step Definition, ver sección 5.1) en algún lenguaje de programación.

Además también existen otros editores muy fáciles de usar, como por ejemplo (Gherkin Editor). Gherkin Editor es un editor de texto para escribir especificaciones usando Gherkin.  Cualquiera de las opciones son muy fáciles de usar.

Los criterios de aceptación o **Scenarios** son una parte intrínseca de la Feature porque definen el alcance de su comportamiento y dan una definición de cuándo la Feature está terminada (Definition of Done). A continuación se muestra una imagen de cómo se estructura una Feature.

Hablaremos de todas las palabras claves más adelante, pero por poner un simple ejemplo, la Feature “Have a lorry” (Tener un camión) tendría la siguiente forma:

**Feature**: Have a lorry

**As** a Rocker

**I want to** a lorry

**Because** I want to be happy

**Scenario**: Buy a lorry

**Given** I can’t transport my guitar rocker

**When** buy a lorry

**Then** I play the guitar on a world tour

Gherkin sirve para documentar y, además, ayudar a automatizar lo que luego se convertirá en test. Si se quiere utilizar alguna herramienta de automatización de pruebas, existen multitud de ellas que entienden el lenguaje de Gherkin, como por ejemplo Cucumber y que permitirán transformar esas especificaciones en pruebas automatizadas.

Figura 7. Con Gherkin automatizamos pruebas de navegadores y pruebas unitarias.

Las Features en Gherkin son especificaciones ejecutables y tiene dos propósitos: servir como documentación de un proyecto y para pruebas automatizadas.

Figura 8. Propósito de Gherkin

## 4.1. Descripción de la Feature

Para describir una Feature puedes hacer uso de todo el texto que quieras en la descripción, siempre y cuando no se incluyan las palabras **Scenario**, **Background** o **Scenario Outline**, ya que también son palabras clave. 

Realmente, todo el texto entre la palabra clave Feature y la palabra clave **Scenario**, **Background** o **Scenario** **Outline** es texto libre, es decir, puedes poner ahí lo que quieras, puedes incluso no poner nada. Pero lo sensato es que ahí describas de manera concisa, y mínima, la funcionalidad del software que se quiere construir. 

|  |
| :-: |
| Lo primero a tener claro es que las Features nos dicen el \*\*qué\*\* hay que construir, qué quieren los usuarios, y no el \*\*cómo\*\*. Se expresan en términos de negocio y en un idioma, y lenguaje, que todos puedan entender. Las Features deben describir los objetivos del negocio y son responsabilidad tanto del equipo técnico (testers y desarrolladores) como del Product Owner. |

Según (Dan North) , una Feature está compuesta por un título, una descripción “Como \[rol\], quiero \[objetivo\], para poder \[beneficio\]” y unas pruebas de aceptación. BDD no obliga a tener una estructura definida para describir una Feature, pero Dan North presenta esta estructura porque le ha demostrado que funciona en muchos proyectos de diferentes tipos y tamaños.

(Dan North) en su artículo recomienda que el título tiene que describir una actividad. Hasta que no se implemente esa Feature, esa actividad, el usuario no va a poder utilizar esa funcionalidad del sistema, lo que va a permitir saber cuándo está “terminada” (Definition of Done). 

La Feature debe ser lo suficientemente pequeña como para poder desarrollarse en una iteración, debe ser la unidad de funcionalidad básica, y por tanto de entrega y también se utilizan como una base en la estimación cuando se planifica.

## 4.2. ¿Es lo mismo una Feature que una historia de usuario?

|  |
| :-: |
| Según (Ferguson, J.S., 2015), las historias de usuario se parecen mucho a las Features. Una historia de usuario no tiene que ser un entregable de forma aislada, pero sí que pueden centrarse en un aspecto en particular de una Feature. Las historias de usuario pueden ayudar a planificar y organizar cómo se va a construir una Feature.  Aunque una historia de usuario no se puede poner en producción por sí misma, sí que se puede y además se debe mostrar las historias terminadas o prototipos a los usuarios finales y otras partes interesadas, para asegurarse de que se está construyendo lo correcto y recibir feedback de los usuarios finales.   En muchos proyectos, las Feature que hemos estado debatiendo estarían representadas como historias de usuario de más alto nivel, y a algunos equipos no les resulta necesario romper las Feature en historias más pequeñas. Esto está bien y funciona bien en proyectos más pequeños como dice (Ferguson, J.S., 2015) Hay algunas ventajas de mantener una distinción entre los dos:   - Una Feature es una funcionalidad del software que se entrega a los usuarios finales o a otras partes interesadas que necesitan para alcanzar los objetivos de negocio.   - Una historia de usuario es una herramienta de planificación que ayuda a profundizar en los detalles de lo que se necesita para ofrecer una característica particular. Es importante recordar que las historias de usuario están planeadas esencialmente como artefactos. Son una gran manera de organizar el trabajo que hay que hacer para ofrecer una función o necesidad, pero el usuario final no le importa la forma de organizar las cosas para conseguir la Feature con tal de que esta se entregue. Una vez que la Feature ha sido implementada, las historias de usuario pueden darse por terminadas. Una Feature se puede construir o entregar con relativa independencia de otras Features y ser probado por los usuarios finales de forma aislada. Las Features se utilizan a menudo para planificar y documentar releases. Pero eso es según (Ferguson, J.S., 2015), para nosotros una Feature y una historia de usuario es lo mismo. Las historias de usuario no son sólo un artefacto de planificación, sino un requerimiento, una descripción de una necesidad de los usuarios finales al igual que una Feature. En esta guía cuando hablemos de Features también nos estaremos refiriendo a historias de usuario.   |

# 

# 5. Cucumber

*“Hace mucho tiempo que en la computación no teníamos un ritmo de cambio como éste; probablemente desde el nacimiento de la computación personal”*

\-- Larry Page

(Cucumber) es una de las herramientas software (escrita en Ruby) más típicas que se utilizan en BDD para convertir los Scenarios escritos en Gherkin en el esqueleto de una prueba o en la definición de un paso (Step Definition). Estas pruebas se codifican en un lenguaje de programación, como podría ser Java o Ruby, entre otros. 

Cuando Cucumber ejecuta un Scenario, si el sistema se comporta como se ha descrito en él, se dice que el Scenario se ha pasado, es decir, el Scenario ha tenido éxito (succeed), si no ocurre, entonces el Scenario ha fallado (failed). Cada vez que se añada un nuevo Scenario y al ejecutar Cucumber, lo marque como pasado, se habrá añadido una nueva funcionalidad al sistema. 

A continuación vamos a ver las definiciones de los pasos o Steps Definitions y la relación con los Steps del Scenario de una Feature.

## 5.1. Steps Definitions

Los **Steps Definitions** (o definición de los pasos o esqueleto del caso de prueba) son la transformación automática por parte de Cucumber de los Scenarios de Gherkin, los Steps Given/When/Then que los encontramos en los archivos .feature, en código, en un lenguaje de programación (o en expresiones regulares como veremos más adelante)  (ver Figura 9).

Un Step Definition es código o expresiones regulares que sigue el patrón del Step, que es el texto que le sigue a la palabra clave.

Figura 9. Transformación que hace Cucumber de cada Step en, para este ejemplo, lenguaje Ruby

En la Figura 9 podemos observar varias cosas en la salida del terminal. Por un lado la Feature que queremos automatizar (marcada en morado) y junto al Scenario y los Steps (en azul) su ubicación (marcado en verde). 

En rojo resaltamos el Step de la Feature con su correspondiente Step Definition, en naranja resaltamos la expresión regular para relacionar un Step con su Step Definition y en amarillo irá el código para pasar la prueba, que en un principio muestra un mensaje de pendiente puesto que no hay nada implementado.

Aunque no esté marcado en la Figura 9, también se puede observar que Cucumber nos muestra el número de Scenarios de la Feature (en este ejemplo 1 Scenario) y el número de Steps (5 Steps en nuestro caso), además del estado en el que se encuentra, es decir, si aun no se ha definido, si ha fallado, o si se ha pasado, así como el tiempo que tarda en ejecutarse.

Cuando Cucumber relaciona un Step con un Step Definition, pasa el valor que encuentra en el Step a los argumentos del Step Definitions como parámetro, porque luego en la implementación de las pruebas se tratan como variables (ver Figura 10). 

Figura 10. Relación del valor de un Step y argumento de un Step Definition

Para que Cucumber pueda convertir los Steps de la Feature en Steps Definitions, debemos colocar cada fichero .feature según una estructura de directorios, para que Cucumber sepa ejecutar los .feature y transformarlos en los correspondientes Steps Definitions.

La estructura a seguir es la siguiente:

  - Prueba\_test

      - features

          - my\_feature.feature
          - step\_definitions

              - código.\<extensión del lenguaje de programación a utilizar\>

Figura 11. Estructura para ejecutar una prueba

Se necesita una carpeta raíz desde donde vamos a lanzar Cucumber (en el caso de la Figura 11 es “Prueba Garras”). Dentro de esta carpeta necesitamos otra carpeta llamada “features” donde Cucumber va a buscar las Features (los archivo .feature). Si no encuentra esta carpeta, se mostrará un mensaje diciendo que no se ha encontrado la carpeta features como en el de la Figura 12.

Figura 12. Cucumber no encuentra la carpeta features

Y dentro de la carpeta features necesitamos una carpeta llamada “step\_definitions” en la que tendremos los Step Definitions, el código correspondiente para pasar la prueba en archivos con la extensión del lenguaje de programación a usar para pasar la prueba, por ejemplo .java o .rb.

Dependiendo en qué lenguaje vayas a implementar la prueba, el Step Definition seguirá una estructura diferente, no obstante, siempre se usan las expresiones regulares. 

Por ejemplo, en Ruby, un Step Definition comienza con una palabra clave (**Given/When/Then**), seguido la expresión regular y la palabra **DO**, luego el código a implementar para pasar la prueba y finaliza con la palabra **END** (se puede ver en cualquiera de los ejemplos que mostramos).

Sin embargo, en Java el Step Definition sigue la estructura de una función o método, es decir, **@palabra\_clave** seguido de la expresión regular, y cerrando la función con llaves. A modo de ejemplo y para entender esto mejor, a continuación mostramos los Step Definition de la Feature de la Figura 6. Para este ejemplo, se ha usado Tidy Gherkin (ver Anexo I).

Figura 13. Steps Definitions usando Java

## 5.2. Expresiones regulares

Como se comentaba en la sección anterior, da igual en qué lenguaje de programación vayas a implementar tus pruebas, Cucumber cuando transforma un Step a un Step Definition propone una expresión regular.

Las expresiones regulares comienzan con el símbolo “**^**” y termina con “**$**“ (se pueden ver ejemplos en las Figuras 13 y 15). Veamos en la Tabla 1 algunos ejemplos de expresiones que podemos utilizar ( expresiones Regulares (Humanizing Work, 2011):

|  |  |
| :-: | :-: |
| \*\*Patrón\*\* | \*\*Descripción\*\* |
| · | Cualquier carácter (excepto el salto de línea) una o ninguna vez. |
| .\\\* | Cualquier carácter (excepto el salto de línea) 0 o más veces.  |
| .+ | Cualquier carácter (excepto el salto de línea) por lo menos una vez. |
| .{2} | Dos caracteres. |
| .{1.3} | De uno o tres caracteres.  |
| ^pattern | Marca el inicio de cadena.  |
| pattern$ | Marca el final de la cadena.  |
| \\\[0-9\\\]\\\*\\\\d\\\* | Serie de números o nada.  |
| \\\[0-9\\\]+ \\\\d+ | Uno o más números.  |
| “\\\[^\\\\”\\\]\\\*” | Cualquier cosa (menos las comillas) entre comillas.  |
| ? | Hace el carácter o el grupo opcional.  |
| \| | Lógico (true\|false). |
| (pattern) | Grupo. Cucumber lo utiliza para capturar el valor para el método. |
| (?:pattern) | Como el de arriba solo que no se captura el grupo. |
| \\\\s | Representa un espacio en blanco. |
| \\\\w | Representa cualquier carácter. |
| \\\\S | Cualquier carácter que no sea un espacio en blanco. |
| \\\\n | Nueva línea. |

Tabla 1. Expresiones regulares 

Estas expresiones regulares se utilizan para enlazar o relacionar el código que implementaremos en el Step Definition para pasar la prueba con los Steps correspondientes de nuestra Feature (ver Figura 15).

El código dentro de cada Step Definition será lo que Cucumber ejecute para evaluar un Step y ver si se pasa la prueba o no.

# 

# 6. Los Scenarios

*“Cualquier tonto puede escribir código que un ordenador entienda. Los buenos programadores escriben código que los humanos pueden entender.”*

\-- Martin Fowler

Los **Scenarios** son una de las estructuras básicas y más importantes de Gherkin. Cada Scenario es un ejemplo de cómo se espera que se comporte la Feature.

Un Scenario está formado por la palabra clave **Scenario:** seguida de una lista de lo que se conoce como Steps, donde cada Step comienza por una de las siguientes palabras clave:  Given, When o Then.

Se utiliza **Given** para indicar el contexto donde ocurre el Scenario (precondición), **When** para indicar cómo interactuar con el sistema (acción) y **Then** para comprobar que el resultado es el que se espera (postcondición).

Cada Feature puede contener uno o varios Scenarios. Y, a su vez, un Scenario puede contener tantos Steps (Given / When / Then) como se desee pero recomendamos que haya entre 3 y 6 Steps por Scenario, ya que si son muy grandes pierden su fuerza expresiva y se vuelven poco mantenibles.

Figura 14. Ejemplo de un Scenario con varios Given y varios When

Al igual que la Feature, también el Scenario y sus Steps se deben centrar en los objetivos de negocio, que, además de servir como documentación será también una prueba de aceptación. En su conjunto, los Scenarios son una especificación del sistema (ver Figura 14). 

Un Scenario bien descrito sólo debe probar una acción y deben describir lo que una Feature debe hacer, no de cómo debe hacerlo.

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*En la Figura 15 se puede ver cómo Cucumber transforma el Scenario al esqueleto del caso de prueba o Steps Definitions y la relación entre los Steps y Steps Definition usando la Feature de la Figura 14.Figura 15. Relación entre Steps y Steps Definition |

Cucumber no diferencia entre las palabras clave, pero elegir las palabras más adecuadas es importante para la legibilidad del Scenario en su conjunto. Es decir, para Cucumber da igual poner la palabra clave Then en lugar de When o Given, Cucumber no lo va a diferenciar, pero es recomendable ponerlo con un orden lógico para dar una estructura y una coherencia al Scenario.

Por poner un ejemplo, puedes escribir: **When** (**precondición**) y seguido **Given** (**acción**) y Cucumber lo ejecutará y lo dará como válido al igual que poniendo Given (**precondición**) When (**acción**) Figura 16 (se ha usado la Feature de la Figura 14 cambiando el orden de los Steps).

Figura 16. Steps intercambiados

Como se puede ver en la Figura 16, Cucumber te propone los Steps Definitions sin importarle el orden de las palabras clave. 

A pesar de que las palabras claves no lleven un orden, la descripciones de los Steps sí que siguen un orden, precondición, acción y resultado, independientemente de las palabras clave. Por eso... ¡Ojo\!, no puedes poner:

When necesito defenderme (**que es la acción**)

Given me he convertido en un superhéroe (**que es la precondición**)

En este caso dará error, no en la primera ejecución de Cucumber, pero sí cuando implementes los Steps Definitions, porque, en el caso del ejemplo, “necesito defenderme” es la acción y “me he convertido en un superhéroe” la precondición, por lo que dará error si quieres ejecutar la acción sin haber ejecutado antes la precondición. Esto ocurre cuando el Given, la precondición, no sólo se utiliza como información.

Hay ciertas palabras clave y símbolos para hacer los Steps, en la siguiente tabla puedes ver un resumen que iremos detallando a continuación

|  |  |
| :-: | :-: |
| Given | Describe el contexto inicial, postcondición (ver sección 6.1, pag 33) |
| When  | Describe una acción (ver sección 6.2, pag 34) |
| Then | Describe los resultados esperados, postcondición (ver sección 6.3, pag 34) |
| And y But | Step Igual al Step anterior (ver sección 6.4, pag 34) |
| Background | Agrupa Steps repetidos en diferentes Scenarios (ver sección 6.5, pag 39) |
| Scenario Outline con Examples | Scenario con un mismo patrón y diferentes valores (ver sección 6.6, pag 43) |
| """ | Cadenas de texto (ver sección 6.7.1, pag 46) |
| \| | Tablas de datos (ver sección 6.7.2, pag 47) |
| @ | Etiquetas (ver sección 6.8, pag 49) |
| \\\# | Comentarios (ver sección 6.9, pag 53) |

Tabla 2. Palabras y símbolos claves

## 6.1. Given

El Step que comienza con la palabra clave **Given** se utiliza para describir el contexto inicial, describe las condiciones previas para la prueba. Por lo general es algo que sucedió en el pasado, por lo que se suelen expresar en pasado, para que sea más obvio indicar estas acciones. 

Se debe conocer el estado de la aplicación o la situación de partida con sólo leer el Step Given.

El Step Given tiene todas las precondiciones que deberían ocurrir antes de la acción que se quiere probar. A veces, un Step Given puede ser puramente informativo, para proporcionar el contexto de la aplicación, incluso si no se requiere ninguna acción en la aplicación se puede obviar este paso.

## 6.2. When 

El Step When se utiliza para describir un evento o una acción. Y dicha acción generará un resultado que se podrá comprobar en el siguiente Step del Scenario, el Step Then que veremos a continuación.

Es muy recomendable que solo haya un único Step When por Scenario. Si se necesitas añadir más, por lo general, es una señal de que debe dividir el Scenario en múltiples Scenarios. 

Al igual que con Given, When también debería describir la acción en términos de “**qué**”, no de “**cómo**”.      

## 6.3. Then

El propósito de **Then** es describir los resultados esperados tras la acción que describió el When. El Step Then debe inspeccionar la salida del sistema (un informe, algo por interfaz de usuario, un mensaje, la salida de un comando, etc.).

Ten cuidado al principio, porque cuando no se tiene mucha experiencia con BDD, un fallo habitual es confundir el Step When con el Then.

## 6.4. And y But 

Hay ocasiones en las que se necesita usar varios Steps Given seguidos en un mismo Scenario (o When o Then). Una opción es añadir Steps repitiendo la palabra clave Given (o When o Then) según necesites como se muestra en la siguiente imagen.

Figura 17. Feature con varios Given y When 

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si ejecutamos Cucumber, nos mostrará cada palabra clave, con su respectiva expresión regular:Figura 18. Ejecución de Cucumber |

Otra opción es, si hay varios Step con la misma palabra clave (por ejemplo Given, Given, When, When, Then), en lugar de repetir las palabras clave (como en la primera opción), también podemos usar otras como **And** y **But** (que también son palabras clave).

Nosotros recomendamos siempre que se pueda usar las palabras claves And y But, en vez de repetir reiteradamente Given, When o Then, ya que el principal objetivo del uso de And y But es escribir los Scenarios más fáciles de leer (ver Figura 19  y 21).  Pero ojo,  que si la lista de "And o But" se empieza a alargar es síntoma de malos olores, algo empieza a ir mal.

Figura 19. Feature usando And

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si ejecutamos Cucumber, cada And en el Step Definition se convertirá en Given y When respectivamente (igual pasaría con la palabra clave Then):Figura 20. Ejecución de una Feature con And |

Normalmente, la palabra clave But se usa para expresar alguna restricción o alguna dificultad en el Scenario, pero de cara a Cucumber, actúa como la palabra clave del Step anterior (ver Figura 21 y 22). 

Figura 21. Feature usando And y But

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si ejecutamos Cucumber, en el Step Definition el And y el But se convertirán en la palabra clave When:Figura 22. Ejecución de una Feature con And y But |

## 6.5. Background

Es posible que de vez en cuando te encuentres Steps repetidos en los diferentes Scenarios. Para evitar que se repitan en cada uno de los Scenarios, se pueden agrupar bajo una sección inicial llamada **Background,** ubicada antes del primer Scenario.

Dicho de otra manera, **Background:** en una Feature se utiliza para especificar un conjunto de Steps que son comunes para todos los Scenarios de la Feature.

En la siguiente imagen podemos ver un ejemplo en el que tenemos dos Scenarios y en cada uno de esos Scenarios dos Steps iguales (los Steps Given y And). 

Figura 23. Feature con Steps repetidos en Scenarios diferentes sin usar Background

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Cucumber convierte los Steps repetidos en un solo Step Definition por lo que en el ejemplo de la Figura 23 tendremos 2 Steps Definitions (uno por cada Step con la misma palabra clave). Esto Cucumber lo hace para reutilizar código. Por último también muestra los 4 Steps Definitions correspondientes a los Steps restantes de cada Scenario (marcados en azul y verde). Ver Figura 24.Figura 24. Ejecución de Cucumber de la Feature de la Figura 23 |

Para mayor legibilidad y mantenibilidad podemos refactorizar la Feature de la Figura 23, agrupando los Steps repetidos utilizando la sección Background como se muestra en la Figura 25:

Figura 25. Feature usando Background

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Aunque la estructura de la Feature cambie, la salida al ejecutar Cucumber no cambia, si comparas la Figura 24 con la Figura 26, sigue habiendo 6 Steps Definitions. Esto se debe a que la refactorización no cambia el comportamiento de las pruebas, ya que los Steps que están en Background se ejecutan al principio de cada Scenario, como antes. Además, hace que los Scenarios individuales sean más fáciles de leer.Figura 26. Ejecución de Cucumber de la Feature de la Figura 24 |

No solo la palabra Given puede ir en la sección Background, cualquiera de las palabras clave Given, When, Then, And o But pueden agruparse en la sección Background. 

Pero ojo, hay veces que la palabra clave Given no es meramente informativo, y la sección Background se ejecuta al principio de cada Scenario, si escribes una acción (When) en Background y la precondición (Given) en el Scenario, dará error del tipo **Unable to find field “x”** porque ejecutará antes la acción que la precondición, no en la primera ejecución de Cucumber, pero al implementar los Steps, como se explicó en la sección 5.1. Y esto ocurre porque no encuentra la información que se requiere previamente en el Given.

## 6.6. Scenario Outline with Examples 

Hay veces que se tienen muchos Scenarios que siguen exactamente el mismo patrón de Steps cambiando solo algunos valores o la salida. 

Usamos esta opción cuando se tiene una necesidad de negocio compleja con diferentes variables y valores o varias salidas, y nuestra Feature tiene varios Scenarios iguales y que sólo se diferencian por sus valores.

Tantos Steps repetidos no ayudan a que la Feature y Scenarios sean fáciles de leer y puede ocasionar multitud de problemas, como por ejemplo un mantenimiento tedioso, problemas de copy-paste, etc. lo que no nos ayudará a tener unas pruebas de calidad.

En la siguiente imagen se muestra un ejemplo de esto, una Feature con tres Scenarios con Steps completamente iguales, salvo los valores numéricos.

Figura 27. Scenarios iguales con valores diferentes

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Como se muestra en la Figura 28, a pesar de tener tres Scenarios con tres Steps cada Scenario, en el Step Definition tendremos solo tres Steps Definitions, puesto que todos los Steps son iguales y solo cambian los valores. Tener más Steps en la Feature que Steps Definitions puede ser algo lioso y tedioso a la larga.Figura 28. Ejecución de Cucumber |

Para mejorar estos Scenarios, Gherkin permite usar en nuestras Features la sección **Scenario Outline:** con el que se especifica primero el patrón de los Steps y siempre acompañado de ejemplos bajo la sección “**Examples:**”. De esta manera no existen repeticiones. Tendremos un único Scenario y una tabla con todos los valores.

Usaremos los símbolos \<...\> y el nombre de una variable para indicar que ahí va el valor (de la sección Examples) que hay que sustituir (ver Figura 29).

El Scenario Outline siempre es seguido por una o más secciones de Examples, que son tablas para indicar los valores con los que sustituiremos las variables.

La tabla debe tener una fila de encabezado correspondiente a las variables del Scenario Outline (será la primera fila). Cada una de las siguientes filas al encabezado creará un nuevo Scenario, rellenando los valores de las variables.

Mediante el símbolo | separamos la tabla en columnas y mediante el salto de línea separamos la tabla en filas.

A continuación se muestra la Feature de la Figura 27 usando Scenario Outline con Examples para escribir la Feature con mayor legibilidad, mantenibilidad y calidad.

Figura 29. Scenario Outline con Examples

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si te fijas en la Figura 28, la salida al ejecutar Cucumber es la misma que la Figura 30. De esta manera se ve que el comportamiento no cambia.Figura 30. Ejecución de Cucumber de la Feature de la Figura 27 Como se puede ver en la imagen anterior, la primera fila de la tabla de Examples corresponde a las variables de los Steps (palabras entre los símbolos \\\< \\\>), y las filas restantes los valores por los que sustituiremos cada variable. |

## 6.7. Paso de argumentos

En ocasiones concretas, necesitamos una tabla de datos o un texto más amplio para probar un sistema. Para esto, Gherkin nos proporciona cadenas de datos y tablas, vamos a verlas.

### 6.7.1. Cadenas de varias líneas

Las cadenas son útiles para la especificación de un texto más amplio. La sintaxis se inspira en la sintaxis de String de Python usando la llamada sintaxis PyString (Behat Guides).

El texto debe estar delimitado entre tres comillas dobles (""" texto """) y automáticamente se pasa como el último parámetro en el Step Definition, como se muestra  en la Figura 32. 

Figura 31. Uso de la cadena de caracteres

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si ejecutamos Cucumber, en la siguiente imagen (Figura 32), podemos ver como el texto entre las comillas “”” “””  pasa a ser argumento del primer Step Definition, correspondiente al Given.Figura 32. Paso de una cadena de caracteres de la Feature como Argumento del Step Definition |

### 6.7.2. Tablas de datos

Las tablas de datos son muy útiles para pasar una lista de valores o una tabla de datos como argumentos al Step Definition (ver sección 5.1). Las tablas siguen la misma estructura que Scenario Outline con Examples, pero la tabla es específica a un Step, en cambio con Scenario Outline con Examples la tabla de la sección Examples abarca todos los Steps del Scenario (ver sección 6.6). 

Figura 33. Ejemplo de una tabla de datos

La primera fila de la tabla es usada para la cabecera de las columnas donde indicando un nombre específico. La tabla especificada en el Scenario es del tipo clave-valor, donde la primera columna va a ser la clave y la segunda columna el valor, por lo que la forma más recomendada de hacerlo es al estilo hash. 

Cucumber nos proporciona **rows\_hash.** Usando por ejemplo la sentencia **data = table.rows\_hash** podremos acceder a los valores de la tabla **data\["Garras"\]** y obtendremos “Para poder arañar y atacar a enemigos”. Esta es la manera más fácil de abordar este tipo de tablas, ya sea añadir, en este caso poderes, modificarlos, etc.

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Si ejecutamos Cucumber, como vemos en la Figura 33, la tabla del Step de nuestra Feature pasa a ser argumento del Step Definition correspondiente, en este caso al Step Given, y con rows\\\_hash se podrá acceder a la tabla.Figura 34. Ejecución de Cucumber del ejemplo de tablas de datos |

## 6.8. Etiquetas

Las etiquetas son una muy buena forma de agrupar y organizar los Scenarios y las Features. Son cadenas y se puede colocar tantas etiquetas como se desee por encima de palabras clave. 

Si tenemos pocos Scenarios puede tener menos sentido usar etiquetas, pero si tenemos muchos Scenarios (aunque no es lo recomendable) y además representan necesidades o propósitos diferentes las etiquetas son muy útiles para organizarlos.

Para añadir una etiqueta en la Feature basta con poner el símbolo **@** (arroba) y el texto que se desee. Por ejemplo podemos organizarla con etiquetas como @small @medium y @large o tal vez @hare, @tortoise, y @sloth.

En el ejemplo de la Figura 34 se utiliza la etiqueta para priorizar. Esto sirve para decirle a Cucumber que ejecute solo aquellos escenarios con ciertas etiquetas o para excluir los Scenarios con esas etiquetas por ejemplo.

Figura 35. Ejemplo de etiquetas

|  |
| :-: |
| \*\*¿Qué hace Cucumber?\*\*Podemos ejecutar los Scenarios por separado usando las etiquetas. En la Figura 36 se puede ver cómo se ejecuta el Scenario con la etiqueta @Prioridad1. Para ello simplemente hay que usar la sentencia \*\*$cucumber --tags @Prioridad1.\*\* Y en la Figura 37 se muestra cómo se ejecuta solo el Scenario con la etiqueta @Prioridad2 usando \*\*$cucumber --tags @Prioridad2.\*\* Figura 36. Ejecutar un Scenario mediante una etiquetaFigura 37. Ejecutar un Scenario mediante una etiqueta |

Es posible que tengas varios Scenarios, y quieras ejecutar más de uno, pero no todos, para ello simplemente tienes ejecutar la sentencia **$cucumber --tags \<etiqueta\> --tags \<etiqueta\>**. Cada etiqueta separada por un espacio. Para el caso de nuestro ejemplo, habría que ejecutar **$cucumber --tags @Prioridad1 --tags @Prioridad2**.

Las etiquetas se heredan de los elementos primarios. Por ejemplo, si se coloca una etiqueta por encima de una Feature, todos los Scenarios en función de que obtendrán dicha etiqueta. Del mismo modo, si se coloca una etiqueta encima de un Scenario Outline o Examples todos los Scenarios derivados de Examples (las filas) heredarán las etiquetas.

Un Scenario o Feature puede tener tantas etiquetas como desee, simplemente basta con separarlos con espacios. El uso de etiquetas permiten mantener los Scenarios de una Feature juntos, y ejecutarlos por separado.

La ventaja de separarlos de esta manera es que se puede ejecutar los Scenarios seleccionandolos por etiquetas, es decir, ejecutar los Scenarios más rápido con más frecuencia, o ejecutar los Scenarios muy grandes o lentos durante la noche.

Otra idea, también se pueden especificar etiquetas para entornos ya que puede haber pruebas que no quieres que se ejecuten en producción.

Además esto es muy útil si tienes cucumber integrado a un servidor de integración contínua con los tests automatizados , y con las etiquetas los Test más pesados van en la build de la noche.

## 6.9. Comentarios 

En Gherkin se puede escribir comentarios para documentar las Feature y Scenarios. El lugar más recomendado es antes de los Scenario, pero con una buena descripción no serían necesarios los comentarios.

Si queremos indicar un comentario, basta con iniciar una línea con el símbolo **\#** (almohadilla) para decirle a Cucumber que el resto de la línea es un comentario y no debe ser ejecutado (cuando ejecutamos Cucumber, los comentarios no se ven reflejados en el Steps Definitions).

Figura 38. Comentarios en una Feature

Hay un caso concreto en el que el símbolo **\#** no actúa como comentario y es para determinar el idioma de Gherkin (ver la sección 3). Escribiendo en la primera línea de la Feature **\#** seguido de **language:** y el código del idioma, especificaremos el idioma en el que vamos a escribir las Feature.

Por ejemplo si quiero usar el español bastaría con poner en la primera línea **\#language: es**. Si no, Cucumber toma como predeterminado el inglés como ya se ha comentado en varias ocasiones. 

# 7. Buenas prácticas 

*"Los buenos programadores usan sus cerebros, pero unas buenas directrices nos ahorran de tener que hacerlo en cada caso"*

*--* Francis Glassborow

Cuando hacemos uso de BDD, empezamos escribiendo historias de usuario/Features (ver seccion 4.2) usando el DSL Gherkin (Carretero, N., 2015) por lo que estamos empezando el Testing desde el principio con la toma de requisitos. 

Una de las mayores dudas que pueden surgir al respecto es **cómo escribir nuestras Features**. A continuación, vamos a ver una serie de buenas prácticas (en concreto 10) para escribir buenas Features, los más eficientes, legibles y mantenibles posibles.

Después de leer esta guía, deberías saber escribir buenas Features más allá de escribir líneas escritas en Gherkin.

## 7.1. Las Feature deben probar partes o funcionalidades de una aplicación y no la aplicación al completo

Como ya se ha comentado en varias ocasiones, una Feature representa una funcionalidad del software que se quiere construir, características o necesidades que piden los usuarios, por eso se les da ese nombre. 

Es una parte del software final que funciona y que además será de gran valor para los usuarios. 

## 7.2. Usar el mismo idioma que los clientes

Que exista una buena comunicación entre la parte no técnica del equipo (los clientes y Product Owner) y la parte técnica (desarrolladores y tester) es muy importante para poder desarrollar y entregar lo que realmente los clientes necesitan.

Al final el propósito de Gherkin es crear un entendimiento compartido proporcionando un lenguaje de negocio que entiende tanto la parte técnica del equipo como la no técnica (ver sección 3) y así mejorar la comunicación entre ellos y que en las conversaciones se puedan identificar cuáles son las necesidades de los clientes.

## 7.3. Organizar las Feature

Una forma útil de organizar los Scenarios es, por ejemplo, por la rapidez con que se ejecutan. Se puede utilizar 2 o 3 niveles de granularidad para esto:

  - **Fast**: en este nivel pondremos aquellos Scenarios que se ejecutan muy rápido, por ejemplo por debajo de una décima de segundo.

  - **Slow**: en este nivel tendremos aquellos Scenarios que son más lentas que “fast”, pero no extremadamente lentas, así como por ejemplo de un segundo.

  - **Glacial**: en este nivel tendremos aquellos Scenarios que se toman un tiempo largo para ejecutarse.

No tienes por qué seguir esta organización o división, puedes usar la organización que mejor se adecúe a vosotros, ponerlos en subdirectorios separados, usar etiquetas (como vamos a ver a continuación en el siguiente punto), etc.

## 7.4. Usar etiquetas

Las etiquetas  (ver sección 6.8)  son una muy buena forma de agrupar y organizar los Scenarios y las Feature. Son cadenas y se puede colocar tantas etiquetas como se necesiten.

Se puede organizar las Feature usando las etiquetas, y clasificándolas como se muestra a continuación:

  - **Cuándo se deben de ejecutar**: por ejemplo usando etiquetas como @checkin @hourly o @daily

  - **Las dependencias externas que tienen**: usando etiquetas como @local, @database o @network

  - **Nivel**: con etiquetas como por ejemplo @functional, @system o @smoke

Y así todas las que se te vayan ocurriendo para tener bien organizados tus Scenarios, sobre todo en caso de que se tengan varios Scenarios.

## 7.5. Escribir Scenarios lo más independientes posible

Lo ideal es que no haya ningún tipo de acoplamiento y dependencia entre los Scenarios, que sean lo más independientes y autónomos posible unos de otros (por eso recomendamos que haya 1 o 2 Scenarios por Feature). De no ser así podría crear problemas si, por ejemplo, el orden de ejecución de los Scenarios se modifica o se ejecutan en paralelo.

## 7.6. Evitar el uso de conjunciones en un mismo Step

Cada Step debe hacer una cosa. Cuando hay un mismo Step que contiene dos acciones separadas mediante una conjunción “y” se recomienda dividirlo en dos Steps diferentes. El tener una acción en cada paso aumenta la capacidad de reutilización. Esta no es una regla general, puede haber en un mismo Step dos acciones, sin embargo, la mayoría de las veces es mejor evitarlos. 

## 7.7. Escribir una narrativa

Las narrativas describen en aproximadamente una frase lo que una Feature hace o de lo que trata (ver sección 4.1). Normalmente contienen un beneficio para el usuario, un rol y una función del mismo. Las narrativas son importantes para saber qué va a implementar esa Feature, debido a esto debería ser lo primero. También contienen una breve descripción de la función para que otros usuarios que la lean obtengan un conocimiento aproximado de qué se trata sin leer los Scenarios.

## 7.8. Given, When, Then (pasado, presente, futuro)

Como ya se ha comentado en la sección 6, los Steps se expresan en pasado, presente y futuro para entender mejor las Features:

  - Given \<a context\>: El Step **Given** se utiliza para describir el contexto inicial del sistema,

describe las condiciones previas para la prueba. Por lo general es algo que sucedió en el pasado, por lo que se suelen expresar en pasado, para que sea más obvio indicar estas acciones.

  - When \<something happens\>: El Step **When** se utiliza para describir un evento o una acción, por ejemplo una persona que interactúa con el sistema, en este caso escribiremos el evento en presente.

  - Then \<you expect some outcome\>: El propósito del Step **Then** es observar los resultados, por lo que se utiliza para describir los **resultados** o **resultados esperados**, por lo que escribiremos el Step en futuro.

## 7.9. Usar los Background de manera coherente

Si utilizamos los mismos Steps en el comienzo de todos los Scenarios de una Feature, lo ideal es quitar esos Steps de los Scenarios y ponerlos bajo la sección de Background de la Feature como se vio en la sección 6.5. 

Los Background se ejecutan antes de cada Scenario. Pero hay que tener cuidado de no poner demasiados Steps en el Background pues pueden llegar a ser difíciles de entender y de mantener.

## 7.10. Estilo imperativo vs estilo declarativo

Los Scenarios deben ser escritos tal y como un usuario podría describirlos (estilo declarativo). Cuidado con los Scenarios que describen solamente hacer clic en enlaces y rellenando los campos del formulario, o de pasos que contienen código (estilo imperativo).

El estilo imperativo es solo otra variante de la programación, pero ciertamente no es una descripción de la necesidad (como cuando escribimos en estilo declarativo). En cualquier caso…

El estilo **imperativo** usa Steps que resume gran parte de la interfaz de usuario. Esto une el Scenario a esa interfaz y requiere más decisiones de diseño realizados por front.

Debido a la granularidad de los Scenarios, estos se vuelven muy frágiles, ya que están sujetos a cambios en los requisitos del cliente. Si, por ejemplo, se añade un nuevo campo, se debe actualizar el Scenario para reflejarlo, a pesar de que el objetivo subyacente del Scenario no haya cambiado.

Figura 39. Ejemplo de una Feature escrita en Estilo Imperativo

 El estilo **declarativo** está más alineado con las historias de usuarios.

La primera cosa que debemos observar de este estilo es que la cantidad de Steps es menor que en el estilo imperativo, lo que es algo bueno (puedes ver un ejemplo de Feature escrito en este estilo más abajo). El estilo imperativo tiende a producir Scenarios con muchos Steps.

Con el estilo declarativo el objetivo del Scenario sigue siendo claro. Cuando se añade un nuevo Step, el Scenario no tiene que ser modificado.

Figura 40. Ejemplo de una Feature escrita en Estilo Declarativo

Aunque creemos que el estilo declarativo tiene muchos puntos fuertes es posible que no siempre sea la mejor opción para todas las situaciones. El estilo imperativo no se debe descartar por completo, si se usa con prudencia en el Scenario se pueden poner ciertos aspectos de la funcionalidad y mejorar así la comunicación.

También es importante darse cuenta de que los dos estilos no son mutuamente excluyentes. Los estilos se pueden mezclar lo largo de una aplicación, una Feature, e incluso un Scenario individual para proporcionar el nivel adecuado de granularidad según requiera la situación.

Uno de los factores más importantes para decidir qué estilo utilizar (aparte de por el mantenimiento o la duplicación de código) es el cliente. Las Feature tienen el propósito de facilitar la comunicación entre el negocio, desarrollador y tester sobre el valor del negocio y la funcionalidad:

  - Si la necesidad de los interesados está en los campos de un formulario se indica en el Scenario con el fin de tener la confianza en el sistema (por parte de los clientes), usando así el estilo imperativo.

  - Si las especificaciones son sólo para el desarrollador, si bien estas historias pueden estar actuando como pruebas de integración para el desarrollador que no es el propósito original, pero necesitan ser entendidas por una audiencia más amplia que desarrolladores, para alcanzar un entendimiento entre todas las partes interesadas, entonces usaremos un estilo declarativo.

A esto, al igual que en la mayoría de las áreas de desarrollo software, no existe una respuesta correcta, al final solo depende de la situación.

# 

# 8. Anexo I: Tidy Gherkin

*"Recuerda: no eres torpe, no importa lo que digan esos libros. Los torpes de verdad son gente que, creyéndose expertos técnicos, no podrían diseñar hardware y software manejable por usuarios normales aunque la vida les fuera en ello"*

*--* Walter Mossberg

La sintaxis de Gherkin se escribe sobre texto plano en ficheros .feature, como comentábamos al principio de esta guía, como es lógico y usual, por lo que cualquier editor tipo “Bloc de notas” sería suficiente.

Frente a ponerse a codificar Gherkin directamente, contra un editor de texto plano y luego pasar por línea de comando el fichero .feature a una herramienta que dé el esqueleto, en un lenguaje de programación de las pruebas (en Java, Ruby, etc.), hay herramientas que te ayudan a transformar una característica en el esqueleto de una prueba, como por ejemplo, Specflow para Visual Studio u otros (Plugins para Eclipse).

Tidy Gherkin es un plugin fácil de usar para Chrome. Se puede descargar y abrir con Chrome y habilitar un editor de Gherkin, más bonito que un bloc de notas, sin tampoco grandes lujos, pero que asiste con las palabras clave y, además, en una ventana inferior va creando el esqueleto de la prueba ya en un lenguaje de programación.

La siguiente imagen muestra la ventana de Tidy Gherkin. En la parte de arriba vamos a escribir nuestra Feature escrita en Gherkin. Y en la parte de abajo, nos mostrará el esqueleto del caso de prueba de nuestra Feature (lo que corresponde a ejecutar por primera ver por línea de comando cucumber) en el lenguaje que se desee, hasta ahora en Java, en Ruby y en JavaSript. 

Figura 41. Tidy Gherkin, un plugin de Google Chrome

Para mostrar su funcionamiento de una manera más gráfica, se ha cogido un ejemplo de las figuras  anteriores, y se ha escrito en la parte de arriba del Tidy Gherkin.

Figura 42. Feature en Tidy Gherkin

La siguiente figura es el esqueleto del caso de prueba o Step Definition (como veremos a continuación) escrito en Java, el propio Tidy Gherkin lo ha convertido.

Figura 43. Steps Definitions o esqueleto del caso de prueba en Java

Tidy Gherkin también te permite convertir la Feature en Steps Definitions escritos en Ruby como se muestra en la siguiente figura.

Figura 44. Steps Definitions en Ruby

Y la última novedad de Tidy Gherkin es poder traducir una Feature escrita en Gherkin en Steps Definitions o esqueleto del caso de prueba escrito en JavaScript. 

Figura 45. Steps Definitions en JavaScript

En comparación al bloc de notas, la línea de comando o la opción plugin en IDE, está aparentemente solución fácil, es muy útil para contar todo esto a usuarios no técnicos.

# 9. Referencias

Behat. Behat A php framework for autotesting your business expectations., from <http://docs.behat.org/en/v3.0/>

Behat Guides. writing features - gherkin language from <http://docs.behat.org/en/v2.5/guides/1.gherkin.html>

Carretero, N., (2015) DSL Gherkin, 2015, from. <http://www.javiergarzas.com/2015/06/bdd-behavior-driven-development-3.html>

Cucumber. Cucumber from <https://cucumber.io>

Cucumber Backgrounder. Cucumber Backgrounder., from <https://github.com/cucumber/cucumber/wiki/Cucumber-Backgrounder>

Dan North. WHAT’S IN A STORY?., from <https://dannorth.net/whats-in-a-story/>

Ferguson, J.S., (2015) BDD in Action, 2015 from <https://www.amazon.com/BDD-Action-Behavior-driven-development-lifecycle/dp/161729165X>

Gherkin. Gherkin., from[ https://github.com/cucumber/cucumber/wiki/Gherkin](https://github.com/cucumber/cucumber/wiki/Gherkin)

Gherkin Editor. Gherkin Editor., from <https://gherkineditor.codeplex.com/wikipage?title=Overview&referringTitle=Home>

Gherkin Languajes. gherkin/gherkin-languages.json., from <https://github.com/cucumber/gherkin/blob/master/gherkin-languages.json>

Hellesøy, A. (2014). The world's most misunderstood collaboration tool., 2014, from <https://cucumber.io/blog/2014/03/03/the-worlds-most-misunderstood-collaboration-tool>

Humanizing Work (2011).  Cucumber Regular Expressions Cheat Sheet, 2011, from [http://agileforall.com/wp-content/uploads/2011/08/Cucumber-Regular-Expressions-Cheat-Sheet.pdf ](http://agileforall.com/wp-content/uploads/2011/08/Cucumber-Regular-Expressions-Cheat-Sheet.pdf)

JBehave. JBehave What is JBehave?., from <http://jbehave.org>

Lettuce. Lettuce 0.2.23 (kryptonite release) documentation., from <http://lettuce.it/intro/overview.html>

Plugins para Eclipse. cucumber-eclipse-plugin from https://github.com/QuBiT/cucumber-eclipse-plugin
