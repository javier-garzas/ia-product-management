---
name: hipotesis-de-epica
author: Javier Garzás — 233 Academy
description: Enmarca una épica como una hipótesis testeable con estructura si/entonces — acción o solución, persona objetivo, resultado esperado — más los experimentos ligeros para validarla y las medidas de éxito antes de comprometerte a construir. Úsala cuando definas una iniciativa importante antes del roadmap, el discovery o la entrega, para gestionar la incertidumbre y tratar las épicas como apuestas y no como promesas. No la uses para una funcionalidad ya validada (salta a `crear-historias-de-usuario`), ni cuando el QUÉ ya está decidido y toca especificar para construir (para eso está `crear-spec-sdd`).
---

# Hipótesis de Épica

## Propósito

Convierte una épica en una **hipótesis testeable**: una apuesta explícita sobre qué crees que pasará, para quién y cómo lo vas a comprobar — con experimentos ligeros y criterios de éxito medibles **antes** de comprometerte a una construcción completa.

Esto **no es una especificación de requisitos**: es una hipótesis que estás testeando, no una funcionalidad que te has comprometido a entregar. La diferencia lo cambia todo: una spec se construye; una hipótesis se puede (y se debe) invalidar.

## Rol

Eres un Product Manager senior que trabaja guiado por evidencia, no por opinión. Sabes que la mayoría de las ideas de producto son falsas hasta que se demuestran, así que tu instinto no es "¿cómo lo construyo?" sino "¿cómo compruebo barato si merece la pena construirlo?". Cuando no tengas datos del problema, lo dices y lo marcas como `[SUPOSICIÓN: ...]` en lugar de disfrazar una corazonada de certeza.

## Qué es una hipótesis de épica (y qué NO es)

Ten claro el eje, Rebelde IAgil: una épica bien planteada es una **apuesta con criterios de cierre**, no una promesa.

### El marco de la hipótesis (Lean UX, Tim Herbig)

Estructura **si/entonces**:

- **Si** [acción o solución] **para** [persona objetivo]
- **Entonces** [obtendremos / lograremos un resultado deseable o un job-to-be-done]

Acompañada de dos piezas que la hacen real:

- **Experimentos (pequeños actos de descubrimiento):** las pruebas rápidas y baratas con las que testeas el supuesto antes de construir.
- **Medidas de validación:** qué observarás, cuánto y en qué plazo para dar la hipótesis por válida o falsa.

### Por qué funciona

- **Guiada por hipótesis:** te obliga a declarar lo que crees (y en lo que podrías estar equivocado).
- **Enfocada en resultados:** el "Entonces" habla del beneficio para el usuario, no de la feature entregada.
- **Experimento primero:** empuja a validar ligero antes de la construcción completa.
- **Falsable:** unos criterios claros permiten **descartar malas ideas pronto**.
- **Gestión de riesgo:** trata las épicas como apuestas, no como compromisos.

### Qué NO es

- **No es una spec de funcionalidad:** "construir un dashboard con 5 gráficos" es una feature, no una hipótesis.
- **No es un compromiso garantizado:** las hipótesis pueden y deben invalidarse.
- **No está enfocada en la salida:** "entregar la función X para Q2" se olvida de lo único que importa: ¿logró el resultado?
- **No vive sin experimentos:** si te saltas las pruebas y vas directo a construir, no estás testeando nada.

### Dónde encaja respecto a sus skills hermanas

- Si la hipótesis **se valida** → descompón la épica en historias con `crear-historias-de-usuario` y sitúala en el `mapa-de-historias-usuario`.
- Cuando el QUÉ ya está decidido y toca especificarlo sin ambigüedad para que lo construya un agente → eso ya es una spec: `crear-spec-sdd`.

### Cuándo usarlo / cuándo no

Úsalo en la exploración temprana de una iniciativa (antes de comprometer el roadmap), para validar encaje de una capacidad nueva, para priorizar (las épicas con hipótesis validada suben) y para gestionar expectativas de stakeholders (enmarcas trabajo como experimentos, no como promesas).

No lo uses para funcionalidades ya validadas (salta a las historias), para ajustes triviales (no sobre-elabores), ni cuando los experimentos no sean viables (raro, pero a veces hay que comprometerse antes de testear).

---

## Aplicación

### Paso 1: Reúne el contexto

Antes de redactar nada, ten claro: el **problema** del usuario, la **persona** que se beneficia, su **job-to-be-done** (qué resultado busca) y las **alternativas actuales** (qué hace hoy: competidores, apaños, o no hacer nada). Si falta esto, no fuerces la hipótesis: haz primero discovery o validación del problema, o márcalo como `[SUPOSICIÓN]`.

### Paso 2: Redacta la hipótesis si/entonces

Reglas de calidad:
- **El "Si" es específico:** no "mejorar el producto", sino "añadir notificaciones de Slack en un clic al asignar tareas".
- **El "para" es una persona concreta:** no "usuarios", sino "project managers remotos con 3+ equipos distribuidos".
- **El "Entonces" es un resultado, no una salida:** no "tendrán notificaciones", sino "responderán a las asignaciones un 50% más rápido".

### Paso 3: Diseña los experimentos (pequeños actos de descubrimiento)

Prueba el supuesto **antes** de construir la épica entera. Tipos habituales:
- **Prototipo + test con usuarios:** simula la función con un prototipo clicable y pásalo con 5-10 usuarios.
- **Test concierge:** haz la función a mano para unos pocos usuarios y mira si la valoran.
- **Landing page:** describe la función y mide registros o interés.
- **Mago de Oz:** preséntala como automatizada, pero opérala a mano por detrás.
- **A/B (si es viable):** versión ligera contra un control.

Cada experimento debe ser **rápido** (días/semanas, no meses), **barato** (nada de builds completos: prototipos, procesos manuales, herramientas que ya tienes) y **falsable** (diseñado para poder demostrarte que estás equivocado).

### Paso 4: Define las medidas de validación

Qué observarás, cuánto y en qué plazo:
- **Plazo realista:** ni 6 meses (demasiado lento) ni 3 días (demasiado pronto). Apunta a 2-4 semanas.
- **Cuantitativo específico:** no "más usuarios", sino "+20% en la tasa de activación".
- **Cualitativo observable:** no "les gusta", sino "8 de cada 10 dicen que pagarían por ella".
- Si no puedes medir el resultado final a tiempo, usa un **indicador adelantado** (activación, no ingresos anuales).

### Paso 5: Ejecuta y decide

Corre los experimentos, mide contra las medidas de validación y toma el punto de decisión:
- ✅ **Validada** → procede: historias de usuario y al roadmap.
- ❌ **Invalidada** → descarta la épica o pivota a otra hipótesis. (Esto es un éxito: te ahorraste construir algo inútil.)
- ⚠️ **No concluyente** → más experimentos o ajusta las medidas.

### Paso 6: Convierte en historias (si se valida)

Descompón la épica validada en historias de usuario con `crear-historias-de-usuario` y colócalas en tu `mapa-de-historias-usuario` para priorizar el MVP.

---

## Plantilla

```markdown
# Hipótesis de épica: [NOMBRE]

## Hipótesis si/entonces
**Si** [acción o solución]
**para** [persona objetivo]
**Entonces** [resultado deseable / job-to-be-done]

## Experimentos (pequeños actos de descubrimiento)
Testearemos el supuesto mediante:
- [Experimento 1 — rápido y barato]
- [Experimento 2 — rápido y barato]

## Medidas de validación
Sabremos que es válida si, dentro de [plazo], observamos:
- [Resultado cuantitativo medible]
- [Resultado cualitativo medible]

## Decisión
[ ] Validada → historias + roadmap  ·  [ ] Invalidada → descartar/pivotar  ·  [ ] No concluyente → más experimentos
```

---

## Ejemplo (completo) — Integración con Google Calendar

```markdown
# Hipótesis de épica: Activación con integración de calendario

## Hipótesis si/entonces
**Si** ofrecemos la integración con Google Calendar en un clic durante el onboarding
**para** usuarios de prueba que gestionan muchas reuniones a la semana
**Entonces** aumentaremos la tasa de activación (llegar al primer valor) del 40% al 50%.

## Experimentos (pequeños actos de descubrimiento)
- **Prototipo + test:** flujo clicable en Figma de la conexión en un clic, probado con
  8 usuarios de prueba, midiendo si entienden el valor y completan el flujo.
- **Mago de Oz:** para 10 cuentas nuevas, conectamos su calendario a mano por detrás
  y observamos si usan el producto más en su primera semana.
- **Landing / botón fantasma:** botón "Conectar Google Calendar" en el onboarding que
  mide la tasa de clic antes de construir la integración real.

## Medidas de validación
Sabremos que es válida si, dentro de 4 semanas, observamos:
- La tasa de activación sube del 40% al 50% (cuantitativo).
- El 75% de los usuarios de prueba encuestados dicen que la integración les ahorró
  tiempo en su primera semana (cualitativo).
- La tasa de clic en el botón fantasma supera el 30% (indicador adelantado de demanda).

## Decisión
[x] Validada → descomponer en historias (conectar cuenta, sincronizar eventos,
    gestionar permisos) y priorizar en el mapa de historias.
```

---

## El Lado Oscuro de las hipótesis de épica (antipatrones)

- **La hipótesis que es una feature:** "Si construimos un dashboard, entonces tendremos un dashboard." Describe la salida, no el resultado; no testea nada. Reescríbela hacia el resultado del usuario ("…los PMs dedicarán un 50% menos de tiempo a pedir estados").
- **Saltarse los experimentos:** "Testearemos el supuesto construyendo la función completa." Eso no es una hipótesis, es un compromiso disfrazado. Diseña pruebas ligeras de días/semanas.
- **La medida de niebla:** "Sabremos que es válida si los usuarios están contentos." Subjetivo e inmedible. Fija métricas falsables ("80% puntúan 4+ sobre 5"; "el tiempo de respuesta baja un 50%").
- **El plazo eterno:** "…si en 6 meses suben los ingresos." Para entonces ya lo has construido. Usa ciclos de 2-4 semanas e indicadores adelantados.
- **La épica que ya era un compromiso:** "Ya se lo dijimos al CEO, así que hay que validarlo." Los experimentos se vuelven teatro: lo vas a construir pase lo que pase. Enmarca como hipótesis **antes** de adquirir el compromiso.
- **Enamorarse de la hipótesis:** ignoras los datos que la contradicen. Invalidar pronto no es fracasar: es ganar el tiempo que no gastas en construir algo muerto.

---

## Frameworks de referencia

- **Tim Herbig — Lean UX Hypothesis Statement** — origen del formato de hipótesis si/entonces.
- **Alberto Savoia — _Pretotype It_ (2011)** — experimentos ligeros para validar la demanda antes de construir ("asegúrate de construir *the right it*").
- **Eric Ries — _The Lean Startup_ (2011)** — el ciclo Construir-Medir-Aprender y los indicadores adelantados frente a las métricas vanidosas.
- **Jobs To Be Done (JTBD)** — para anclar el "Entonces" en el resultado que persigue el usuario.

Que la IAgilidad te acompañe.
