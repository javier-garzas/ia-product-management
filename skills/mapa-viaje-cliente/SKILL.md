---
name: mapa-viaje-cliente
author: Javier Garzás — 233 Academy
description: Crea un mapa del viaje del cliente (customer journey map) de principio a fin — etapas, puntos de contacto, acciones, emociones, puntos de dolor y oportunidades — más los momentos críticos (momento ajá, momentos de la verdad, disparadores de churn) y una lista de mejoras priorizadas. Úsala cuando quieras mapear la experiencia del cliente, encontrar dónde se genera fricción, mejorar el onboarding o la retención, o visualizar el viaje del usuario de principio a fin. No la uses para decidir qué construir por releases (para eso está `mapa-de-historias-usuario`) ni para el detalle interno de procesos y sistemas (eso es un service blueprint).
---

# Mapa del Viaje del Cliente

## Propósito

Convierte lo que sabes de tus clientes en un **mapa del viaje (customer journey map)**: la experiencia completa de una persona con tu producto, desde que lo descubre hasta que lo recomienda, contando en cada etapa qué hace, qué siente, dónde sufre y qué oportunidad hay de mejorar.

El objetivo no es dibujar bonito: es **encontrar dónde se rompe la experiencia** —la fricción que frena la conversión y dispara el churn— y salir con una lista de mejoras priorizadas sobre la que actuar.

## Rol

Eres un Product Manager / diseñador de experiencia senior que ha mapeado decenas de viajes reales. No te inventas al cliente: partes de evidencia (entrevistas, datos, soporte) y, cuando no la tienes, lo dices en voz alta y lo marcas como suposición en vez de rellenar el hueco a ciegas.

## Qué es un journey map (y qué NO es)

Ten claro el eje, Rebelde IAgil, porque aquí se confunden tres cosas:

- **Mapa del viaje del cliente** — la experiencia **vista desde el cliente**: sus etapas, emociones y dolores. Es lo que hace esta skill.
- **Service blueprint** — mira **por dentro**: los procesos, sistemas y personas de tu organización que sostienen (o rompen) esa experiencia. Va un paso más allá y no es esto.
- **Mapa de historias de usuario (story map)** — sirve para decidir **qué construir y en qué orden** (releases, MVP). Es planificación de producto, no experiencia. Para eso está `mapa-de-historias-usuario`.

Un journey map bueno se centra en **una persona haciendo un viaje concreto**. Si intentas meter a todos tus clientes en un solo mapa, no sale ninguno.

---

## Aplicación

**Antes de empezar (léelo, Rebelde IAgil):**

- Si el usuario aporta material —transcripciones de entrevistas, encuestas, analítica, tickets de soporte, un mapa previo—, **léelo primero**: el viaje sale de ahí, no de tu imaginación. Si da una URL del producto, úsala para entenderlo.
- Si no hay evidencia suficiente, **no la inventes**: márcalo como `[SUPOSICIÓN: ...]` y sigue. Es mejor un mapa honesto con huecos que uno falsamente completo.

### Paso 1: Define la persona y su objetivo (JTBD)

¿Quién recorre este viaje? Una **persona concreta con su Job To Be Done** (el trabajo que quiere resolver), no un "usuario" genérico. El mismo producto lo viven de forma distinta un primer usuario y uno que renueva: elige uno.

### Paso 2: Define las etapas del viaje

Usa estas como punto de partida y **adáptalas al producto** (elimina o añade lo que haga falta):

| Etapa | Pregunta clave |
|---|---|
| Conocimiento | ¿Cómo descubre por primera vez el producto? |
| Consideración | ¿Qué evalúa? ¿Con qué alternativas lo compara? |
| Adquisición | ¿Cómo se registra o compra? |
| Onboarding | Primera experiencia real — *tiempo hasta el valor* |
| Engagement | Uso habitual — creación de hábito |
| Retención | ¿Qué le hace volver? ¿Qué podría provocar el churn? |
| Recomendación | ¿Cuándo y por qué lo recomienda a otros? |

### Paso 3: Rellena cada etapa

Para cada etapa documenta:

- **Puntos de contacto (touchpoints):** dónde interactúa (web, email, dentro de la app, soporte, redes, boca a boca).
- **Acciones del usuario:** qué hace, en verbos concretos.
- **Pensamientos y preguntas:** lo que tiene en la cabeza ("¿merece esto mi tiempo?", "¿cómo hago para...?").
- **Emociones:** cómo se siente, con un indicador claro (😄 / 🙂 / 😐 / 😟 / 😡) para poder dibujar la **curva emocional** de todo el viaje.
- **Puntos de dolor:** fricción, confusión, esperas, riesgo de abandono.
- **Oportunidades:** cómo mejorar la experiencia justo en ese punto.

### Paso 4: Marca los momentos críticos

- **Momento "ajá":** cuando el cliente experimenta por primera vez el valor central. Todo antes de ese punto debería empujar hacia él.
- **Momentos de la verdad:** puntos de decisión donde se compromete… o se va.
- **Disparadores de churn:** dónde abandonan con más frecuencia.

### Paso 5: Prioriza las mejoras

No todas las oportunidades valen igual. Ordénalas:

- **Victorias rápidas:** poco esfuerzo, mejora inmediata.
- **Apuestas de fondo:** más inversión, pero el mayor retorno en conversión o retención.
- Y sé explícito sobre **qué dolor impacta más** en el negocio (conversión / retención), no solo cuál molesta más.

### Paso 6: Entrega

- Devuelve un **documento markdown** con la persona, la tabla del viaje completa, los momentos críticos y las mejoras priorizadas.
- Para un mapa **visual**, sugiere llevar esta misma tabla a **Miro o FigJam** y dibujar encima la curva emocional.

---

## Plantilla del mapa

```markdown
# Mapa del viaje del cliente: [PRODUCTO]

**Persona**: [nombre] — [rol / contexto]
**Job To Be Done**: [el trabajo que quiere resolver]
**Escenario**: [el viaje concreto que se mapea]

## El viaje

| Etapa | Punto de contacto | Acción del usuario | Emoción | Punto de dolor | Oportunidad |
|---|---|---|---|---|---|
| Conocimiento | ... | ... | 🙂 | ... | ... |
| Consideración | ... | ... | 😐 | ... | ... |
| ... | ... | ... | ... | ... | ... |

## Momentos críticos

- **Momento ajá**: [cuándo llega el valor por primera vez]
- **Momentos de la verdad**: [puntos de decisión clave]
- **Disparadores de churn**: [dónde se cae la gente]

## Mejoras priorizadas

- **Victorias rápidas**: [...]
- **Apuestas de fondo**: [...]
```

---

## Ejemplo (academia online que vende un curso)

```markdown
# Mapa del viaje del cliente: Academia online

**Persona**: Marta, Product Manager con 3 años de experiencia que quiere aprender a aplicar IA en su trabajo.
**Job To Be Done**: "Dejar de ir por detrás con la IA y aplicarla ya en mi día a día sin perder rigor."
**Escenario**: desde que ve un vídeo del formador hasta que termina el curso y lo recomienda.

## El viaje

| Etapa | Punto de contacto | Acción del usuario | Emoción | Punto de dolor | Oportunidad |
|---|---|---|---|---|---|
| Conocimiento | Vídeo de YouTube / post en LinkedIn | Ve un contenido útil y se queda con el nombre | 🙂 | No sabe que existe un curso detrás | CTA claro y suave al final del contenido |
| Consideración | Landing del curso | Lee el temario, busca opiniones | 😐 | Duda de si el nivel es el suyo y de si tendrá tiempo | Test de nivel + testimonios de perfiles como el suyo |
| Adquisición | Checkout | Compra el curso | 🙂 | Dudas de última hora sobre la garantía | Garantía visible y FAQ en el propio checkout |
| Onboarding | Email de bienvenida + campus | Entra por primera vez al campus | 😟 | No sabe por dónde empezar; demasiadas cosas a la vez | Ruta guiada "empieza por aquí" y primera lección de 10 min |
| Engagement | Campus + comunidad | Avanza módulos, pregunta dudas | 😄 | Se atasca en un módulo denso y pierde ritmo | Recordatorios y un punto de ayuda humano en los módulos difíciles |
| Retención | Emails de progreso | Vuelve a retomar el curso | 😐 | Si abandona una semana, ya no vuelve | Aviso de "retoma donde lo dejaste" + micro-logros |
| Recomendación | Comunidad / redes | Cuenta su resultado a colegas | 😄 | No tiene un momento claro para recomendar | Pedir la recomendación justo tras un logro (certificado) |

## Momentos críticos

- **Momento ajá**: primera lección aplicada a un caso real suyo → "esto lo puedo usar mañana".
- **Momentos de la verdad**: el checkout y el primer acceso al campus (onboarding).
- **Disparadores de churn**: atascarse en un módulo denso y la primera semana sin entrar.

## Mejoras priorizadas

- **Victorias rápidas**: ruta "empieza por aquí" en el onboarding; garantía visible en el checkout.
- **Apuestas de fondo**: sistema de recordatorios y micro-logros para sostener el ritmo y frenar el churn de la primera semana.
```

---

## El Lado Oscuro de los journey maps (antipatrones)

- **El mapa de todos y de nadie:** metes a todas las personas en un solo viaje. Un mapa = una persona con un objetivo.
- **El viaje de fantasía:** te inventas emociones y dolores sin una sola entrevista ni dato. Si no hay evidencia, márcalo como `[SUPOSICIÓN]`, no lo cueles como hecho.
- **El mapa feliz:** todo son caritas sonrientes. Si no aparece fricción, no has mirado de verdad; el valor está justo en los puntos de dolor.
- **El mapa que se queda en dibujo:** precioso en Miro, cero acciones. Sin oportunidades priorizadas, no sirve para decidir nada.
- **Confundirlo con el blueprint:** empiezas a mapear procesos internos y sistemas. Eso es otra herramienta; aquí manda la mirada del cliente.
- **La emoción decorativa:** pones emojis sueltos sin curva. El valor está en ver **cómo sube y baja** el ánimo a lo largo del viaje.

---

## Frameworks de referencia

- **Customer Journey Map** — la experiencia de punta a punta vista desde el cliente.
- **Jobs To Be Done (JTBD)** — para anclar el viaje en lo que el cliente intenta lograr, no en la demografía.
- **Momento "ajá" / time-to-value** — el instante en que llega el valor; acortarlo es la palanca nº1 de activación.
- **Momentos de la verdad (MoT)** — los puntos de decisión que hacen o rompen la relación.
- **Curva emocional** — la línea de altibajos que revela dónde intervenir.
- **Service blueprint** — el complemento "por dentro" cuando quieras conectar la experiencia con tus procesos.

Que la IAgilidad te acompañe.
