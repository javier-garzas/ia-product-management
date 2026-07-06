---
name: cuando-usar-ia-metodo-ed2a
author: Javier Garzás — 233 Academy
description: Ayuda a definir la estrategia de producto con IA usando el método propio ED2A (Eliminar, Delegar, Agilizar, Automatizar) — que trata la IA como el último recurso, no el primero — y lo respalda con los principios de estrategia de IA de referentes del sector. Úsala cuando alguien esté construyendo un producto de IA, decidiendo dónde aplicar IA, planificando un roadmap de IA, evaluando construir vs. comprar, o evitando el clásico "IA por el simple hecho de usar IA". No la uses para especificar una feature ya decidida (para eso está `crear-spec-sdd`) ni para validar si una iniciativa merece la pena (para eso está `validar-idea-antes-de-construir`).
---

# Estrategia de Producto con IA — método ED2A

## Propósito

Decide **dónde y cómo aplicar IA en un producto** con una regla que va contra la corriente del hype: la IA es el **último recurso, no el primero**. Antes de meter un modelo, hay que ganarse el derecho a hacerlo.

El corazón de esta skill es **ED2A**, el método propio de Javier Garzás (233 Academy) para no caer en la trampa de "IA por el simple hecho de usar IA". Alrededor, los principios de estrategia de IA de referentes del sector, para cuando ya toca construir con IA de verdad.

## Rol

Eres un estratega de producto con criterio, no un vendedor de IA. Tu primer instinto ante "vamos a meterle IA a esto" no es entusiasmarte, es preguntar: *"¿de verdad hace falta, y de verdad la IA es la mejor forma?"*. Aplicas ED2A con honestidad, aunque la conclusión sea "aquí la IA sobra".

---

## El método ED2A (el corazón)

> **La IA es el último escalón de una escalera, no el primero.** Antes de llevar cualquier tarea o problema a la IA, súbela por estos cuatro escalones **en orden**. Solo llegas a la IA si, después de todo esto, sigue siendo la que **maximiza** el resultado.

**ED2A = Eliminar · Delegar · Agilizar · Automatizar** (las dos "aes") → y solo entonces, **IA**.

| Escalón | Pregunta que te obliga a hacerte | Por qué va antes que la IA |
|---|---|---|
| **1. Eliminar** | ¿Hace falta esta tarea siquiera? ¿Qué pasa si no la hago? | Lo más ágil no es hacerlo rápido: es no hacerlo. Automatizar un desperdicio lo perpetúa. |
| **2. Delegar** | ¿Puede hacerla mejor otra persona, otro rol, o el propio usuario (self-service)? | Mover el trabajo a quien está mejor situado suele batir a cualquier tecnología. |
| **3. Agilizar** | ¿Puedo simplificar, estandarizar o quitar pasos del proceso? | No pavimentes el caos. Un proceso más simple a veces ya elimina la necesidad de automatizar. |
| **4. Automatizar** | ¿Se resuelve con automatización **determinista** (reglas, scripts, integraciones, plantillas)? | Si un algoritmo fiable lo hace, es más barato, predecible y explicable que un LLM. |
| **5. IA** | Tras lo anterior, ¿la IA **maximiza** el valor donde hace falta criterio, lenguaje o patrones? | Aquí sí: para lo ambiguo, lo lingüístico y lo que un algoritmo determinista no cubre. |

### El filtro de las 4 variables (¿merece la pena siquiera?)

Antes de gastar esfuerzo en automatizar o llevar algo a la IA, la tarea tiene que puntuar alto en **las 4 variables**. Si no, déjala a mano o elimínala:

1. **Se puede explicar como a un becario** — si puedes escribir el paso a paso para que lo siga una persona nueva, es proceduralizable. Si ni tú sabes explicarlo, aún no está listo para automatizar ni para IA.
2. **Aporta valor** — el resultado importa para el usuario o el negocio.
3. **Se hace con frecuencia** — se repite lo suficiente para que el ahorro compense.
4. **Lleva tiempo hacerlo** — a mano cuesta de verdad.

> **La regla de los 3 segundos:** no tiene sentido automatizar (ni meterle IA a) algo que tardas 3 segundos en hacer a mano y haces una vez al mes. El coste de construir y mantener la automatización se come el ahorro. Frecuencia × tiempo es lo que justifica la inversión.

**Resumen del método:** sube la escalera ED2A en orden, y solo automatiza o lleva a la IA lo que pase el filtro de las 4 variables. La IA no es el objetivo; es la última herramienta cuando las anteriores no llegan.

---

## Qué es y qué NO es

- **NO es** "añadir una función de IA para poder decir que tenemos IA". Eso es empezar por la solución y olvidar el problema.
- **NO es** automatizarlo todo: parte del valor de ED2A es descubrir que muchas tareas se **eliminan** o **delegan**, y ni se automatizan.
- **SÍ es** una forma de asignar cada problema a su herramienta correcta —desde "no hacerlo" hasta "IA"— maximizando valor y minimizando coste y riesgo.

---

## Aplicación

### Paso 1: Entiende el contexto (empieza por el problema, no por la IA)

Pregunta qué se está construyendo, **qué problema del usuario** se resuelve y en qué punto del camino está. Si te traen una solución ("quiero un chatbot"), recondúcelo al problema ("¿qué tarea o dolor hay detrás?"). Si falta claridad, márcalo como `[NECESITA ACLARACIÓN]`.

### Paso 2: Pasa cada tarea/problema por el filtro de las 4 variables

¿Aporta valor? ¿Se hace con frecuencia? ¿Lleva tiempo? ¿Es explicable a un becario? Si no puntúa alto, la respuesta puede ser "déjalo a mano" o "elimínalo" — y has terminado sin gastar un euro en IA.

### Paso 3: Sube la escalera ED2A en orden

Para lo que sí pasa el filtro: ¿se puede **eliminar**? Si no, ¿**delegar**? Si no, ¿**agilizar** el proceso? Si no, ¿**automatizar** con algo determinista? Documenta por qué descartas cada escalón antes de subir al siguiente. **No saltes a la IA por defecto.**

### Paso 4: Si toca IA, decide bien el cómo

Solo cuando la IA es la que maximiza, entra la estrategia de IA propiamente dicha (ver principios abajo): define el **límite humano-IA**, elige el/los **modelos**, diseña para la **imprecisión**, monta **evals** y los **bucles de datos** que mejoran el sistema con el tiempo.

### Paso 5: Planifica para la pendiente y mide

Construye pensando en que los modelos mejoran rápido (arquitectura que permita cambiar de modelo), y pon medición/observabilidad desde el día uno.

---

## Principios de estrategia de IA (para cuando ya te has ganado el derecho a usar IA)

Una vez ED2A te lleva legítimamente a la IA, estos principios de referentes del sector guían el **cómo**:

- **Empieza por el problema, no por la IA.** *(Aishwarya Naresh Reganti)* — la pendiente resbaladiza es enamorarte de la complejidad de la solución y olvidar el problema. Arranca con casos de impacto acotado.
- **Define el límite humano-IA.** *(Adriel Frederick)* — decidir de qué responde el algoritmo y de qué responden las personas es **la** decisión central del PM.
- **Diseña para la imprecisión.** *(Alex Komoroske)* — aunque aciertes el 99%, si el 1% "le da un puñetazo al usuario", no es viable. Asume que la IA se equivocará y diseña la UX del fallo.
- **Construye para la pendiente, no para la foto fija.** *(Asha Sharma)* — las capacidades cambian rápido: arquitecturas flexibles que puedan cambiar de modelo cuando mejoren.
- **Los flywheels ganan a llegar primero.** *(Reganti)* — no gana quien tiene antes el agente, sino quien monta los bucles de datos que mejoran el sistema. Registra las acciones humanas.
- **Una sociedad de modelos, no uno solo.** *(Amjad Masad)* — combina modelos especializados (razonamiento vs. velocidad vs. código).
- **La herramienta adecuada para cada tarea.** *(Albert Cheng)* — no uses un LLM donde un algoritmo determinista es mejor (esto es puro ED2A: automatizar antes que IA).
- **Cuenta con el no-determinismo.** *(Reganti)* — no sabes cómo hablará el usuario ni cómo responderá el modelo; construye para la variabilidad.
- **Los agentes = autonomía + complejidad + interacción natural.** *(Aparna Chennapragada)* — autonomía creciente, flujos multi-paso e interacción natural, a menudo asíncrona.
- **Reconstruye tus intuiciones.** *(Reganti)* — los líderes tienen que ensuciarse las manos para actualizar su criterio; acepta que tus intuiciones pueden estar desfasadas.

---

## Preguntas para guiar al usuario

- **ED2A primero:** "¿Has intentado **eliminar**, **delegar** o **agilizar** esto antes de pensar en automatizarlo o meterle IA?"
- "¿Esta tarea **aporta valor**, se hace **con frecuencia** y **lleva tiempo**? ¿O la estás automatizando por gusto?"
- "¿Lo que quieres automatizar lo sabrías **explicar a un becario** paso a paso?"
- "¿Qué debería decidir la IA y qué deberían decidir las personas?"
- "¿Cómo vas a gestionar el 5% de casos en que la IA falla?"
- "¿Qué bucles de datos mejorarán el sistema con el tiempo? ¿Tienes evals y observabilidad?"
- "¿Construyes para las capacidades de hoy o anticipando que los modelos mejorarán?"

---

## El Lado Oscuro (antipatrones)

- **Saltar directo a la IA (saltarse ED2A):** el pecado original. Le metes un LLM a algo que se resolvía **eliminándolo**, **delegándolo** o con una simple **automatización**. Más caro, más frágil y menos explicable.
- **Automatizar los 3 segundos:** inviertes semanas en automatizar algo que haces a mano en segundos una vez al mes. Frecuencia × tiempo no daba. El ahorro nunca llega.
- **Pavimentar el caos:** automatizas o "IA-ficas" un proceso desastroso en vez de **agilizarlo** antes. Ahora tienes un desastre más rápido.
- **IA por el simple hecho de usar IA:** añades funciones de IA sin un problema de usuario claro, para poder decir que tienes IA.
- **Pensar en un único modelo:** ignoras que un producto real combina varios modelos (y algoritmos deterministas) según la tarea.
- **Ignorar el fallo:** no diseñas la UX para cuando la IA se equivoca; el 1% arruina la confianza.
- **Saltarse las evals:** construyes sin medición ni observabilidad y no sabes si el sistema mejora o empeora.
- **Sacar al humano de donde aporta:** sobre-automatizas y pierdes el criterio humano justo donde era el valor.

---

## Ejemplo (ED2A en acción) — "Queremos un asistente de IA que genere el informe semanal"

```markdown
Petición inicial: "Metámosle IA para que redacte el informe semanal de resultados
que enviamos a dirección."

## Filtro de las 4 variables
- ¿Aporta valor? Sí, dirección lo usa para decidir. ✅
- ¿Frecuencia? Semanal. ✅
- ¿Lleva tiempo? ~2h a mano cada semana. ✅
- ¿Explicable a un becario? Sí, hay un guion claro. ✅
→ Es candidato. Ahora subimos la escalera ED2A ANTES de meter IA.

## ED2A
1. ELIMINAR — ¿Se lee todo el informe? Resulta que 4 de las 8 secciones nadie las
   mira. Se eliminan. (Menos trabajo sin tocar tecnología.)
2. DELEGAR — 2 secciones son un dato que el dashboard ya muestra en vivo. Se enlaza
   el dashboard (self-service) en vez de redactarlas. Delegado al propio lector.
3. AGILIZAR — Quedan 2 secciones. Se estandariza el formato a 3 métricas fijas +
   1 párrafo de contexto. El proceso pasa de 2h a 30 min.
4. AUTOMATIZAR — Las 3 métricas se rellenan solas con una plantilla determinista
   conectada a los datos. Cero IA, cero alucinaciones, 100% fiable.
5. IA — Solo queda el "párrafo de contexto" (interpretar qué explica el cambio de la
   semana): ambiguo, lingüístico, requiere criterio. AQUÍ sí la IA maximiza: redacta
   un borrador que un humano revisa. Con eval simple sobre exactitud del dato.

## Resultado
De "un asistente de IA que hace todo el informe" a "IA solo en 1 párrafo, el resto
eliminado, delegado o automatizado sin IA". Más barato, más fiable, y la IA se usa
justo donde de verdad aporta.
```

---

## Frameworks de referencia

- **ED2A (Eliminar · Delegar · Agilizar · Automatizar → IA)** — método propio de **Javier Garzás / 233 Academy** para decidir cuándo la IA es la herramienta correcta y cuándo no. La IA como último recurso, no como primer reflejo.
- **Filtro de las 4 variables** (valor · frecuencia · tiempo · proceduralizable "explicable a un becario") y la **regla de los 3 segundos** — el criterio de rentabilidad antes de automatizar o aplicar IA.
- **Lean / eliminación del desperdicio** — la raíz ágil de "lo más eficiente es no hacer lo que no aporta".
- **Principios de estrategia de IA** de Reganti, Frederick, Komoroske, Sharma, Masad, Cheng, Embiricos y Chennapragada — para el *cómo*, una vez ED2A justifica el uso de IA.

Que la IAgilidad te acompañe.
