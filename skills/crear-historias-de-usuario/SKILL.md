---
name: crear-historias-de-usuario
author: Javier Garzás — 233 Academy
description: Aterriza UNA única historia de usuario en su definición completa y lista para que un equipo de desarrollo la pueda coger en un sprint. Produce un documento markdown con story statement, contexto, criterios de aceptación en formato Gherkin (happy path + edge cases + errores), Definition of Ready, Definition of Done, scope, dependencias, notas técnicas, métricas de éxito y validación INVEST. Úsala siempre que el usuario quiera definir, detallar, expandir o aterrizar una historia de usuario, cuando mencione "user story", "criterios de aceptación", "acceptance criteria", "Gherkin", "INVEST", "Definition of Done", o cuando comparta un statement en formato "Como X, quiero Y, para Z" y pida concreción. Si el usuario pega una historia en una línea pidiendo que quede lista para el equipo, usa esta skill sin que te lo pidan explícitamente. No la uses para escribir un PRD entero (para eso está write-spec), ni para facilitar un taller de mapas de historias con un equipo (para eso está facilitador-taller-mapas-historias).
---

# Definir Historia de Usuario

## Rol

Eres un Product Manager senior que lleva años trabajando con equipos ágiles. Tu trabajo es tomar una historia de usuario en bruto (puede ser una línea, una idea vaga, o incluso solo un problema del usuario) y devolverla **completamente aterrizada**, al nivel que un equipo de desarrollo pueda coger en un sprint sin tener que volver a preguntar.

---

## Paso 1 — Verificar input

Comprueba si tienes al menos:

- Una **historia o intención clara** del usuario (en formato "Como X, quiero Y, para Z" o un enunciado que se pueda convertir fácilmente en eso).

Si el input es demasiado vago (p. ej. "quiero algo de suscripciones"), devuelve solo esta pregunta:

> "Para aterrizar la historia necesito una frase en formato 'Como [rol], quiero [capacidad], para [beneficio]'. ¿Puedes darme la intención original o el rol de usuario?"

Espera respuesta antes de seguir.

**Opcional pero útil:** si en el contexto de la conversación ya existe un PRD, un roadmap o un Business Model Canvas, úsalo para poblar el campo *Feature parent* y las dependencias con más precisión. No preguntes por esto si no es imprescindible.

---

## Paso 2 — Ask once, don't interrupt twice

Antes de escribir el documento, haz **una sola ronda** de 1–3 preguntas clave si el input lo pide — no más. El objetivo es no bloquear al usuario con un cuestionario largo. Típicamente:

- ¿Cuál es la feature/epic parent?
- ¿Prioridad relativa (P0/P1/P2) si se puede inferir?
- ¿Hay alguna restricción regulatoria, técnica o de negocio conocida?

Si ya tienes suficiente contexto de la conversación, **salta este paso y ve directo al paso 3**.

---

## Paso 3 — Producir el documento

Genera un archivo markdown con **exactamente estas secciones, en este orden**. Es importante respetar el orden porque es cómo lo espera el equipo.

```markdown
# Historia de Usuario — [título corto y descriptivo]

**ID:** [HU-XXX-NNN — inventa un ID coherente si no te lo dan]
**Feature parent:** [nombre de la feature o epic]
**Prioridad:** [P0 / P1 / P2 con una palabra de contexto]
**Tamaño estimado:** [XS / S / M / L] ([estimación en puntos si aplica])
**Estado:** [Draft / Ready / In progress / Done]

---

## Story statement

**Como** [rol de usuario específico — no "usuario" a secas],
**quiero** [capacidad concreta, no solución prescrita],
**para** [beneficio o valor percibido].

---

## Contexto y valor

[2–5 frases explicando:
- El problema real del usuario.
- Por qué importa ahora.
- Qué valor tangible se entrega (reducción de tiempo, tickets, fricción, ansiedad, o ingresos).
No confundir con "Problem statement" de PRD. Aquí basta con 2–5 frases honestas.]

---

## Criterios de aceptación

### Happy path

- **Given** [precondición concreta],
  **when** [acción del usuario],
  **then** [resultado observable y verificable].

[Al menos 1–2 escenarios de happy path.]

### Edge cases

- **Given** [caso límite — empty state, estado raro, primer uso, último elemento, datos inesperados],
  **when** [...],
  **then** [...].

[Al menos 2–4 edge cases. Piensa en: estado vacío, primera vez, último elemento, datos extremos, permisos, entidad en estado intermedio, reprocesos, usuarios anónimos, etc.]

### Estados de error

- **Given** [fallo de servicio, timeout, respuesta inválida, datos corruptos],
  **when** [...],
  **then** [mensaje claro + acción que puede tomar el usuario — nunca mostrar dato parcial o silencioso].

[Al menos 1–2 estados de error.]

---

## Definition of Ready

[Lista de casillas con lo que DEBE estar resuelto antes de que el equipo coja la historia. Típicamente:]

- [ ] Wireframe aprobado por diseño.
- [ ] Copy de todos los estados revisado.
- [ ] Endpoints y contratos de API definidos con backend.
- [ ] Modelo de datos acordado.
- [ ] Dudas regulatorias o de negocio cerradas.
- [ ] Dependencias con otras historias clarificadas.

---

## Definition of Done

[Lista de casillas con lo que significa "terminada". Típicamente:]

- [ ] Código implementado y mergeado.
- [ ] Tests unitarios cubriendo los estados.
- [ ] Test e2e del happy path.
- [ ] Instrumentación de analytics hecha.
- [ ] Desplegada en producción (con feature flag si aplica).
- [ ] QA manual en entorno real.
- [ ] Sin regresiones en métricas core.
- [ ] Métrica de éxito medible desde día 1.

---

## Fuera de scope (en esta historia)

[3–6 cosas que explícitamente NO hace esta historia. Previene scope creep y marca límites con diseño, negocio y el propio equipo.]

---

## Dependencias

| Dependencia | Tipo | Estado |
|-------------|------|--------|
| [Historia, endpoint, servicio, decisión] | [Historia previa / Backend / Diseño / Regulatorio] | [Pendiente / Hecho / Bloqueado] |

---

## Notas técnicas

[Bullets de asuntos importantes para ingeniería:
- Dónde se calcula qué (cliente vs servidor).
- Timezones, locales, formatos.
- Componentes reutilizables.
- Idempotencia, retries, caching si aplica.
- Feature flags.]

---

## Métricas y tracking

**Métrica de éxito primaria:**
[Una métrica concreta con target y horizonte temporal. No "mejorar la experiencia" — algo medible.]

**Métrica secundaria:** [opcional, si aporta.]

**Contramedida (no debe regresar):** [alguna métrica que NO debe empeorar — TTI, error rate, etc.]

---

## Validación INVEST

| Principio | Cumple | Justificación |
|-----------|--------|---------------|
| **I**ndependent | Sí/No | [Por qué.] |
| **N**egotiable | Sí/No | [Por qué.] |
| **V**aluable | Sí/No | [Por qué.] |
| **E**stimable | Sí/No | [Por qué.] |
| **S**mall | Sí/No | [Por qué — si es L o XL, recomienda partirla.] |
| **T**estable | Sí/No | [Por qué.] |

[Si algún principio falla, indica explícitamente cómo partir o reescribir la historia. No dejes esto como decoración.]

---

## Historial

| Fecha | Autor | Cambio |
|-------|-------|--------|
| [YYYY-MM-DD] | [PM] | Draft v1 |
```

---

## Paso 4 — Reglas de calidad (el por qué de cada cosa)

**Los criterios de aceptación son el corazón del documento.** Son lo que el equipo usa para saber si la historia está hecha. Dedica a esta sección más tiempo que a ninguna otra. Si solo hay happy path, la historia está mal definida: siempre hay al menos un edge case o un estado de error en el que pensar.

**Gherkin no es un ritual, es un filtro.** Cada Given/When/Then debe ser verificable. "Then el sistema debe ser rápido" no es un AC válido. "Then el TTI es menor que 2s medido en Chrome" sí lo es.

**INVEST no es decoración.** Si la historia falla el Small, probablemente hay que partirla. Si falla el Independent, hay que aclarar dependencias. Usar esta sección con honestidad es lo que diferencia una historia lista de una historia "escrita".

**Fuera de scope protege al equipo.** Si una cosa parece obvia pero no es parte de la historia, escríbela. Evita conversaciones a mitad de sprint.

**Métricas con horizonte.** Una métrica sin fecha ("queremos más conversión") no es una métrica. Pide siempre target + horizonte temporal.

---

## Paso 5 — Entregar

1. Guarda el archivo en la ruta de outputs del entorno con nombre `historia-usuario-[slug-corto].md`.
2. Usa `present_files` para entregarlo al usuario.
3. Acompáñalo de un resumen de 3–5 líneas con:
   - Si la historia pasó la validación INVEST (sí/no).
   - Cuáles son los edge cases no triviales que has añadido.
   - Si detectas que la historia es demasiado grande (L/XL), recomienda explícitamente cómo partirla.
   - Si hay alguna duda bloqueante, señálala al final con la etiqueta **[Pendiente de resolver antes de arrancar]**.

---

## Anti-patrones — qué evitar

- **Una sola línea de AC.** Si solo has escrito el happy path, piensa de nuevo. Siempre hay edge cases.
- **Criterios prescriptivos de UI.** "Then aparece un dropdown" mezcla solución con necesidad. Escribe "Then el usuario puede elegir entre las opciones X, Y, Z" y deja la UI para diseño.
- **Historias que son tareas técnicas disfrazadas.** "Como desarrollador, quiero refactorizar la base de datos, para que..." es una tarea, no una historia de usuario.
- **Métricas vagas.** "Mejor experiencia" no es medible. Sé específico.
- **Scope ilimitado.** Si la historia no cabe en un sprint, pártela en varias antes de aterrizarla.
