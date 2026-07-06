# Cómo usar estas skills

Guía para instalar y usar las skills de este repositorio. Está pensada para un perfil un poco técnico (sabes usar una terminal y `git`), pero cada paso es copia-y-pega.

---

## 1. ¿Qué es una skill y qué necesitas?

Cada skill es una **carpeta** con un fichero `SKILL.md` dentro (y, a veces, ficheros de apoyo en subcarpetas como `referencia/`). Ese `SKILL.md` le enseña al agente **cómo hacer bien una tarea**, con su método, sus pasos y sus ejemplos.

Necesitas una herramienta que **soporte Agent Skills**. Las dos vías más habituales:

- **Claude Code** (CLI / extensión de IDE) — la vía recomendada si eres técnico.
- **La app de Claude (escritorio o web)** — subiendo la skill en los ajustes.

> ⚠️ **Regla de oro:** una skill se instala **con su carpeta completa**, no solo el `SKILL.md`. Algunas (p. ej. `crear-y-revisar-okrs`) incluyen ficheros de apoyo en subcarpetas que tienen que viajar con ella.

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

Si la quieres únicamente en un proyecto concreto (y no en todo tu equipo), cópiala en la carpeta `.claude/skills/` **dentro de ese proyecto** en vez de en tu carpeta personal.

---

## 3. Instalar en la app de Claude (escritorio / web)

1. Descarga el repo como ZIP (botón verde **Code → Download ZIP** en GitHub) o clónalo.
2. Localiza la carpeta de la skill que quieras dentro de `skills/` (por ejemplo `crear-lean-canvas/`).
3. En Claude, ve a **Ajustes → Capabilities / Skills** y **sube la carpeta de la skill** (o un `.zip` de esa carpeta, si te lo pide).

> Si te pide un `.zip`, comprime la **carpeta de la skill entera** (la que contiene el `SKILL.md`), no solo el fichero.

---

## 4. Cómo se usa, ya instalada

Tienes dos formas:

- **Automática:** describe tu tarea con normalidad. Si encaja con la descripción de una skill, Claude la activa solo.
  > *"Ayúdame a montar el spec de una feature de lista de deseos"* → se activa `crear-spec-sdd`.
- **Explícita:** invócala escribiendo `/` y su nombre.
  > `/facilitar-inception-agil`

Muchas skills son **conversacionales** (te van preguntando paso a paso): `crear-lean-canvas`, `crear-y-revisar-okrs`, `facilitar-inception-agil`, `diseno-organizacional-agil`. Solo tienes que seguirles la conversación.

---

## 5. Cómo actualizar

Cuando se publiquen nuevas skills o mejoras:

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

## 6. Problemas frecuentes

- **"No se activa la skill".** Comprueba que la carpeta está en `~/.claude/skills/` (o `%USERPROFILE%\.claude\skills\`) y que **dentro** hay un `SKILL.md`. Reinicia la sesión de Claude Code.
- **Copié solo el `SKILL.md` y algo falla.** Copia la **carpeta completa**; algunas skills necesitan sus subcarpetas.
- **No veo la sección Skills en la app.** La disponibilidad depende de tu plan/versión de Claude. En ese caso, usa Claude Code.

---

## 7. Licencia y créditos

Skills creadas por **Javier Garzás — 233 Academy**, bajo licencia **CC BY-NC-SA 4.0** (úsalas y adáptalas citando la autoría; no comercial). Ojo: la **[Guía de OKRs](skills/crear-y-revisar-okrs/referencia/guia-okrs.md)** incluida tiene **su propia licencia** (CC BY-NC-ND). Ver el [README](README.md) para el detalle.

_Que la IAgilidad te acompañe._
