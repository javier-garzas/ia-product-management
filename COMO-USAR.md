# Cómo usar estas skills

Guía para instalar y usar las skills de este repositorio. Está pensada para un perfil un poco técnico (sabes usar una terminal y `git`), pero cada paso es copia-y-pega.

> ♻️ **Son portables — no es solo para Claude.** Cada skill es texto en Markdown, así que su conocimiento funciona con **cualquier IA** (Claude, ChatGPT/Codex, Gemini, Cursor, GitHub Copilot…). La instalación "nativa" en Claude añade la comodidad de que se **activen solas**, pero el método vale en todas partes. Y lo que producen (por ejemplo un `spec.md` con `crear-spec-sdd`) es **agnóstico de herramienta**: lo lees o lo ejecutas con el agente de coding que quieras.

---

## 1. ¿Qué es una skill?

Cada skill es una **carpeta** con un fichero `SKILL.md` dentro (y, a veces, ficheros de apoyo en subcarpetas como `referencia/`). Ese `SKILL.md` le enseña al agente **cómo hacer bien una tarea**, con su método, sus pasos y sus ejemplos.

Hay dos maneras de aprovecharlas:

- **Instalación nativa** (Claude Code o la app de Claude) → la skill se **activa sola** cuando tu petición encaja. La vía más cómoda.
- **Portable** → coges el contenido del `SKILL.md` y lo usas como contexto en **cualquier otra IA**. Menos automático, igual de válido.

> ⚠️ **Regla de oro (instalación nativa):** una skill se instala **con su carpeta completa**, no solo el `SKILL.md`. Algunas (p. ej. `crear-y-revisar-okrs`) incluyen ficheros de apoyo que tienen que viajar con ella.

---

## 2. Instalar en Claude Code (recomendado)

Las skills personales de Claude Code viven en:

- **macOS / Linux:** `~/.claude/skills/`
- **Windows:** `%USERPROFILE%\.claude\skills\`

### Opción A — instalar todo el repositorio (todas las skills)

**macOS / Linux:**
```bash
git clone https://github.com/javier-garzas/ia-product-management.git
mkdir -p ~/.claude/skills
cp -r ia-product-management/skills/* ~/.claude/skills/
```

**Windows (PowerShell):**
```powershell
git clone https://github.com/javier-garzas/ia-product-management.git
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse ia-product-management\skills\* "$env:USERPROFILE\.claude\skills\"
```

### Opción B — instalar solo una skill

Cambia `crear-spec-sdd` por la que quieras:

**macOS / Linux:**
```bash
cp -r ia-product-management/skills/crear-spec-sdd ~/.claude/skills/
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse ia-product-management\skills\crear-spec-sdd "$env:USERPROFILE\.claude\skills\"
```

### ¿Solo para un proyecto?

Si la quieres únicamente en un proyecto concreto, cópiala en la carpeta `.claude/skills/` **dentro de ese proyecto** en vez de en tu carpeta personal.

---

## 3. Instalar en la app de Claude (escritorio / web)

1. Descarga el repo como ZIP (**Code → Download ZIP** en GitHub) o clónalo.
2. Localiza la carpeta de la skill que quieras dentro de `skills/`.
3. En Claude, ve a **Ajustes → Capabilities / Skills** y **sube la carpeta de la skill** (o un `.zip` de esa carpeta, si te lo pide).

---

## 4. Usar las skills con otras IAs (son portables)

Como el `SKILL.md` es solo texto, puedes usar su método en cualquier asistente, sin instalación nativa:

- **ChatGPT / Codex, Gemini, Claude web…** — abre el `SKILL.md` de la skill, copia su contenido y **pégalo como contexto** al inicio de la conversación (o como *system prompt* / *custom instructions*). Luego pídele la tarea.
- **Cursor, GitHub Copilot, Windsurf y otros IDE con IA** — guarda el `SKILL.md` en tu proyecto (p. ej. en una carpeta `docs/` o como regla del proyecto) y pídele al agente que lo siga. Ideal para `crear-spec-sdd`: generas el `spec.md` y lo usas ahí mismo para que el agente programe.
- **Como fichero adjunto** — muchas IAs permiten adjuntar el `.md` y trabajar sobre él.

> 💡 La gran ventaja del enfoque **spec-driven**: la spec es un artefacto **portable**. La escribes una vez (con `crear-spec-sdd`) y la reutilizas con el agente de coding que prefieras, hoy o dentro de un año, cambies de herramienta o no.

---

## 5. Cómo se usa, ya instalada (Claude)

- **Automática:** describe tu tarea con normalidad; si encaja con la descripción de una skill, Claude la activa sola.
  > *"Ayúdame a montar el spec de una feature de lista de deseos"* → se activa `crear-spec-sdd`.
- **Explícita:** invócala escribiendo `/` y su nombre.
  > `/facilitar-inception-agil`

Varias skills son **conversacionales** (te preguntan paso a paso): `crear-lean-canvas`, `crear-y-revisar-okrs`, `facilitar-inception-agil`, `diseno-organizacional-agil`.

---

## 6. Cómo actualizar

**macOS / Linux:**
```bash
cd ia-product-management && git pull
cp -r skills/* ~/.claude/skills/
```

**Windows (PowerShell):**
```powershell
cd ia-product-management; git pull
Copy-Item -Recurse -Force skills\* "$env:USERPROFILE\.claude\skills\"
```

---

## 7. Problemas frecuentes

- **"No se activa la skill".** Comprueba que la carpeta está en `~/.claude/skills/` (o `%USERPROFILE%\.claude\skills\`) y que **dentro** hay un `SKILL.md`. Reinicia la sesión.
- **Copié solo el `SKILL.md` y algo falla.** Copia la **carpeta completa**; algunas skills necesitan sus subcarpetas.
- **No veo la sección Skills en la app.** Depende de tu plan/versión. Usa Claude Code, o el modo **portable** (sección 4) con la IA que tengas.

---

## 8. Licencia y créditos

Skills creadas por **Javier Garzás — 233 Academy**, bajo licencia **CC BY-NC-SA 4.0** (úsalas y adáptalas citando la autoría; no comercial). Ojo: la **[Guía de OKRs](skills/crear-y-revisar-okrs/referencia/guia-okrs.md)** incluida tiene **su propia licencia** (CC BY-NC-ND). Ver el [README](README.md) para el detalle.

_Que la IAgilidad te acompañe._
