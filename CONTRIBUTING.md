# Cómo se organizan las skills

Este repo mantiene un estándar simple para que todas las skills sean consistentes.

## Estructura de una skill

Cada skill vive en su propia carpeta dentro de `skills/`:

```
skills/
  nombre-de-la-skill/
    SKILL.md
```

## El fichero `SKILL.md`

Empieza siempre con un frontmatter YAML:

```markdown
---
name: nombre-de-la-skill
author: Javier Garzás — 233 Academy
description: Una descripción clara de QUÉ hace y CUÁNDO debe activarse. Es lo que el agente lee para decidir si usarla, así que sé concreto en los disparadores.
---

## Propósito
...

## Aplicación
Pasos concretos.

## Ejemplo
Un ejemplo completo y realista.

## Antipatrones
Qué NO hacer.
```

### Reglas

- **`name`** en `kebab-case`, igual que el nombre de la carpeta.
- **`description`** clara y orientada a disparadores: el agente la usa para saber cuándo activar la skill.
- Incluye siempre un **ejemplo realista** y una sección de **antipatrones**.
- Escribe el **método**, no una respuesta genérica: el valor de una skill es el criterio profesional que aporta.

## Añadir una skill nueva

1. Crea `skills/tu-skill/SKILL.md` siguiendo la plantilla.
2. Añádela a la tabla de skills del [`README.md`](README.md).
3. Abre un Pull Request.
