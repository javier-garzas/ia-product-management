# Skills de 233 Academy · IA + Product Management

> ### 🧭 Del problema del cliente a la spec — con criterio.

[![Skills](https://img.shields.io/badge/Skills-12-2ea44f.svg)](#skills-disponibles)
[![Método ED2A](https://img.shields.io/badge/M%C3%A9todo-ED2A-blueviolet.svg)](skills/cuando-usar-ia-metodo-ed2a/)
[![Licencia: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)

Colección de **12 skills para agentes de IA** (Claude, y compatibles) creadas por **[Javier Garzás](https://www.javiergarzas.com/) — 233 Academy** y compartidas de forma abierta con la comunidad.

Cada skill encapsula una forma de trabajar probada y con criterio profesional, para que el agente no te devuelva un resultado genérico, sino uno que sigue un método real. Juntas forman **un método de producto de punta a punta: del riesgo a la spec.**

---

## ⭐ El método ED2A — la IA como último recurso, no el primero

El corazón de este repo es **ED2A**, el método propio de Javier Garzás para no caer en el _"IA por el simple hecho de usar IA"_:

> **Antes de llevar nada a la IA, súbelo por la escalera:**
> **E**liminar · **D**elegar · **A**gilizar · **A**utomatizar → y **solo entonces, IA.**

Cada escalón se descarta antes de subir al siguiente, y solo automatizas o aplicas IA a lo que pasa el **filtro de las 4 variables** (aporta valor · se hace con frecuencia · lleva tiempo · es explicable a un becario). Nada de automatizar algo de 3 segundos.

👉 **[Abrir la skill `cuando-usar-ia-metodo-ed2a`](skills/cuando-usar-ia-metodo-ed2a/)**

---

## Cómo encajan: del riesgo a la spec

Las skills no son piezas sueltas: cubren el recorrido completo de una decisión de producto, desde _"¿esto siquiera merece IA?"_ hasta la especificación lista para construir.

```mermaid
flowchart TD
    LC["💡 crear-lean-canvas<br/>Modelo de negocio en 1 página"]
    OK["📈 crear-y-revisar-okrs<br/>Fijar los resultados (OKRs)"]
    A["🚪 cuando-usar-ia-metodo-ed2a<br/>¿Toca IA? — método ED2A"]
    T["🌳 arbol-oportunidad-solucion<br/>Estructurar el discovery"]
    P["🎯 priorizar-funcionalidades<br/>¿En qué trabajar primero?"]
    B["✅ validar-idea-antes-de-construir<br/>¿Merece construirse?"]
    R["🗓️ planificacion-roadmap<br/>Secuenciar en releases"]
    C["🗺️ mapa-viaje-cliente<br/>¿Dónde duele la experiencia?"]
    D["📊 mapa-de-historias-usuario<br/>¿Qué construir y en qué orden?"]
    G["✂️ division-de-historias-usuario<br/>¿Es demasiado grande? Divídela"]
    E["📝 crear-historias-de-usuario<br/>Cada historia, lista para el sprint"]
    F["📐 crear-spec-sdd<br/>Spec para que la IA lo construya"]
    LC -.-> A
    OK -.-> T
    OK -.-> R
    A --> T --> P --> B --> R --> C --> D --> G --> E --> F
```

**Punto de partida** (negocio o idea nueva): `crear-lean-canvas` — el modelo entero en una página.
**Estrategia** (metas): `crear-y-revisar-okrs` — fija los resultados que persiguen el discovery y el roadmap.
**Decidir y descubrir** (¿qué problema, debo hacerlo?): `ED2A` → `arbol-oportunidad-solucion` → `priorizar` → `validar-idea`.
**Planificar** (¿en qué orden?): `planificacion-roadmap`.
**Diseñar y especificar** (hacerlo bien): `mapa-viaje-cliente` → `mapa-de-historias-usuario` → `division-de-historias-usuario` → `crear-historias-de-usuario` → `crear-spec-sdd`.

No hace falta usarlas en orden: cada una vale por sí sola. El flujo solo muestra cómo se apoyan entre ellas.

---

## ¿Qué es una skill?

Una skill es una carpeta con un fichero `SKILL.md`: instrucciones que le enseñan al agente **cómo hacer bien una tarea concreta** (con su método, sus pasos, su plantilla y sus antipatrones). Cuando la tienes instalada, el agente la activa sola en cuanto detecta que la tarea encaja con su descripción.

---

## Skills disponibles

| Skill | Qué hace |
|-------|----------|
| [`crear-lean-canvas`](skills/crear-lean-canvas/) | Guía **paso a paso, en conversación**, para construir un **Lean Canvas** (Ash Maurya): rellena los 9 bloques uno a uno con preguntas y ejemplos, y entrega el lienzo completo. El punto de partida cuando arrancas un negocio o producto nuevo y quieres su modelo en una página. |
| [`crear-y-revisar-okrs`](skills/crear-y-revisar-okrs/) | Asistente de **OKRs** con el método probado de Javier Garzás: **crea** un OKR (desde visión/misión/estrategia y el reto del trimestre), lo **revisa** con checklist, o **resuelve dudas**. Objetivo cualitativo + máx. 3 KR que son outcomes de impacto (no tareas ni KPIs), con 3 métodos de medición (Radical Focus, Google/Doerr, Lamorte). |
| [`cuando-usar-ia-metodo-ed2a`](skills/cuando-usar-ia-metodo-ed2a/) ⭐ | Decide **cuándo usar IA (y cuándo no)** con el método propio **ED2A** (Eliminar · Delegar · Agilizar · Automatizar → IA): la IA como último recurso. Incluye el filtro de las 4 variables y los principios de estrategia de IA de referentes del sector. Contra el "IA por el simple hecho de usar IA". |
| [`arbol-oportunidad-solucion`](skills/arbol-oportunidad-solucion/) | Construye un **Árbol de Oportunidad-Solución** (OST de Teresa Torres) que conecta un resultado deseado con oportunidades del cliente, soluciones candidatas y experimentos. Para estructurar el discovery y no saltar directo a la solución. Prioriza problemas, no funcionalidades. |
| [`priorizar-funcionalidades`](skills/priorizar-funcionalidades/) | Prioriza un **backlog de ideas** por impacto, esfuerzo, riesgo y alineación estratégica, y devuelve las **5 principales** con justificación, trade-offs y qué se despriorizó. Usa marcos probados (Opportunity Score de Dan Olsen, ICE, RICE). Para decidir en qué trabajar primero con criterio, no por quién grita más. |
| [`validar-idea-antes-de-construir`](skills/validar-idea-antes-de-construir/) | Convierte una idea o iniciativa en una **hipótesis testeable** (si/entonces): acción, persona y resultado esperado, más los experimentos ligeros para validarla y las medidas de éxito **antes de construir**. Trata las iniciativas como apuestas con criterios de cierre, no como promesas. |
| [`planificacion-roadmap`](skills/planificacion-roadmap/) | Convierte la estrategia en un **roadmap orientado a resultados**: reúne entradas, define épicas como hipótesis, prioriza, secuencia en releases (Now/Next/Later) y alinea a stakeholders. Un workflow de 5 fases contra el roadmap "fábrica de funcionalidades". Orquesta `priorizar-funcionalidades` y `validar-idea-antes-de-construir`. |
| [`mapa-viaje-cliente`](skills/mapa-viaje-cliente/) | Crea un **mapa del viaje del cliente** de principio a fin: etapas, puntos de contacto, acciones, emociones, puntos de dolor y oportunidades, más los momentos críticos (momento ajá, momentos de la verdad, churn) y las mejoras priorizadas. Para encontrar dónde se rompe la experiencia y mejorar conversión y retención. |
| [`mapa-de-historias-usuario`](skills/mapa-de-historias-usuario/) | Crea un **mapa de historias de usuario** (user story mapping de Jeff Patton): columna vertebral de actividades → pasos → tareas, con líneas de release que separan el MVP de lo que viene después. Para construir entendimiento compartido y priorizar el backlog en torno al viaje del usuario. |
| [`division-de-historias-usuario`](skills/division-de-historias-usuario/) | Divide una **historia o épica demasiado grande** en historias más pequeñas, verticales y entregables de forma independiente, con los 8 patrones de división probados (flujo, reglas, datos, criterios de aceptación, esfuerzo, dependencias, DevOps y actos de descubrimiento). Para bajar el tamaño de lote, reducir riesgo y mantener el flujo. |
| [`crear-historias-de-usuario`](skills/crear-historias-de-usuario/) | Aterriza **una única historia de usuario** hasta dejarla lista para que un equipo la coja en un sprint: story statement, criterios de aceptación en Gherkin (happy path + errores), Definition of Ready, Definition of Done, scope, dependencias y validación INVEST. |
| [`crear-spec-sdd`](skills/crear-spec-sdd/) | Convierte una idea de feature en un `spec.md` completo listo para **SDD (Spec-Driven Development)**, siguiendo el estándar de GitHub Spec Kit: historias priorizadas con criterios de aceptación en Gherkin, requisitos funcionales, entidades, criterios de éxito medibles y suposiciones. |

**12 skills** — y la lista irá creciendo.

---

## Cómo usar una skill

### En Claude Code

1. Clona este repositorio (o descárgalo como ZIP):
   ```bash
   git clone https://github.com/javier-garzas/ia-product-management.git
   ```
2. Copia la carpeta de la skill que quieras dentro de tu carpeta de skills personales:
   ```bash
   cp -r ia-product-management/skills/cuando-usar-ia-metodo-ed2a ~/.claude/skills/
   ```
3. Ya está. En tu próxima sesión, el agente activará la skill cuando la tarea encaje, o puedes invocarla con `/cuando-usar-ia-metodo-ed2a`.

### En Claude (app de escritorio / web)

1. Descarga la carpeta de la skill (por ejemplo `cuando-usar-ia-metodo-ed2a/`) o el repo completo.
2. En **Ajustes → Capabilities / Skills**, súbela como skill personalizada.

> La carpeta de skills personales en Claude Code suele ser `~/.claude/skills/` (macOS/Linux) o `%USERPROFILE%\.claude\skills\` (Windows).

---

## Autoría y licencia

Creado por **Javier Garzás — [233 Academy](https://233gradosdeti.com/)**.

Este material se publica bajo licencia **[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0)](LICENSE)**:

- ✅ Puedes **usarlo y adaptarlo** libremente, **citando la autoría**.
- ✅ Debes **compartir tus adaptaciones bajo la misma licencia**.
- ❌ **No puedes usarlo con fines comerciales** sin permiso.

Si quieres un uso comercial, escribe a [hello@233gradosdeti.com](mailto:hello@233gradosdeti.com).

> **Excepción — material incluido con licencia propia:** la [Guía de OKRs](skills/crear-y-revisar-okrs/referencia/guia-okrs.md) (base de conocimiento de la skill `crear-y-revisar-okrs`) se publicó bajo **CC BY-NC-ND 4.0** (Reconocimiento-NoComercial-SinObraDerivada), distinta de la licencia del resto del repo. Se incluye por su autor, Javier Garzás. © 233gradosdeTI.

---

_Que la IAgilidad te acompañe._
