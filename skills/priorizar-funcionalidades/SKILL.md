---
name: priorizar-funcionalidades
author: Javier Garzás — 233 Academy
description: Prioriza un backlog de ideas de funcionalidades en función del impacto, el esfuerzo, el riesgo y la alineación estratégica, y devuelve las 5 principales con su justificación, trade-offs y qué se despriorizó. Usa marcos probados (Opportunity Score de Dan Olsen, ICE y RICE). Úsala cuando tengas un backlog o una lista de ideas y haya que decidir en qué trabajar, tomar decisiones de alcance o clasificar iniciativas. No la uses para validar en profundidad UNA idea (para eso está `validar-idea-antes-de-construir`) ni para ordenar el trabajo dentro de una sola iniciativa por releases (para eso está `mapa-de-historias-usuario`).
---

# Priorizar Funcionalidades

## Propósito

Convierte un backlog de ideas —esa lista donde "todo es importante"— en una **clasificación defendible**: las 5 funcionalidades que hay que abordar primero, con el porqué, los trade-offs y, sobre todo, **qué se deja fuera y por qué**.

Priorizar no es ordenar por entusiasmo: es hacer explícito el criterio con el que decides, para que la decisión sea discutible con datos y no una cuestión de quién grita más fuerte en la reunión.

## Rol

Eres un Product Manager senior que sabe que **priorizar es el trabajo**, no un trámite. Tu instinto no es "¿qué construimos?" sino "¿qué problema del cliente merece más nuestra capacidad limitada, y qué renunciamos al elegirlo?". Cuando faltan datos para puntuar algo, lo dices y lo marcas como `[SUPOSICIÓN]` en vez de fabricar una cifra que aparenta rigor.

## El fundamento (narrativa)

En **233 Academy**, Javier Garzás lo repite, Rebelde IAgil: *priorizar no va de decir "sí" a lo bueno, va de decir "no" a lo bueno para poder decir "sí" a lo mejor.* Tres ideas sostienen un buen orden de prioridad:

- **Prioriza problemas, no soluciones (Dan Olsen).** El _Opportunity Score_ mide dónde hay hueco real: `Importancia × (1 − Satisfacción)`. Alta importancia + baja satisfacción = la mejor oportunidad. Enamórate del problema del cliente, no de tu feature.
- **El coste de retraso manda (Reinertsen / WSJF).** Lo caro no suele ser construir, es **tardar** en entregar algo valioso. Priorizar por valor entre esfuerzo (tipo ICE/RICE/WSJF) es una forma de perseguir el coste de retraso, no el capricho.
- **La capacidad es finita.** Cada "sí" gasta un hueco que ya no tienes para otra cosa. Por eso una priorización sin una lista explícita de **despriorizados** está incompleta.

## Marcos que usa esta skill

- **Opportunity Score (Dan Olsen, _The Lean Product Playbook_)** — para evaluar **problemas del cliente**: `Importancia × (1 − Satisfacción)`, normalizado 0–1. Úsalo cuando tengas datos de clientes.
- **ICE** — para puntuar iniciativas rápido: `Impacto × Confianza × Facilidad (Ease)`. Simple y suficiente en la mayoría de casos.
- **RICE** — añade el **Alcance (Reach)** como factor aparte (`Reach × Impact × Confidence / Effort`); útil en equipos y carteras más grandes.

Regla práctica: elige **un** marco y aplícalo a todo el backlog por igual. Mezclar marcos entre ideas rompe la comparación.

## Qué es (y qué NO es)

- **NO es** una votación de opiniones ni un "lo que pida el que más manda".
- **NO es** ordenar por esfuerzo (empezar por lo fácil) ni por novedad (lo más molón).
- **NO es** planificación dentro de una iniciativa (eso es `mapa-de-historias-usuario`).
- **SÍ es** comparar ideas entre sí con un criterio homogéneo de impacto/esfuerzo/riesgo/estrategia y quedarte con las que más mueven la aguja.

### Cuándo usarlo / cuándo no

Úsalo cuando tengas varias ideas compitiendo por la misma capacidad, cuando haya que recortar alcance, o cuando el equipo no se pone de acuerdo en qué va primero.

No lo uses si solo tienes una idea (valídala con `validar-idea-antes-de-construir`), si la decisión ya está tomada, o si te falta cualquier señal de valor y estás puntuando puro humo (primero consigue algo de evidencia).

---

## Aplicación

### Paso 1: Fija el objetivo y la métrica

Confirma el **objetivo de producto** y la **métrica de éxito** contra la que vas a medir el impacto. Sin una métrica clara, "impacto" es una opinión. Si no la hay, defínela o márcala como `[NECESITA ACLARACIÓN]`.

### Paso 2: Evalúa cada idea contra cuatro ejes

- **Impacto:** ¿cuánto mueve la métrica? Usa el _Opportunity Score_ si tienes datos de clientes.
- **Esfuerzo:** desarrollo + diseño + coordinación. Sé honesto con lo que no se ve.
- **Riesgo / incertidumbre:** ¿cuántos supuestos sin validar? (Mucho riesgo → antes que construir, un experimento: ver `validar-idea-antes-de-construir`.)
- **Alineación estratégica:** ¿empuja la visión y los objetivos de este trimestre, o es un desvío?

### Paso 3: Puntúa con un marco homogéneo

Aplica ICE (o RICE / Opportunity Score) a **todas** las ideas por igual y calcula la puntuación. Anota de dónde sale cada número: una puntuación sin trazabilidad no es defendible.

### Paso 4: Devuelve el Top 5

Para cada una de las 5 principales: **ranking (1-5)**, **justificación breve**, **trade-offs** considerados y —clave— **qué se despriorizó y por qué**. Preséntalo en tabla si ayuda.

### Paso 5: Revisa el sesgo

Antes de cerrar: ¿estás priorizando lo importante o lo fácil? ¿lo estratégico o lo ruidoso? ¿hay alguna idea alta en impacto pero con riesgo tan alto que primero pide un experimento, no un desarrollo?

---

## Plantilla

```markdown
# Priorización: [PRODUCTO / TRIMESTRE]
**Objetivo**: [objetivo de producto]  ·  **Métrica de éxito**: [métrica]
**Marco usado**: ICE (Impacto × Confianza × Facilidad)

| # | Idea | Impacto (1-10) | Confianza (1-10) | Facilidad (1-10) | ICE | Notas |
|---|------|:---:|:---:|:---:|:---:|-------|
| | ... | | | | | |

## Top 5 recomendado
1. **[Idea]** — [justificación]. Trade-off: [...].
...

## Despriorizado (y por qué)
- **[Idea]** — [motivo: bajo impacto / alto riesgo → experimento primero / fuera de estrategia].
```

---

## Ejemplo (completo) — Backlog de una academia online

```markdown
# Priorización: Academia online — Q3
**Objetivo**: subir la finalización de cursos.  **Métrica**: % de alumnos que terminan.
**Marco**: ICE (Impacto × Confianza × Facilidad), cada eje 1-10.

| # | Idea | Impacto | Confianza | Facilidad | ICE | Notas |
|---|------|:---:|:---:|:---:|:---:|-------|
| 1 | Ruta "empieza por aquí" en el onboarding | 8 | 8 | 9 | 576 | Ataca el abandono de la 1ª semana |
| 2 | Recordatorios "retoma donde lo dejaste" | 9 | 7 | 8 | 504 | Alto impacto en finalización |
| 3 | Certificado descargable al terminar | 6 | 8 | 8 | 384 | Motivación + recomendación |
| 4 | Comunidad/foro por curso | 7 | 4 | 3 | 84  | Impacto dudoso, mucho esfuerzo |
| 5 | Recomendador de cursos con IA | 6 | 3 | 3 | 54  | Riesgo alto: incógnitas sin validar |
| 6 | Rediseño visual del campus | 4 | 5 | 4 | 80  | Bonito, no mueve la métrica |

## Top 5 recomendado
1. **Ruta de onboarding** (ICE 576) — máximo impacto en el punto de mayor churn, y barata.
2. **Recordatorios de retomar** (504) — el mayor efecto directo en finalización.
3. **Certificado al terminar** (384) — empuja finalización y genera recomendación.
4. **Comunidad por curso** (84) — entra por estrategia de retención a largo plazo, aunque cara.
   Trade-off: se acepta su bajo ICE por su encaje con la visión de comunidad.
5. **Recomendador con IA** (54) — NO se construye aún: se convierte en un experimento
   (`validar-idea-antes-de-construir`) por su riesgo. Sube si se valida.

## Despriorizado (y por qué)
- **Rediseño visual del campus** — no mueve la métrica de finalización; es estética, no palanca.
```

---

## El Lado Oscuro (antipatrones)

- **Priorizar por esfuerzo:** empiezas por lo fácil para "ir marcando cosas". Vacías el backlog sin mover la métrica.
- **La cifra que aparenta:** pones ICE de 8·9·7 sacados del aire. Un número inventado es más peligroso que una corazonada honesta, porque parece objetivo. Traza de dónde sale cada puntuación.
- **Enamorarse de la solución:** priorizas tu feature favorita en vez del problema del cliente. Vuelve al _Opportunity Score_: ¿dónde hay importancia alta y satisfacción baja?
- **La priorización sin "no":** todo acaba en el Top. Si no hay lista de despriorizados, no has priorizado, has ordenado.
- **Mezclar marcos:** puntúas unas ideas con ICE y otras con RICE. Ya no son comparables. Un marco para todo el backlog.
- **Ignorar el riesgo:** metes en desarrollo una idea de impacto alto pero llena de incógnitas. Eso no es una prioridad de build, es una prioridad de **experimento**.

---

## Frameworks de referencia

- **Dan Olsen — _The Lean Product Playbook_ (2015)** — Opportunity Score; prioriza problemas (oportunidades) sobre soluciones.
- **ICE / RICE** — puntuación rápida de iniciativas (RICE popularizado por Intercom); valor entre esfuerzo, con o sin Reach.
- **Donald Reinertsen — coste de retraso y WSJF** — priorizar por _Weighted Shortest Job First_ persigue el valor que se pierde por esperar, no el capricho.
- **Kano** — para distinguir lo básico, lo lineal y lo que deleita, cuando quieras matizar el "impacto".
- **MoSCoW** — Must / Should / Could / Won't, útil como corte grueso de alcance antes de puntuar fino.

Que la IAgilidad te acompañe.
