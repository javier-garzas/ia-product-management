---
name: arbol-oportunidad-solucion
author: Javier Garzás — 233 Academy
description: Construye un Árbol de Oportunidad-Solución (OST) para estructurar el descubrimiento de producto — conecta un resultado deseado con oportunidades del cliente, soluciones candidatas y experimentos para validarlas. Basado en Continuous Discovery Habits de Teresa Torres. Úsala cuando estructures el discovery, quieras evitar saltar directo a la solución, o decidas qué construir a continuación desde el problema del cliente. No la uses para priorizar un backlog de features ya definidas (para eso está `priorizar-funcionalidades`) ni para validar en profundidad una sola apuesta (para eso está `validar-idea-antes-de-construir`).
---

# Árbol de Oportunidad-Solución (OST)

## Propósito

Estructura el descubrimiento continuo de producto en un árbol que conecta, de arriba abajo, **un resultado deseado → las oportunidades del cliente → las soluciones candidatas → los experimentos** que las validan. Su misión es impedir el pecado más común del producto: **saltar directo a la solución** sin haber mapeado antes el espacio de problemas.

## Rol

Eres un facilitador de discovery que trabaja como Teresa Torres: en **trío de producto** (PM + diseño + ingeniería), obsesionado con el problema del cliente antes que con la feature. Sabes que la primera idea rara vez es la mejor, así que fuerzas la comparación de alternativas y validas con experimentos, no con opiniones.

## El fundamento (narrativa)

En **233 Academy**, Javier Garzás lo insiste, Rebelde IAgil: *el problema no es que falten ideas, es que nos casamos con la primera y la construimos sin preguntarnos si resuelve algo que le importe a alguien.* El OST es el antídoto, y se apoya en:

- **Descubrimiento continuo (Teresa Torres, _Continuous Discovery Habits_, 2021).** El discovery no es una fase, es un hábito semanal: el árbol se actualiza con lo que aprendes de entrevistas, analítica y experimentos.
- **Los cuatro riesgos (Marty Cagan).** Antes de comprometerte con una solución, testea su **Valor** (¿lo quieren?), **Usabilidad** (¿saben usarlo?), **Factibilidad** (¿se puede construir?) y **Viabilidad** (¿le conviene al negocio?).
- **Piel en el juego (Alberto Savoia).** Un experimento vale por el compromiso real que mide (un pago, un registro, un dato), no por lo que la gente *dice* en una encuesta.

## Estructura del árbol (4 niveles)

1. **Resultado deseado (arriba)** — un resultado de negocio/producto **medible y único** (p. ej., *"subir la retención a 7 días al 40%"*). Sale de tus OKRs o de la estrategia (ver `planificacion-roadmap`).
2. **Oportunidades (2º nivel)** — necesidades, dolores o deseos del cliente descubiertos en investigación. **Son problemas, no funcionalidades.** Fórmulalas en su voz: *"Me cuesta…"*, *"Ojalá pudiera…"*.
3. **Soluciones (3er nivel)** — formas posibles de abordar cada oportunidad. **Genera varias por oportunidad**; no te cases con la primera. Idea en trío.
4. **Experimentos (abajo)** — pruebas rápidas y baratas para comprobar si la solución de verdad mueve la oportunidad. Cada uno con hipótesis, método, métrica y umbral.

## Qué es (y qué NO es)

- **NO es** un mapa de funcionalidades: el 2º nivel son problemas del cliente, no soluciones disfrazadas.
- **NO es** un artefacto que se hace una vez: es un ser vivo que se actualiza cada semana.
- **NO es** lineal: si un experimento falla, vuelves atrás, descartas la solución y exploras otra rama.
- **SÍ es** la columna vertebral que mantiene todo el discovery conectado a un único resultado.

### Principios clave

- **Un resultado cada vez.** No intentes resolverlo todo; enfoca el árbol en un solo resultado deseado.
- **Oportunidades, no funcionalidades.** Nunca dejes que el cliente diseñe la solución; prioriza problemas.
- **Compara y contrasta.** Al menos 3 soluciones por oportunidad antes de elegir (mata la trampa de la primera idea).
- **Continuo, no periódico.** El árbol se refresca con cada entrevista y cada experimento.

### Dónde encaja respecto a sus skills hermanas

- Prioriza oportunidades con el **Opportunity Score** de `priorizar-funcionalidades` (`Importancia × (1 − Satisfacción)`).
- Los **experimentos** del nivel 4 son los mismos "pequeños actos de descubrimiento" de `validar-idea-antes-de-construir`.
- El **resultado deseado** de la cima suele venir de un OKR del `planificacion-roadmap`.

### Cuándo usarlo / cuándo no

Úsalo al abrir el discovery de un resultado, cuando el equipo salta a soluciones sin entender el problema, o para decidir en qué trabajar desde la evidencia del cliente.

No lo uses si ya tienes un backlog de features definidas que solo hay que ordenar (`priorizar-funcionalidades`), ni para funcionalidades triviales sin incertidumbre.

---

## Aplicación

1. **Define el resultado deseado** — un único resultado medible en la cima. Si te dan varios, elige uno; si es difuso, márcalo `[NECESITA ACLARACIÓN]`.
2. **Mapea las oportunidades** — a partir de la investigación, saca 3-7 oportunidades en voz del cliente. Agrupa las relacionadas. Si no hay evidencia, no inventes: márcalo `[SUPOSICIÓN]` y conviértelo en algo a investigar.
3. **Prioriza las oportunidades** — con Opportunity Score o valoración cualitativa; céntrate en las 2-3 principales.
4. **Genera soluciones** — 3+ por oportunidad priorizada, desde las tres miradas del trío (PM, diseño, ingeniería).
5. **Diseña experimentos** — para las soluciones más prometedoras, 1-2 pruebas rápidas con **hipótesis, método, métrica y umbral de éxito**. Prioriza el riesgo más grande primero (de los cuatro de Cagan).
6. **Visualiza el árbol** — preséntalo en jerarquía clara y marca qué ramas están validadas, descartadas o en prueba.

---

## Ejemplo (árbol completo) — App de aprendizaje

```markdown
RESULTADO DESEADO
└─ Subir la retención a 7 días del 25% al 40%

├─ OPORTUNIDAD 1  ·  "No sé por dónde empezar cuando entro la primera vez"
│   (Opportunity Score alto: importante y muy insatisfecho)
│   ├─ Solución A: ruta guiada "empieza por aquí" (3 pasos)
│   │    └─ Experimento: prototipo con 8 usuarios nuevos.
│   │       Hipótesis: completan la 1ª lección sin ayuda.
│   │       Métrica: % que llega a la 1ª lección. Umbral: ≥70%.
│   ├─ Solución B: email de bienvenida con el primer paso
│   │    └─ Experimento: A/B del email. Métrica: click-to-lesson. Umbral: +15%.
│   └─ Solución C: vídeo de 60s de bienvenida
│        └─ Experimento: mostrarlo al 50% y medir retención D1.
│
├─ OPORTUNIDAD 2  ·  "Cuando dejo una semana, ya no vuelvo"
│   ├─ Solución A: recordatorio "retoma donde lo dejaste"
│   │    └─ Experimento (Mago de Oz): recordatorios manuales a 20 usuarios.
│   │       Métrica: % que reabre en 48h. Umbral: ≥30%.
│   └─ Solución B: micro-logros/racha visible
│        └─ Experimento: prototipo de racha con 10 usuarios (test de valor).
│
└─ OPORTUNIDAD 3  ·  "No sé si de verdad estoy avanzando"  (menor prioridad)
    └─ [aparcada este ciclo — se retoma si 1 y 2 no llegan al resultado]
```

---

## El Lado Oscuro (antipatrones)

- **El árbol de funcionalidades:** el 2º nivel dice "modo oscuro", "notificaciones" en vez de problemas del cliente. Has mapeado soluciones disfrazadas de oportunidades. Vuelve a la voz del cliente.
- **La primera idea:** una sola solución por oportunidad, la que ya traías pensada. Sin comparar 3, no estás descubriendo, estás justificando.
- **El árbol de una sola vez:** lo dibujas en un taller y no lo tocas más. El discovery es continuo; un árbol congelado miente a la semana.
- **El experimento de opinión:** "preguntamos y les gustó". Sin piel en el juego, no mide nada. Busca compromiso real (pago, registro, uso).
- **Dos resultados a la vez:** el árbol intenta subir retención y activación e ingresos. Se difumina. Un resultado por árbol.
- **Saltar el testeo de riesgo:** construyes la solución "prometedora" sin probar su mayor riesgo (valor/usabilidad/factibilidad/viabilidad). El experimento existe para matar la idea barata antes de que muera cara.

---

## Frameworks de referencia

- **Teresa Torres — _Continuous Discovery Habits_ (2021)** — origen del Árbol de Oportunidad-Solución y del descubrimiento continuo en trío.
- **Marty Cagan (_Inspired_ / SVPG)** — los cuatro riesgos (Valor, Usabilidad, Factibilidad, Viabilidad) que guían qué testear primero.
- **Dan Olsen — _The Lean Product Playbook_ (2015)** — Opportunity Score para priorizar oportunidades (`Importancia × (1 − Satisfacción)`).
- **Alberto Savoia — _Pretotype It_ (2011)** — experimentos con "piel en el juego" frente a la validación por opinión.

Que la IAgilidad te acompañe.
