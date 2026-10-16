---
name: cuando-usar-ia-metodo-e2ad
author: Javier Garzás · 233 Academy
description: Ayuda a decidir qué tareas, procesos o problemas merecen llevarse a la IA (y cuáles no) con el método propio E2AD de Javier Garzás (Eliminar, Agilizar, Automatizar y, solo con lo que quede, Delegar), que trata la IA como el último recurso, no el primero, y lo respalda con los principios de estrategia de IA de referentes del sector. Úsala cuando alguien esté construyendo un producto de IA, decidiendo dónde aplicar IA, planificando un roadmap de IA, evaluando construir vs. comprar, o evitando el clásico "IA por el simple hecho de usar IA". No la uses para especificar una feature ya decidida (para eso está `crear-spec-sdd`) ni para validar si una iniciativa merece la pena (para eso está `validar-idea-antes-de-construir`).
---

# Cuándo usar IA: el método E2AD

## Propósito

Decide **qué merece ir a la IA y qué no** con una regla que va contra la corriente del hype: la IA es el **último recurso, no el primero**. Antes de meter un modelo, hay que ganarse el derecho a hacerlo.

El corazón de esta skill es **E2AD**, el método propio de Javier Garzás (233 Academy) que se explica en el capítulo 16 de su libro *Irremplazable en la era de la IA*. Alrededor, los principios de estrategia de IA de referentes del sector, para cuando ya toca construir con IA de verdad.

## Rol

Eres un estratega con criterio, no un vendedor de IA. Tu primer instinto ante "vamos a meterle IA a esto" no es entusiasmarte, es preguntar: *"¿de verdad hace falta, y de verdad la IA es la mejor forma?"*. Aplicas E2AD con honestidad, aunque la conclusión sea "aquí la IA sobra".

---

## El método E2AD (el corazón)

> **Automatizar un desperdicio es fabricar basura más rápido.** Antes de llevar cualquier tarea a la IA, pásala por estos cuatro filtros **en orden**. Lo que se resuelve en un filtro ya no pasa al siguiente.

**E2AD = Eliminar · Agilizar · Automatizar · Delegar** (las dos "aes" van en medio).

### Paso 0: el volcado cerebral

Si no sabes lo que haces, es difícil mejorarlo. Antes de filtrar, haz una lista de todas las tareas recurrentes (diarias, semanales, mensuales, trimestrales) con su área y su frecuencia. No es burocracia: es poner delante lo que hoy vive difuso en tu cabeza.

| Filtro | Pregunta que te obliga a hacerte | Por qué va en este orden |
|---|---|---|
| **1. Eliminar** | ¿Aporta valor? ¿Genera negocio, nos hace la vida mejor o nos ayuda a descubrir nuevos negocios? | Lo que no aporta es desperdicio: no se agiliza, ni se automatiza, ni se delega. Se elimina, exista o no la IA. |
| **2. Agilizar** | ¿Se puede hacer con menos pasos, menos aprobaciones o menos personas? | Un proceso con pasos de más tiene desperdicio dentro: automatizarlo no lo arregla, lo consagra. |
| **3. Automatizar** | ¿Pasa el semáforo? (ver abajo) | La A más seductora y la más peligrosa. Solo la cruza lo que tiene el semáforo en verde. Si un algoritmo determinista lo resuelve, mejor que un LLM; la IA, para lo ambiguo o lingüístico. |
| **4. Delegar** | Con lo que queda: ¿lo podría hacer otra persona? | Si no, has llegado a lo que solo puedes hacer tú. Por el camino te has quitado muchísimo trabajo. |

### El semáforo de la A de Automatizar

Puntúa cada tarea de **1 a 5** en tres variables. Si los números y la media son bajos, ni te lo plantees:

1. **¿Es procedimentable?** ¿Podrías escribir el paso a paso? ¿Se lo explicarías a un becario en una hoja? Si sí, puede convertirse en un prompt o en una skill. Si no, es tarea creativa y no va.
2. **¿Se hace muchas veces?** Cada día o cada semana, sí. Una vez al año, no compensa la complejidad.
3. **¿Lleva tiempo?** Minutos u horas. Si es instantánea, automatizarla solo añade una pieza más que un día se romperá.

> **El punto dulce** es la tarea que puntúa alto en las tres: procedimentable, frecuente y pesada. Vuélcalas en una tabla, puntúalas y automatiza de arriba abajo, empezando por las que hacen pleno.
>
> **La regla de los 3 segundos:** no tiene sentido automatizar (ni meterle IA a) algo que tardas 3 segundos en hacer a mano y haces una vez al mes.

### Trabaja por MVP

Añadir es fácil y quitar es una pesadilla. No le des a la IA toda la tarea el primer día: dale una parte pequeña y clara, comprueba que la hace bien y solo entonces súmale la siguiente. Ve de menos a más.

### Lo que NO le das a la IA

Saber qué no darle a la IA es tan profesional como saber qué darle. Cuatro territorios que no se cruzan:

- **El criterio:** elegir la estrategia, decidir a quién contratas.
- **Las relaciones:** la conversación difícil, la mala noticia.
- **Lo irreversible:** decisiones sobre personas, dinero o salud.
- **La marca personal:** donde tu cara, tu voz o tu gusto son irremplazables.

Los cuatro fallan casi siempre en el "procedimentable": no sabrías escribir en una hoja cómo decides una estrategia. Esa imposibilidad no es un defecto: es la señal de dónde está tu valor.

---

## Qué es y qué NO es

- **NO es** "añadir una función de IA para poder decir que tenemos IA". Eso es empezar por la solución y olvidar el problema.
- **NO es** un método para automatizar más rápido: es para decidir con criterio qué merece automatizarse. Parte de su valor es descubrir que muchas tareas se **eliminan** o se **agilizan** y ni se automatizan.
- **SÍ es** una forma de asignar cada tarea a su destino correcto (eliminar, agilizar, automatizar o delegar), maximizando valor y minimizando coste y riesgo.

---

## Aplicación

### Paso 1: Entiende el contexto (empieza por el problema, no por la IA)

Pregunta qué se está construyendo, **qué problema del usuario** se resuelve y en qué punto del camino está. Si te traen una solución ("quiero un chatbot"), recondúcelo al problema ("¿qué tarea o dolor hay detrás?"). Si falta claridad, márcalo como `[NECESITA ACLARACIÓN]`.

### Paso 2: Haz el volcado

Lista las tareas o subtareas implicadas, con su frecuencia y el tiempo que llevan.

### Paso 3: Pásalas por E2AD en orden

¿Se puede **eliminar**? Si no, ¿**agilizar**? Si sigue en pie, ¿pasa el **semáforo** para **automatizar**? Lo que queda, ¿se puede **delegar**? Documenta por qué cada tarea se resuelve en un filtro y no en otro. **No saltes a la IA por defecto.**

### Paso 4: Si toca IA, decide bien el cómo

Cuando lo que pasa el semáforo pide IA (y no un algoritmo determinista), entra la estrategia de IA propiamente dicha (ver principios abajo): define el **límite humano-IA**, elige el/los **modelos**, diseña para la **imprecisión**, monta **evals** y los **bucles de datos** que mejoran el sistema con el tiempo. Empieza por un MVP.

### Paso 5: Planifica para la pendiente y mide

Construye pensando en que los modelos mejoran rápido (arquitectura que permita cambiar de modelo), y pon medición y observabilidad desde el día uno.

---

## Principios de estrategia de IA (para cuando ya te has ganado el derecho a usar IA)

Una vez E2AD te lleva legítimamente a la IA, estos principios de referentes del sector guían el **cómo**:

- **Empieza por el problema, no por la IA.** *(Aishwarya Naresh Reganti)* La pendiente resbaladiza es enamorarte de la complejidad de la solución y olvidar el problema. Arranca con casos de impacto acotado.
- **Define el límite humano-IA.** *(Adriel Frederick)* Decidir de qué responde el algoritmo y de qué responden las personas es **la** decisión central del PM.
- **Diseña para la imprecisión.** *(Alex Komoroske)* Aunque aciertes el 99%, si el 1% "le da un puñetazo al usuario", no es viable. Asume que la IA se equivocará y diseña la UX del fallo.
- **Construye para la pendiente, no para la foto fija.** *(Asha Sharma)* Las capacidades cambian rápido: arquitecturas flexibles que puedan cambiar de modelo cuando mejoren.
- **Los flywheels ganan a llegar primero.** *(Reganti)* No gana quien tiene antes el agente, sino quien monta los bucles de datos que mejoran el sistema. Registra las acciones humanas.
- **Una sociedad de modelos, no uno solo.** *(Amjad Masad)* Combina modelos especializados (razonamiento vs. velocidad vs. código).
- **La herramienta adecuada para cada tarea.** *(Albert Cheng)* No uses un LLM donde un algoritmo determinista es mejor.
- **Cuenta con el no-determinismo.** *(Reganti)* No sabes cómo hablará el usuario ni cómo responderá el modelo; construye para la variabilidad.
- **Los agentes = autonomía + complejidad + interacción natural.** *(Aparna Chennapragada)* Autonomía creciente, flujos multi-paso e interacción natural, a menudo asíncrona.
- **Reconstruye tus intuiciones.** *(Reganti)* Los líderes tienen que ensuciarse las manos para actualizar su criterio; acepta que tus intuiciones pueden estar desfasadas.

---

## Preguntas para guiar al usuario

- **E2AD primero:** "¿Has intentado **eliminar** o **agilizar** esto antes de pensar en automatizarlo o meterle IA?"
- "¿Esta tarea **aporta valor** de verdad? ¿O la estás automatizando por inercia?"
- "¿Lo que quieres automatizar lo sabrías **explicar a un becario** paso a paso? ¿Se hace **muchas veces**? ¿**Lleva tiempo**?"
- "¿Cuál es el MVP: la parte más pequeña que podrías darle a la IA esta semana?"
- "¿Qué debería decidir la IA y qué deberían decidir las personas?"
- "¿Cómo vas a gestionar el 5% de casos en que la IA falla?"
- "¿Qué bucles de datos mejorarán el sistema con el tiempo? ¿Tienes evals y observabilidad?"

---

## El Lado Oscuro (antipatrones)

- **Saltar directo a la A de Automatizar (saltarse E2AD):** el pecado original, casi siempre por FOMO. Le metes un LLM a algo que se resolvía **eliminándolo** o **agilizándolo**. Más caro, más frágil y menos explicable.
- **Automatizar los 3 segundos:** inviertes semanas en automatizar algo que haces a mano en segundos una vez al mes. El ahorro nunca llega.
- **Consagrar el caos:** automatizas un proceso con pasos de más en vez de **agilizarlo** antes. Ahora tienes un desastre más rápido.
- **Entrar a saco:** cuarenta automatizaciones encadenadas de golpe, sin MVP. Ahora no puedes quitar ninguna sin que se caiga otra.
- **IA por el simple hecho de usar IA:** añades funciones de IA sin un problema de usuario claro, para poder decir que tienes IA.
- **Ignorar el fallo:** no diseñas la UX para cuando la IA se equivoca; el 1% arruina la confianza.
- **Saltarse las evals:** construyes sin medición ni observabilidad y no sabes si el sistema mejora o empeora.
- **Cruzar los territorios humanos:** le das a la IA el criterio, las relaciones, lo irreversible o tu marca personal.

---

## Ejemplo (E2AD en acción): "Queremos un asistente de IA que genere el informe semanal"

```markdown
Petición inicial: "Metámosle IA para que redacte el informe semanal de resultados
que enviamos a dirección."

## Volcado
- Informe semanal a dirección: semanal, ~2 h a mano. 8 secciones.

## E2AD
1. ELIMINAR: ¿se lee todo el informe? Resulta que 4 de las 8 secciones nadie las
   mira. Se eliminan. (Menos trabajo sin tocar tecnología.)
2. AGILIZAR: 2 secciones son un dato que el dashboard ya muestra en vivo; se enlaza
   el dashboard en vez de redactarlas. Las 2 que quedan se estandarizan a 3 métricas
   fijas + 1 párrafo de contexto. Pasa de 2 h a 30 min.
3. AUTOMATIZAR: semáforo de lo que queda.
   - 3 métricas: procedimentable 5 · frecuencia 4 · tiempo 3 → sí. Plantilla
     determinista conectada a los datos. Cero IA, cero alucinaciones.
   - Párrafo de contexto: procedimentable 3 · frecuencia 4 · tiempo 4 → con
     supervisión. La IA redacta un borrador (ambiguo, lingüístico) que un humano
     revisa, con una eval simple sobre la exactitud del dato. Se empieza por un MVP:
     una semana de prueba antes de darlo por bueno.
4. DELEGAR: la revisión del borrador no tiene por qué hacerla quien dirige el
   área: puede hacerla otra persona del equipo con un checklist.

## Resultado
De "un asistente de IA que hace todo el informe" a "IA solo en 1 párrafo, el resto
eliminado, agilizado o automatizado sin IA". Más barato, más fiable, y la IA se usa
justo donde de verdad aporta.
```

---

## Frameworks de referencia

- **E2AD (Eliminar · Agilizar · Automatizar · Delegar)**: método propio de **Javier Garzás / 233 Academy**, explicado en el capítulo 16 de *Irremplazable en la era de la IA*, para decidir qué merece ir a la IA y qué no. La IA como último recurso, no como primer reflejo.
- **El semáforo** (procedimentable · frecuencia · tiempo, de 1 a 5) y la **regla de los 3 segundos**: el criterio de rentabilidad antes de automatizar o aplicar IA.
- **Volcado cerebral**, inspirado en *Getting Things Done* de David Allen.
- **Lean / eliminación del desperdicio**: la raíz ágil de "lo más eficiente es no hacer lo que no aporta".
- **Principios de estrategia de IA** de Reganti, Frederick, Komoroske, Sharma, Masad, Cheng, Embiricos y Chennapragada, para el *cómo*, una vez E2AD justifica el uso de IA.

Que la IAgilidad te acompañe.
