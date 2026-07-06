# Skills de 233 Academy

[![Licencia: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)

Colección de **skills para agentes de IA** (Claude, y compatibles) creadas por **[Javier Garzás](https://www.javiergarzas.com/) — 233 Academy** y compartidas de forma abierta con la comunidad.

Cada skill encapsula una forma de trabajar probada y con criterio profesional, para que el agente no te devuelva un resultado genérico, sino uno que sigue un método real.

---

## ¿Qué es una skill?

Una skill es una carpeta con un fichero `SKILL.md`: instrucciones que le enseñan al agente **cómo hacer bien una tarea concreta** (con su método, sus pasos, su plantilla y sus antipatrones). Cuando la tienes instalada, el agente la activa sola en cuanto detecta que la tarea encaja con su descripción.

---

## Skills disponibles

| Skill | Qué hace |
|-------|----------|
| [`crear-spec-sdd`](skills/crear-spec-sdd/) | Convierte una idea de feature en un `spec.md` completo listo para **SDD (Spec-Driven Development)**, siguiendo el estándar de GitHub Spec Kit: historias priorizadas con criterios de aceptación en Gherkin, requisitos funcionales, entidades, criterios de éxito medibles y suposiciones. |
| [`crear-historias-de-usuario`](skills/crear-historias-de-usuario/) | Aterriza **una única historia de usuario** hasta dejarla lista para que un equipo la coja en un sprint: story statement, criterios de aceptación en Gherkin (happy path + errores), Definition of Ready, Definition of Done, scope, dependencias y validación INVEST. |
| [`mapa-viaje-cliente`](skills/mapa-viaje-cliente/) | Crea un **mapa del viaje del cliente** de principio a fin: etapas, puntos de contacto, acciones, emociones, puntos de dolor y oportunidades, más los momentos críticos (momento ajá, momentos de la verdad, churn) y las mejoras priorizadas. Para encontrar dónde se rompe la experiencia y mejorar conversión y retención. |
| [`mapa-de-historias-usuario`](skills/mapa-de-historias-usuario/) | Crea un **mapa de historias de usuario** (user story mapping de Jeff Patton): columna vertebral de actividades → pasos → tareas, con líneas de release que separan el MVP de lo que viene después. Para construir entendimiento compartido y priorizar el backlog en torno al viaje del usuario. |
| [`validar-idea-antes-de-construir`](skills/validar-idea-antes-de-construir/) | Convierte una idea o iniciativa en una **hipótesis testeable** (si/entonces): acción, persona y resultado esperado, más los experimentos ligeros para validarla y las medidas de éxito **antes de construir**. Para tratar las iniciativas como apuestas con criterios de cierre, no como promesas. |
| [`cuando-usar-ia-metodo-ed2a`](skills/cuando-usar-ia-metodo-ed2a/) | Decide **cuándo usar IA (y cuándo no)** con el método propio **ED2A** (Eliminar · Delegar · Agilizar · Automatizar → IA): la IA como último recurso, no como primer reflejo. Incluye el filtro de las 4 variables y los principios de estrategia de IA de referentes del sector. Contra el "IA por el simple hecho de usar IA". |

_La lista irá creciendo._

---

## Cómo usar una skill

### En Claude Code

1. Clona este repositorio (o descárgalo como ZIP):
   ```bash
   git clone https://github.com/javier-garzas/ia-product-management.git
   ```
2. Copia la carpeta de la skill que quieras dentro de tu carpeta de skills personales:
   ```bash
   cp -r ia-product-management/skills/crear-spec-sdd ~/.claude/skills/
   ```
3. Ya está. En tu próxima sesión, el agente activará la skill cuando la tarea encaje, o puedes invocarla con `/crear-spec-sdd`.

### En Claude (app de escritorio / web)

1. Descarga la carpeta de la skill (por ejemplo `crear-spec-sdd/`) o el repo completo.
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

---

_Que la IAgilidad te acompañe._
