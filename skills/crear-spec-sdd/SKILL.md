---
name: crear-spec-sdd
author: Javier Garzás — 233 Academy
description: Convierte una idea de feature en un spec.md completo, listo para SDD (Spec-Driven Development). Sigue el estándar de GitHub Spec Kit: historias priorizadas con criterios de aceptación en Gherkin, requisitos funcionales, entidades, criterios de éxito medibles y suposiciones. Céntrate en el QUÉ y el PORQUÉ, nunca en el CÓMO técnico. Úsala cuando tengas una feature o un problema y quieras dejar la especificación que más adelante se le pasará a una herramienta de coding con IA.
---

## Propósito
Convierte la descripción de una feature en un fichero **`spec.md`** completo y sin ambigüedades, listo para ser la fuente de verdad de la que, en un paso posterior, un agente de coding genere plan, tareas y código.

Sigue el estándar de facto de SDD en 2026: **GitHub Spec Kit** (el `spec.md` que produce su comando `specify`). Esta skill no escribe el plan ni las tareas ni el código: se detiene en la spec, que es la pieza que hay que clavar.

Su corazón son historias de usuario con criterios de aceptación testables. Para aterrizar UNA historia en profundidad puedes apoyarte en la skill `historia-de-usuario`; esta skill se encarga de reunir varias, priorizarlas y envolverlas con todo lo que un `spec.md` necesita alrededor.

## Qué es una spec en SDD (y en qué se diferencia de una historia)

Esto es el eje de todo, Rebelde IAgil, y hay que tenerlo claro:

- Una **historia de usuario** es negociable y deliberadamente incompleta: es el arranque de una conversación entre humanos.
- Una **spec SDD** es lo contrario: precisa, completa y no ambigua, porque quien la "lee" para construir ya no es un humano que pregunta, es un **agente que ejecuta**. Lo que dejes a medias, el agente se lo inventará.

La spec captura el **QUÉ** (qué necesita el usuario) y el **PORQUÉ** (qué valor entrega), y **nunca el CÓMO técnico**. Nada de stack, frameworks, APIs, tablas ni estructura de código. Esa es la regla de oro: si empiezas a decidir tecnología dentro de la spec, la estás contaminando y la atas a decisiones que aún no toca tomar.

Cuando algo no lo sabes, **no lo inventes**: márcalo con `[NECESITA ACLARACIÓN: ...]`. Es preferible una spec honesta con huecos marcados que una spec falsamente completa.

---

## Aplicación

**Cómo ejecutar esta skill (léelo antes de empezar, Rebelde IAgil):**
1. **Reúne el contexto de la feature.** Necesitas: problema que resuelve, usuarios afectados y resultado deseado. Si no te lo han dado, **pregúntalo antes de escribir nada**. No inventes usuarios ni motivaciones.
2. **QUÉ y PORQUÉ, nunca CÓMO.** Si te sale escribir tecnología (base de datos, endpoint, librería, framework), párate: eso va en el plan, no en la spec.
3. **No rellenes a ciegas.** Todo lo que no puedas derivar del contexto se marca `[NECESITA ACLARACIÓN: pregunta concreta]`.
4. **Prioriza las historias.** Cada historia lleva P1 / P2 / P3, y debe poder probarse de forma independiente.
5. **Salida = un único fichero `spec.md`** con la estructura de la plantilla de más abajo, listo para copiar/guardar.
6. **Una feature por spec.** Si el alcance es enorme, dilo y propón partirlo en varias specs antes de escribir.

---

### Paso 1: Entiende la feature y su alcance (discovery mínimo)

Antes de especificar, ten claro:
- **El problema:** ¿qué intenta lograr el usuario y qué le frena hoy? Una frase.
- **Los usuarios/personas:** ¿para quién es? Personas concretas, no "usuario" genérico.
- **El resultado y el valor:** ¿cómo es el éxito para el usuario y para el negocio?
- **Los límites:** qué entra y —muy importante en SDD— **qué queda fuera de alcance**.

Si te faltan datos para algo de esto, no sigas a ciegas: pregúntalo o márcalo como `[NECESITA ACLARACIÓN]`.

---

### Paso 2: Escribe las historias priorizadas con sus criterios de aceptación

Cada historia del `spec.md` lleva:
- Un **título breve** y una **prioridad**: **P1** (imprescindible, el MVP no existe sin ella), **P2** (importante), **P3** (deseable).
- El **journey en lenguaje llano** (formato Como / quiero / para).
- **Por qué esta prioridad:** una línea que justifica el orden.
- **Test independiente:** cómo se puede probar esa historia por sí sola, sin las demás.
- **Escenarios de aceptación** en Gherkin (Dado / Cuando / Entonces), con happy path Y casos de error.

Regla: un solo "Cuando" por escenario; varios escenarios (feliz + alternativos) es correcto. Si una historia necesita 5 "Cuando" no relacionados, divídela. (Para aterrizar una historia concreta en detalle, apóyate en la skill `historia-de-usuario`.)

---

### Paso 3: Casos límite (Edge Cases)

Lista qué pasa cuando algo no va como se espera: producto agotado, usuario no logueado, carrito vacío, pago rechazado, sin conexión, datos inválidos, límites de volumen. Cada caso límite suele convertirse en un escenario de error dentro de alguna historia.

---

### Paso 4: Requisitos funcionales y entidades

**Requisitos funcionales:** numéralos y redáctalos como capacidades verificables del sistema.
- Formato: `FR-001: El sistema DEBE [capacidad concreta y testable]`.
- Cada FR debe ser comprobable. Nada de "el sistema debe ser rápido" (no falsable) → "el sistema DEBE mostrar resultados en menos de 2 segundos".
- Lo que no esté claro: `FR-00X: El sistema DEBE [...] [NECESITA ACLARACIÓN: ...]`.

**Entidades clave (solo si la feature maneja datos):** enumera los conceptos de datos y qué representan, sin implementación.
- Formato: `[Entidad]: qué representa, atributos clave, relaciones`. Sin tipos, sin tablas, sin SQL.

---

### Paso 5: Criterios de éxito medibles

Numéralos y hazlos **medibles y no técnicos** (resultados, no funcionalidades).
- Formato: `SC-001: [resultado medible]`.
- Ejemplos: "SC-001: El 90% de los clientes completa la compra sin abandonar en el paso de pago"; "SC-002: El tiempo medio hasta finalizar el pedido baja de 3 a 2 minutos".
- Evita métricas de implementación (nada de "latencia de la API"): habla del resultado para el usuario o el negocio.

---

### Paso 6: Suposiciones (Assumptions)

Lista de forma explícita lo que estás dando por hecho: sobre los usuarios, sobre los límites de alcance y sobre dependencias de sistemas o datos que ya existen. Hacer visibles las suposiciones evita malentendidos cuando el agente construya.

---

### Paso 7: Marca los huecos y valida

- Repasa toda la spec buscando ambigüedades y márcalas con `[NECESITA ACLARACIÓN: ...]`.
- Comprueba que **no se ha colado ningún CÓMO técnico**.
- Comprueba que cada historia es independiente, priorizada y testable, y que cada FR y cada SC son verificables.
- Si quedan `[NECESITA ACLARACIÓN]`, la spec está en borrador: enumera esas preguntas al usuario para cerrarlas.

---

## Plantilla de spec.md

```markdown
# Especificación de Feature: [NOMBRE DE LA FEATURE]

**Rama**: `[###-nombre-feature]`
**Creada**: [FECHA]
**Estado**: Borrador
**Input**: Descripción del usuario: "[texto original de la petición]"

## Escenarios de usuario y pruebas *(obligatorio)*

### Historia de Usuario 1 - [Título breve] (Prioridad: P1)

[El journey en lenguaje llano: Como [persona], quiero [acción], para [resultado].]

**Por qué esta prioridad**: [una línea justificando por qué es P1]

**Test independiente**: [cómo se prueba esta historia por sí sola]

**Escenarios de aceptación**:
1. **Dado** [contexto], **Cuando** [acción], **Entonces** [resultado esperado]
2. **Dado** [contexto de error], **Cuando** [acción], **Entonces** [cómo responde el sistema]

### Historia de Usuario 2 - [Título breve] (Prioridad: P2)

[...]

**Por qué esta prioridad**: [...]
**Test independiente**: [...]
**Escenarios de aceptación**:
1. **Dado** [...], **Cuando** [...], **Entonces** [...]

### Casos límite

- ¿Qué pasa cuando [condición límite]?
- ¿Cómo maneja el sistema [escenario de error]?

## Requisitos *(obligatorio)*

### Requisitos funcionales

- **FR-001**: El sistema DEBE [capacidad concreta y verificable]
- **FR-002**: El sistema DEBE [...]
- **FR-003**: El sistema DEBE [...] [NECESITA ACLARACIÓN: pregunta concreta]

### Entidades clave *(incluir si la feature maneja datos)*

- **[Entidad 1]**: [qué representa, atributos clave, relaciones — sin implementación]
- **[Entidad 2]**: [...]

## Criterios de éxito *(obligatorio)*

### Resultados medibles

- **SC-001**: [resultado medible, no técnico]
- **SC-002**: [...]

## Suposiciones

- [Suposición sobre usuarios / alcance / dependencias]
- [...]
```

---

## El Lado Oscuro de las specs (antipatrones)

- **La spec viejuna que decide el CÓMO:** mete stack, endpoints o tablas. Ata la solución antes de tiempo. (Eso va en el plan.)
- **El requisito no falsable:** "el sistema debe ser rápido / intuitivo / escalable". Si no se puede medir, no es un requisito, es un deseo.
- **La spec que rellena huecos a ciegas:** en vez de `[NECESITA ACLARACIÓN]`, inventa datos que nadie ha validado. El agente los construirá tal cual.
- **La historia sin prioridad:** todo es "importante", así que nada lo es. Sin P1/P2/P3 no hay MVP.
- **La spec sin "fuera de alcance":** si no dices qué NO se hace, el agente asume que todo entra.
- **El criterio de éxito de implementación:** "latencia de la API < 100ms" en vez de "el cliente completa la compra sin frustrarse". La spec mide resultado, no tripas.
- **La spec-monstruo:** una sola spec que abarca media aplicación. Si no cabe en la cabeza, pártela en varias features.

---

## Ejemplo (spec.md de una tienda online)

```markdown
# Especificación de Feature: Lista de deseos y aviso de disponibilidad

**Rama**: `001-lista-de-deseos`
**Creada**: 2026-07-06
**Estado**: Borrador
**Input**: Descripción del usuario: "Quiero que los clientes puedan guardar productos que aún no compran y que les avisemos si vuelve el stock"

## Escenarios de usuario y pruebas *(obligatorio)*

### Historia de Usuario 1 - Guardar productos para más tarde (Prioridad: P1)

Como cliente de la tienda online que aún no se decide a comprar, quiero guardar un producto en mi lista de deseos, para encontrarlo fácilmente y comprarlo más adelante sin volver a buscarlo.

**Por qué esta prioridad**: sin poder guardar, el resto de la feature (avisos, compartir) no tiene sobre qué construirse. Es el mínimo que ya entrega valor.

**Test independiente**: se puede probar guardando y recuperando productos, sin necesidad de los avisos de stock ni de nada más.

**Escenarios de aceptación**:
1. **Dado** que he iniciado sesión y estoy en la página de un producto, **Cuando** pulso "Añadir a la lista de deseos", **Entonces** el producto aparece en mi lista y el icono queda marcado como guardado.
2. **Dado** que no he iniciado sesión, **Cuando** pulso "Añadir a la lista de deseos", **Entonces** se me pide iniciar sesión o registrarme, y al hacerlo el producto queda guardado.

### Historia de Usuario 2 - Aviso cuando vuelve el stock (Prioridad: P2)

Como cliente que quiere un producto agotado, quiero que me avisen cuando vuelva a estar disponible, para comprarlo antes de que se acabe de nuevo.

**Por qué esta prioridad**: aporta mucho valor, pero depende de que la lista de deseos (P1) exista primero.

**Test independiente**: se puede probar marcando un producto agotado y simulando la reposición de stock para comprobar que llega el aviso.

**Escenarios de aceptación**:
1. **Dado** que tengo en la lista de deseos un producto agotado, **Cuando** el producto vuelve a tener stock, **Entonces** recibo un aviso con el enlace al producto.
2. **Dado** que el producto sigue agotado, **Cuando** reviso mi lista de deseos, **Entonces** veo el producto marcado como "sin stock" y la opción de activar el aviso.

### Casos límite

- ¿Qué pasa si el producto se elimina del catálogo mientras está en una lista de deseos?
- ¿Cómo se maneja un cliente que añade el mismo producto dos veces?
- ¿Qué pasa si el stock vuelve y se agota otra vez antes de que el cliente entre?

## Requisitos *(obligatorio)*

### Requisitos funcionales

- **FR-001**: El sistema DEBE permitir a un cliente identificado añadir y quitar productos de su lista de deseos.
- **FR-002**: El sistema DEBE conservar la lista de deseos entre sesiones del mismo cliente.
- **FR-003**: El sistema DEBE permitir activar un aviso de disponibilidad sobre un producto agotado de la lista.
- **FR-004**: El sistema DEBE notificar al cliente cuando un producto con aviso activo vuelve a tener stock.
- **FR-005**: El sistema DEBE mostrar el estado de stock de cada producto de la lista. [NECESITA ACLARACIÓN: ¿en tiempo real o al abrir la lista?]

### Entidades clave

- **Lista de deseos**: pertenece a un cliente; contiene productos guardados y la fecha en que se añadieron.
- **Producto guardado**: referencia a un producto del catálogo, con su estado de stock y si tiene aviso activo.
- **Aviso de disponibilidad**: relación entre un cliente y un producto agotado que dispara una notificación al reponerse.

## Criterios de éxito *(obligatorio)*

- **SC-001**: Al menos el 25% de los clientes que usan la lista de deseos acaban comprando un producto guardado.
- **SC-002**: El 80% de los avisos de disponibilidad se entregan en menos de 1 hora desde la reposición de stock.
- **SC-003**: El uso de la lista de deseos reduce en un 10% los productos abandonados sin ninguna acción.

## Suposiciones

- Solo los clientes identificados tienen lista de deseos (los anónimos no).
- Queda FUERA de alcance en esta feature: compartir la lista con otras personas y las listas múltiples por cliente.
- Existe ya un sistema de notificaciones (email/push) reutilizable para los avisos.
```

---

## Frameworks de referencia

- **GitHub Spec Kit** — estándar de SDD; su `spec.md` es la base de esta plantilla (Spec → Plan → Tasks → Implement).
- **Spec-Driven Development (SDD)** — la spec es la fuente de verdad; el código es la salida generada, no al revés.
- **Regla QUÉ-no-CÓMO** — la spec describe qué necesita el usuario y por qué, nunca la tecnología.
- **Gherkin** — criterios de aceptación "Dado / Cuando / Entonces".
- **INVEST** — para que cada historia sea Independiente, Negociable, Valiosa, Estimable, Pequeña y Testable.

Que la IAgilidad te acompañe.
