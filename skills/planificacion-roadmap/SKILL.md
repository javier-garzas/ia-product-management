---
name: planificacion-roadmap
author: Javier Garzás — 233 Academy
description: Planifica un roadmap estratégico orientado a resultados, orquestando la recogida de entradas, la definición de épicas como hipótesis, la priorización, la secuenciación en releases y la alineación de stakeholders. Úsala cuando conviertas la estrategia en un plan de releases que los equipos puedan ejecutar y que dirección apruebe, evitando el roadmap "fábrica de funcionalidades". No la uses para la planificación táctica de un sprint (usa el backlog) ni cuando la estrategia aún no está clara (defínela antes).
---

# Planificación de Roadmap

> Workflow de 5 fases · orientación temporal: ~1-2 semanas (vía rápida: 1 semana). Puede ejecutarse como conversación guiada.

## Propósito

Convierte una maraña de peticiones inconexas en un **roadmap cohesionado y orientado a resultados**: uno que muestra *qué* construyes, *por qué* importa y *cómo* conecta con los resultados de negocio. Su enemigo declarado es el roadmap "fábrica de funcionalidades" — esa lista de features sin narrativa ni cliente detrás.

Esto **no es un diagrama de Gantt**: es una herramienta de comunicación estratégica y de alineación, no un calendario de compromisos.

## Rol

Eres un líder de producto que sabe que un roadmap se juega su credibilidad en dos frentes: que **sobreviva a la revisión de dirección** y que **el equipo lo pueda ejecutar**. Por eso no vendes una lista de features: cuentas una historia de resultados, haces explícito el porqué de cada prioridad y —lo más incómodo y más valioso— dices en voz alta **qué NO se va a hacer**.

## El fundamento (narrativa)

En **233 Academy**, Javier Garzás lo avisa, Rebelde IAgil: *un roadmap de funcionalidades es una lista de deseos con fechas; un roadmap de resultados es una estrategia con narrativa.* Tres ideas lo sostienen:

- **Resultados sobre entregables (Melissa Perri, _Escaping the Build Trap_).** La trampa de construir es medir el éxito por features entregadas en lugar de por el problema resuelto. El roadmap debe hablar de resultados de cliente/negocio, no de outputs.
- **Contra la fábrica de funcionalidades (John Cutler).** Un equipo que produce features sin conectar con impacto es una cadena de montaje ciega. El roadmap es la herramienta que reconecta el trabajo con el porqué.
- **Now/Next/Later y la incertidumbre honesta.** El futuro se conoce peor cuanto más lejos: comprometer fechas trimestre a trimestre finge una certeza que no existe. Un buen roadmap decrece en confianza según se aleja.

## Qué es (y qué NO es)

- **NO es un compromiso:** un roadmap es un plan estratégico, no un contrato de fechas.
- **NO es una lista de funcionalidades:** enmarca problemas y resultados, no solo soluciones.
- **NO es waterfall:** evoluciona cada trimestre según lo que aprendes.
- **SÍ es** la traducción de la estrategia a un plan de releases secuenciado, con narrativa y foco en resultados.

### Formatos de roadmap

- **Now / Next / Later** — Ahora (comprometido) · Siguiente (alta confianza) · Después (exploración). Ideal para equipos ágiles e incertidumbre.
- **Por temas** — organizado por temas estratégicos ("Retención", "Expansión enterprise"). Ideal para comunicar a dirección.
- **Por línea temporal (trimestres)** — Q1/Q2/Q3. Ideal para planificar recursos.
- **Por funcionalidades (ANTIPATRÓN)** — lista features sin contexto ni problema de cliente. No lo uses.

### Dónde encaja respecto a sus skills hermanas

Este workflow **orquesta** varias skills del repo: en la Fase 2 usa el formato de hipótesis de `validar-idea-antes-de-construir`; en la Fase 3, el de `priorizar-funcionalidades`. Y aguas abajo, cada épica del roadmap se diseña con `mapa-viaje-cliente`, `mapa-de-historias-usuario`, `division-de-historias-usuario`, `crear-historias-de-usuario` y `crear-spec-sdd`. Si el roadmap incluye features de IA, pásalas antes por `cuando-usar-ia-metodo-ed2a`.

### Cuándo usarlo / cuándo no

Úsalo en ciclos de planificación trimestral/anual, tras una sesión de estrategia, al incorporar stakeholders, o al reconvertir un roadmap de funcionalidades en uno de resultados.

No lo uses para planificar un sprint (eso es el backlog), cuando la estrategia no está clara (defínela primero), o cuando los stakeholders esperan compromisos de fecha (gestiona antes esa expectativa).

### Modo de facilitación

Puede correrse como conversación guiada: avisa al inicio, ofrece un modo de entrada (Guiado / Volcado de contexto / Mejor estimación), una pregunta por turno en lenguaje sencillo, muestra progreso (p. ej. *Contexto Px/8*, *Puntuación Px/5*), gestiona pausa/reanudación y ofrece recomendaciones numeradas en los puntos de decisión.

---

## Aplicación — 5 fases

### Fase 1 · Reunir entradas

Recopila las cuatro fuentes que alimentan el roadmap:
- **Objetivos de negocio (OKRs):** las 3-5 prioridades de empresa y las métricas a mover. → *3-5 resultados de negocio.*
- **Problemas de cliente (discovery):** los 3-5 dolores validados, por alcance e intensidad. → *3-5 problemas validados.*
- **Restricciones y oportunidades técnicas:** bloqueantes, inversiones habilitadoras, deuda. → *lista de inversiones técnicas.*
- **Peticiones de stakeholders:** ventas, marketing, CS, dirección (sin comprometer aún). → *lista de peticiones.*

### Fase 2 · Definir iniciativas (épicas)

Convierte las entradas en épicas con hipótesis, métrica de éxito y esfuerzo:
- **Hipótesis de épica** (formato de `validar-idea-antes-de-construir`): *"Creemos que [construir X] para [persona] logrará [resultado] porque [supuesto]."*
- **Esfuerzo por tallas de camiseta:** S (1-2 sem) · M (3-4 sem) · L (2-3 meses) · XL (3+ meses), con ingeniería.
- **Mapea cada épica a su resultado de negocio** (retención, adquisición, engagement…).

> Ejemplo: *"Onboarding guiado — Creemos que un checklist paso a paso para usuarios no técnicos subirá la activación del 40% al 60% porque hoy abandonan por falta de guía. Métrica: % que completa la 1ª acción en 24h. Esfuerzo: M."*

### Fase 3 · Priorizar iniciativas

Ordena las épicas con un marco homogéneo (ver `priorizar-funcionalidades`): RICE, ICE o Valor/Esfuerzo. Puntúa todas por igual, y **ajusta por encaje estratégico**: una apuesta puede subir aunque puntúe menos si es crítica para la estrategia (ej.: SSO enterprise puntúa bajo en alcance pero desbloquea la expansión enterprise). → *backlog ordenado + Top 10.*

### Fase 4 · Secuenciar el roadmap

- **Mapea dependencias:** ¿la épica B necesita la A? ¿hay bloqueantes técnicos? → *grafo de dependencias.*
- **Secuencia por trimestre / Now-Next-Later:** Ahora (top sin dependencias), Siguiente (alta confianza), Después (menor confianza).
- **Valida con ingeniería:** ¿es realista la capacidad? ¿bloqueantes ocultos? → *secuencia validada.*

```
Q1 (Ahora · comprometido)     Q2 (Siguiente · alta confianza)   Q3+ (Después · exploración)
├─ Onboarding guiado          ├─ Informes avanzados             ├─ App móvil (dep. API)
├─ SSO enterprise             │   (dep. pipeline de datos, Q1)  ├─ Recomendaciones con IA
└─ Flujos móviles             └─ Integración con Slack          └─ Soporte multi-idioma
```

### Fase 5 · Comunicar el roadmap

- **Prepara la presentación (30-45 min):** contexto estratégico → visión Q1/Q2/Q3 → profundización por trimestre (épica, hipótesis, métrica) → **lo que NO está y por qué** → dependencias y riesgos.
- **Preséntalo** a dirección, producto, ingeniería, ventas, marketing y CS. Foco en **narrativa** ("por qué X antes que Y"), en **resultados** ("cada épica impulsa [resultado]") y en **flexibilidad** ("plan, no contrato").
- **Recoge feedback, refina y publica** (interno: Notion/Confluence; externo opcional: formato Now/Next/Later).

---

## Ejemplo (roadmap resultante · formato Now/Next/Later)

```markdown
# Roadmap de producto — SaaS · 2026

AHORA (Q actual · comprometido)
- Onboarding guiado        → Retención   · activación 40%→60%
- SSO enterprise           → Adquisición · deals enterprise 2→5/trim
- Flujos optimizados móvil  → Engagement  · DAU móvil 5%→20%

SIGUIENTE (alta confianza)
- Informes avanzados       → Expansión (depende del pipeline de datos)
- Integración con Slack    → Engagement
- Rediseño de precios      → Adquisición

DESPUÉS (exploración · menor confianza)
- App móvil nativa (depende del rediseño de API)
- Recomendaciones con IA (pasar antes por ED2A + validar como experimento)
- Soporte multi-idioma

FUERA DEL ROADMAP (y por qué)
- Rediseño visual del campus → no mueve ninguna métrica de resultado; es estética.
```

---

## El Lado Oscuro (antipatrones)

- **El roadmap fábrica de funcionalidades:** lista "modo oscuro, SSO, filtros" sin resultados. Nadie entiende el porqué. Enmárcalo como hipótesis con métricas.
- **Priorizar por HiPPO** (_Highest Paid Person's Opinion_): manda quien más cobra, no los datos. Usa un marco de priorización transparente y defiéndelo.
- **El roadmap-contrato:** lo tratas como promesa de fechas y no puedes pivotar cuando aprendes. Comunícalo como "plan sujeto a aprendizaje".
- **Secuenciar sin dependencias:** una épica de Q2 se bloquea porque su dependencia de Q1 no terminó. Mapea dependencias en la Fase 4 y valida con ingeniería.
- **El roadmap en solitario:** el PM lo cocina solo y presenta un plan cerrado. Sin las entradas de todos (Fase 1) y un borrador para feedback (Fase 5), no hay buy-in.
- **El roadmap sin "fuera de alcance":** si no dices qué NO se hace, cada stakeholder asume que lo suyo entra. La diapositiva de lo descartado es la más importante.

---

## Frameworks de referencia

- **Melissa Perri — _Escaping the Build Trap_ (2018)** — resultados sobre entregables; la raíz de por qué el roadmap habla de outcomes.
- **John Cutler — _"Feature Factory"_** — el antipatrón del equipo que produce features desconectadas del impacto.
- **McCarthy, Lombardo, Ryan y Connors — _Product Roadmaps Relaunched_ (2017)** — roadmaps orientados a resultados y el marco **Now / Next / Later**.
- **RICE / ICE** — la priorización que alimenta la Fase 3 (ver `priorizar-funcionalidades`).
- **OKR** — para anclar las iniciativas del roadmap en resultados de negocio medibles.

Que la IAgilidad te acompañe.
