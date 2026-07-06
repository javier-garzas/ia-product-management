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

_La lista irá creciendo._

---

## Cómo usar una skill

### En Claude Code

1. Clona este repositorio (o descárgalo como ZIP):
   ```bash
   git clone https://github.com/USUARIO/JAVIER-GARZAS-233-ACADEMY-SKILLS.git
   ```
2. Copia la carpeta de la skill que quieras dentro de tu carpeta de skills personales:
   ```bash
   cp -r JAVIER-GARZAS-233-ACADEMY-SKILLS/skills/crear-spec-sdd ~/.claude/skills/
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
