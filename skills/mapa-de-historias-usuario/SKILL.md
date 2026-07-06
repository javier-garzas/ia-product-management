---
name: mapa-de-historias-usuario
author: Javier Garzás — 233 Academy
description: Crea un mapa de historias de usuario (user story mapping, de Jeff Patton) que despliega la columna vertebral de actividades, sus pasos y tareas, y traza las líneas de release para separar el MVP de lo que viene después. Úsala cuando arranques un producto o una funcionalidad grande, quieras construir entendimiento compartido entre producto, diseño e ingeniería, priorizar un backlog en torno al viaje del usuario o definir qué entra en el MVP. No la uses para aterrizar UNA historia en detalle (para eso está `crear-historias-de-usuario`) ni para mapear emociones y puntos de dolor de la experiencia (para eso está `mapa-viaje-cliente`).
---

# Mapa de Historias de Usuario (User Story Mapping)

## Propósito

Visualiza el viaje del usuario como un **mapa en dos dimensiones**: en horizontal, la historia de lo que la persona hace de principio a fin; en vertical, la prioridad, que te deja dibujar las líneas de release y separar el MVP de lo demás.

Esto **no es un backlog**: es un artefacto estratégico que muestra *cómo* los usuarios logran su objetivo y, a partir de ahí, informa *qué* construir y *en qué orden*. Un backlog es una lista plana que esconde el todo; un story map lo enseña de un vistazo.

## Rol

Eres un facilitador de producto senior formado en la técnica de Jeff Patton. Sabes que el mayor valor de un story map no es el dibujo, sino la **conversación** que lo produce: por eso no lo construyes en aislamiento y luego lo "presentas", sino que lo levantas con el equipo. Cuando no tengas evidencia de cómo se comporta el usuario, lo dices y lo marcas como `[SUPOSICIÓN: ...]` en vez de inventarlo.

## Qué es un story map (y qué NO es)

Ten claro el marco, Rebelde IAgil, porque es lo que separa un mapa útil de una lista disfrazada.

### El marco de Jeff Patton

El story mapping organiza el trabajo en una estructura 2D:

**Eje horizontal (de izquierda a derecha) — el viaje del usuario en el tiempo:**
- **Columna vertebral (backbone):** las actividades de alto nivel que el usuario realiza.
- **Pasos:** las acciones concretas dentro de cada actividad.
- **Tareas:** el trabajo detallado necesario para completar cada paso.

**Eje vertical (de arriba abajo) — prioridad y releases:**
- **Filas superiores:** lo esencial (MVP / Release 1).
- **Filas inferiores:** lo deseable (releases futuros).

```
Segmento → Persona → Narrativa (objetivo del usuario)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Actividad 1] → [Actividad 2] → [Actividad 3] → [Actividad 4]   ← BACKBONE
     ↓              ↓              ↓              ↓
  [Paso 1.1]     [Paso 2.1]     [Paso 3.1]     [Paso 4.1]        ← PASOS
  [Paso 1.2]     [Paso 2.2]     [Paso 3.2]     [Paso 4.2]
· · · · · · · · · · · línea de release: MVP · · · · · · · · · · ·
  [Tarea R1]     [Tarea R1]     [Tarea R1]     [Tarea R1]        ← MVP
· · · · · · · · · · · línea de release: R2 · · · · · · · · · · · ·
  [Tarea R2]     [Tarea R2]     [Tarea R2]     [Tarea R2]        ← futuro
```

### Por qué funciona

- **Centrado en el usuario:** organiza el trabajo en torno a los objetivos de la persona, no a los módulos de ingeniería.
- **Entendimiento compartido:** producto, diseño e ingeniería ven el mismo viaje a la vez.
- **Claridad de priorización:** arriba = MVP, abajo = iteraciones futuras.
- **Detecta huecos:** los pasos o tareas que faltan saltan a la vista.
- **Planifica releases:** las líneas horizontales definen el alcance de cada entrega.

### Qué NO es

- **No es un Gantt:** no es gestión de proyectos ni fechas, es el viaje del usuario.
- **No es una lista de funcionalidades:** las actividades son *comportamientos* del usuario, no features del producto.
- **No es estático:** el mapa evoluciona según aprendes más de los usuarios.

### Y no lo confundas con sus skills hermanas

- **`mapa-viaje-cliente`** mira la **experiencia** (emociones, puntos de dolor): sirve para saber dónde sufre el cliente, no para planificar qué construir.
- **`crear-historias-de-usuario`** aterriza **UNA** historia en detalle (Gherkin, DoD). El story map **informa** esas historias; no las reemplaza.

### Cuándo usarlo / cuándo no

Úsalo al arrancar un producto o una funcionalidad grande, para alinear a stakeholders, para priorizar el backlog según el usuario, para separar MVP de futuro y para incorporar a gente nueva a la visión.

No lo uses para funcionalidades triviales (no mapees lo que ya entiendes), cuando los flujos cambian a cada minuto (el mapa estabiliza flujos), ni como sustituto de las historias de usuario.

---

## Aplicación

**Antes de empezar (léelo, Rebelde IAgil):** si hay material del usuario (entrevistas, analítica, soporte, un mapa previo), léelo primero — el viaje sale de la evidencia. Y siempre que puedas, **mapea en equipo**: el artefacto vale, pero la conversación vale más.

### Paso 1: Define el contexto (segmento y persona)

**Segmento — ¿para quién construyes?** Específico, no "usuarios": *"diseñadores freelance que gestionan varios clientes a la vez"*.

**Persona — dale cara dentro de ese segmento:** demografía, comportamientos, dolores y objetivos.
> *Ej.: "Sara, diseñadora gráfica freelance de 35 años, lleva 5-10 proyectos a la vez, lucha con la facturación y el cobro, quiere menos administración y más diseñar."*

### Paso 2: Define la narrativa (el objetivo)

¿Qué intenta lograr la persona? Formúlalo como un **Job To Be Done**, enfocado en el resultado y en **una sola frase**.
> *Ej.: "Entregar un proyecto de cliente desde el arranque hasta cobrar la factura final."*

Si no cabe en una frase, el alcance es demasiado amplio: pártelo.

### Paso 3: Identifica las actividades (la columna vertebral)

Lista **3-5 actividades** de alto nivel que la persona atraviesa para cumplir la narrativa. Reglas: son **secuenciales** (izquierda→derecha), describen lo que el **usuario hace** (no lo que el producto ofrece), y si te salen 10 es que estás mezclando actividades con pasos.

### Paso 4: Descompón cada actividad en pasos

Para cada actividad, **3-5 pasos** que detallen cómo se lleva a cabo. Cada paso es **accionable y observable** (podrías ver a alguien hacerlo) y sigue una secuencia lógica.

### Paso 5: Descompón cada paso en tareas

Para cada paso, las **tareas** concretas. Granulares y específicas; incluye tanto lo visible para el usuario ("enviar el email") como lo de entre bastidores ("recibir la confirmación"). Son las que priorizarás en vertical.

### Paso 6: Prioriza en vertical y traza las líneas de release

Ordena las tareas de arriba abajo por prioridad y **dibuja las líneas de release**:
- **MVP / Release 1:** lo imprescindible para que el usuario complete el viaje de punta a punta (el *walking skeleton*: fino pero entero).
- **Release 2:** importante, no crítico.
- **Futuro / deseable:** lo demás.

La regla de oro del MVP en un story map: una fina rebanada horizontal que **cruza todas las actividades** y ya entrega valor completo — no una columna entera perfecta y las demás vacías.

### Paso 7: Busca huecos y oportunidades

Repasa el mapa: ¿faltan pasos o tareas?, ¿hay puntos de dolor sin abordar?, ¿oportunidades de deleitar?, ¿fluye todo de forma lógica de izquierda a derecha?

---

## Plantilla

```markdown
# Mapa de historias: [PRODUCTO / FUNCIONALIDAD]

**Segmento**: [a quién sirve]
**Persona**: [nombre + contexto, dolores, objetivos]
**Narrativa (JTBD)**: [el objetivo del usuario en una frase]

## Columna vertebral → pasos → tareas (por release)

### Actividad 1: [comportamiento del usuario]
Pasos: [paso 1.1] · [paso 1.2] · [paso 1.3]
- **MVP**: [tarea] · [tarea]
- **R2**: [tarea]
- **Futuro**: [tarea]

### Actividad 2: [comportamiento del usuario]
Pasos: [paso 2.1] · [paso 2.2]
- **MVP**: [tarea] · [tarea]
- **R2**: [tarea]
- **Futuro**: [tarea]

## Huecos y oportunidades
- [lo que falta o la oportunidad detectada]
```

---

## Ejemplo (completo) — Sara, diseñadora freelance

```markdown
# Mapa de historias: Herramienta de gestión para diseñadores freelance

**Segmento**: diseñadores freelance que gestionan varios clientes a la vez.
**Persona**: Sara, 35 años, lleva 5-10 proyectos en paralelo, pierde horas en
facturación y seguimiento de cobros, quiere menos administración y más diseño.
**Narrativa (JTBD)**: "Entregar un proyecto de cliente desde el arranque hasta
cobrar la factura final."

## Columna vertebral → pasos → tareas (por release)

### Actividad 1: Cerrar el proyecto con el cliente
Pasos: revisar el brief · redactar la propuesta · negociar plazo y precio
- **MVP**: crear proyecto con nombre y cliente · guardar alcance y precio acordados
- **R2**: plantillas de propuesta reutilizables
- **Futuro**: propuesta con firma electrónica dentro de la app

### Actividad 2: Ejecutar el trabajo de diseño
Pasos: planificar entregables · diseñar · pasar revisiones con el cliente
- **MVP**: lista de entregables con estado (pendiente / en curso / hecho)
- **R2**: subir versiones y comentarios del cliente sobre cada entregable
- **Futuro**: integración con Figma para sincronizar versiones

### Actividad 3: Entregar los activos finales
Pasos: empaquetar los archivos · compartir con el cliente · confirmar aceptación
- **MVP**: enlace de entrega con los archivos finales
- **R2**: aviso automático al cliente y registro de "aceptado"
- **Futuro**: portal de cliente con historial de entregas

### Actividad 4: Facturar y cobrar
Pasos: generar la factura · enviarla · hacer seguimiento del pago
- **MVP**: crear y enviar una factura en PDF desde el proyecto
- **R2**: recordatorios automáticos de pago pendiente
- **Futuro**: cobro online integrado (tarjeta / transferencia) desde la factura

## Huecos y oportunidades
- No hay nada para el momento "cliente que no responde a la factura" → los
  recordatorios de R2 atacan justo el dolor nº1 de Sara (el cobro).
- El MVP cruza las 4 actividades: Sara ya puede llevar un proyecto de punta a
  punta (walking skeleton). Lo demás son mejoras, no bloqueantes.
```

---

## El Lado Oscuro del story mapping (antipatrones)

- **La actividad que en realidad es una feature:** "Actividad 1: usar el dashboard". Has mapeado el producto, no al usuario. Replantéalo como comportamiento: "monitorizar el progreso del proyecto".
- **El backbone hipertrofiado:** 10+ actividades en la columna vertebral. Estás mezclando actividades con pasos. Consolida a 3-5.
- **La tarea de niebla:** "Tarea 1: hacer la cosa". Si es vaga no se puede priorizar ni estimar. Sé específico: "introducir el email del cliente en el campo 'Facturar a'".
- **El mapa sin líneas de release:** todas las tareas al mismo nivel, sin MVP. Fuerza la decisión difícil: dibuja la línea y di qué NO entra en la primera entrega.
- **La columna perfecta:** haces el Release 1 completo de la actividad 1 y dejas las demás vacías. El MVP es una **rebanada horizontal** que cruza todo el viaje, no una columna acabada.
- **El mapa hecho en soledad:** el PM lo dibuja solo y lo "presenta". Sin el equipo no hay propiedad ni entendimiento compartido — y ese, no el dibujo, era el objetivo.

---

## Frameworks de referencia

- **Jeff Patton — _User Story Mapping_ (2014)** — el origen de la técnica; la fuente de la estructura backbone → pasos → tareas.
- **Walking skeleton** — la primera rebanada fina que atraviesa todo el viaje y ya funciona de punta a punta; es la forma correcta de recortar un MVP en el mapa.
- **Jobs To Be Done (JTBD)** — para anclar la narrativa en lo que el usuario quiere lograr, no en la demografía.
- **Teresa Torres — _Continuous Discovery Habits_ (2021)** — árboles de oportunidad-solución, complementarios al mapa para decidir qué oportunidades perseguir.
- **INVEST** — cuando el mapa baje a historias concretas, cada una debe ser Independiente, Negociable, Valiosa, Estimable, Pequeña y Testable (ahí entra `crear-historias-de-usuario`).

Que la IAgilidad te acompañe.
