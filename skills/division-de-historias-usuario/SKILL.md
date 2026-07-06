---
name: division-de-historias-usuario
author: Javier Garzás — 233 Academy
description: Divide una historia o épica demasiado grande en historias más pequeñas, verticales y entregables de forma independiente, usando los 8 patrones de división probados (flujo de trabajo, reglas de negocio, variaciones de datos, criterios de aceptación, esfuerzo, dependencias, DevOps y pequeños actos de descubrimiento). Úsala cuando un elemento del backlog sea demasiado grande para estimarlo, secuenciarlo o entregarlo en un sprint, o cuando una historia acumule varios "Cuando/Entonces". No la uses para aterrizar UNA historia ya del tamaño correcto (para eso está `crear-historias-de-usuario`) ni para mapear el conjunto del viaje (para eso está `mapa-de-historias-usuario`).
---

# División de Historias de Usuario

## Propósito

Descompón una historia, épica o funcionalidad grande en historias **más pequeñas, verticales y entregables de forma independiente**, sin perder valor por el camino. El objetivo no es trocear: es **reducir el tamaño de lote** para acelerar el feedback, bajar el riesgo y mantener el flujo del equipo.

En **233 Academy**, Javier Garzás lo resume así, Rebelde IAgil: *una historia grande no es un problema de tamaño, es un problema de **incertidumbre acumulada**.* Dividir bien es la forma de repartir esa incertidumbre en apuestas pequeñas que puedes validar una a una.

## Rol

Eres un facilitador ágil senior que ha partido cientos de historias con equipos reales. Sabes que la división no es una operación mecánica sino una **decisión de diseño**: cada corte debe seguir una línea de valor para el usuario, no una capa técnica. Y sabes cuándo **no** dividir, que es la mitad del oficio.

## El fundamento: por qué el tamaño importa (narrativa)

Dividir historias no es una manía de metodólogos; se apoya en teoría de flujo bien establecida:

- **Tamaño de lote pequeño (Reinertsen).** En _The Principles of Product Development Flow_, Donald Reinertsen demuestra que reducir el tamaño de lote acelera el feedback, reduce el trabajo en curso y baja el riesgo económico de cada entrega. Una historia grande es un lote grande: tarda más en dar señal y esconde más sorpresas.
- **Ley de Little.** El tiempo de ciclo es proporcional al trabajo en curso dividido por el ritmo de entrega. Historias más pequeñas → menos trabajo atascado a la vez → entregas antes y con menos cuellos de botella.
- **Corte vertical, no horizontal.** Cada historia dividida debe atravesar todas las capas (interfaz + lógica + datos) y entregar **una capacidad completa de cara al usuario**. Es el mismo principio del *walking skeleton* del `mapa-de-historias-usuario`: una rebanada fina pero entera, no "la mitad de arriba".

Esta es la regla de oro que hila todo lo demás: **si un corte no entrega valor al usuario por sí mismo, no es una división de historia, es una descomposición en tareas.**

## Qué es (y qué NO es)

- **NO es trocear horizontal:** nada de "historia de front-end" e "historia de back-end". Cada historia entrega valor de punta a punta.
- **NO es descomposición en tareas:** "montar la base de datos", "escribir la API" son tareas, no historias.
- **NO es trocear arbitrario:** partir "gestión de usuarios" en "añadir usuario" y "gestión" no significa nada.
- **SÍ es** repartir una historia grande en varias pequeñas, cada una con su propio resultado de usuario, testeable y entregable sola.

### Dónde encaja respecto a sus skills hermanas

- El `mapa-de-historias-usuario` te da el mapa completo; **esta skill** parte las piezas del mapa que siguen siendo demasiado grandes.
- Una vez dividida, cada historia resultante se aterriza en detalle con `crear-historias-de-usuario`.

### Cuándo usarlo / cuándo no

Úsalo cuando la historia no cabe en un sprint, cuando acumula varios "Cuando/Entonces", cuando una épica necesita incrementos entregables, cuando el equipo no consigue estimarla, o cuando mezcla varias personas o flujos.

No lo uses si la historia ya es pequeña y está bien acotada (no la sobredividas), si dividir crearía dependencias que ralenticen la entrega, o si es una tarea puramente técnica (usa descomposición de ingeniería).

---

## Aplicación

### Paso 1: Parte de la historia original

Empieza con la historia/épica bien escrita en formato de historia de usuario (Como… quiero… para…) y con sus criterios de aceptación. Si no lo está, ponla primero en forma.

### Paso 2: Recorre los 8 patrones de división (en orden, párate en el que aplique)

**Basado en _The Humanizing Work Guide to Splitting User Stories_ de Richard Lawrence y Peter Green.**

**1. Pasos del flujo de trabajo** — ¿hay pasos secuenciales?
> "Registrarse, verificar email y completar onboarding" → (a) registrarse, (b) verificar email, (c) responder 3 preguntas de perfil.

**2. Variaciones de reglas de negocio** — ¿reglas distintas por escenario?
> "Aplicar descuentos (10% miembro, 20% VIP, 5% primerizo)" → una historia por tipo de descuento.

**3. Variaciones de datos** — ¿distintos tipos de entrada?
> "Subir archivos (imágenes, PDFs, vídeos)" → una historia por tipo de archivo.

**4. Complejidad de los criterios de aceptación** — ¿varios "Cuando/Entonces"?
> "Gestionar el carrito" (añadir / eliminar / actualizar cantidad) → una historia por cada par Cuando/Entonces.
>
> **Es el indicador más frecuente:** si ves varios pares Cuando/Entonces, divide justo por ahí.

**5. Esfuerzo mayor** — ¿trabajo técnico entregable por fases?
> "Colaboración en tiempo real" → (a) ver quién está presente, (b) ver cursores en vivo, (c) ver ediciones en vivo.

**6. Dependencias externas** — ¿varios sistemas/APIs?
> "Login con Google, Facebook o Twitter" → una historia por proveedor OAuth.

**7. Pasos de DevOps** — ¿despliegue o infraestructura compleja?
> "Subir archivos grandes a la nube" → (a) archivos pequeños, (b) grandes con progreso, (c) reanudar subidas.

**8. Pequeños Actos de Descubrimiento (TADs)** — si nada de lo anterior aplica, hay incógnitas que despejar.
> "Recomendaciones con IA" (demasiado vago) → prototipar 3 algoritmos, definir métrica de éxito, construir el más simple, medir.
>
> **Ojo:** los TADs **no son historias, son experimentos** (los mismos "pequeños actos de descubrimiento" de `validar-idea-antes-de-construir`). Reducen el riesgo antes de escribir historias.

### Paso 3: Escribe cada historia dividida

Cada división es una historia completa: título, "Como/Quiero/Para" y criterios de aceptación en Gherkin (Dado/Cuando/Entonces). Indica **qué patrón** usaste.

### Paso 4: Valida las divisiones

Pregúntate, para cada una:
1. ¿Entrega **valor al usuario** por sí sola? (no solo "front-end hecho")
2. ¿Se puede desarrollar **de forma independiente**? (sin dependencias duras)
3. ¿Se puede **testear** sola? (criterios claros)
4. ¿Cabe en un sprint? (~1-5 días)
5. ¿La suma de las divisiones **equivale a la original**? (no se pierde nada)

Si alguna respuesta es "no", revisa el corte.

---

## Ejemplo (completo) — Gestión de miembros de un equipo

```markdown
### Historia original (demasiado grande)
Como admin de equipo, quiero gestionar los miembros del equipo para controlar el acceso.
Criterios de aceptación:
- Cuando invito a alguien por email, entonces recibe una invitación para unirse.
- Cuando elimino a un miembro, entonces pierde el acceso de inmediato.
- Cuando cambio el rol de un miembro, entonces sus permisos se actualizan.

→ Tres pares "Cuando/Entonces" ⇒ patrón 4 (complejidad de criterios de aceptación).

### División 1 — Invitar miembros  (patrón 4)
Como admin de equipo, quiero invitar a nuevos miembros por email,
para que puedan empezar a colaborar sin que yo tenga que crearles la cuenta.
- Dado que soy admin, Cuando invito un email válido, Entonces esa persona recibe
  una invitación con enlace para unirse al equipo.
- Dado un email ya invitado, Cuando lo invito otra vez, Entonces el sistema avisa
  de que ya tiene una invitación pendiente.

### División 2 — Eliminar miembros  (patrón 4)
Como admin de equipo, quiero eliminar a un miembro,
para retirar el acceso de quien ya no debe estar.
- Dado un miembro activo, Cuando lo elimino, Entonces pierde el acceso de inmediato
  y deja de aparecer en la lista del equipo.

### División 3 — Cambiar roles  (patrón 4)
Como admin de equipo, quiero cambiar el rol de un miembro,
para ajustar sus permisos sin tener que recrearlo.
- Dado un miembro con rol "lector", Cuando lo cambio a "editor", Entonces puede
  editar el contenido del equipo desde ese momento.

### Validación
Cada división entrega valor, se desarrolla y testea sola, cabe en un sprint, y las
tres juntas cubren la historia original. ✅ Nada se pierde.
```

---

## El Lado Oscuro (antipatrones)

- **El corte horizontal:** "Historia 1: la API. Historia 2: la UI." Ninguna entrega valor sola. Corta **vertical**: cada historia lleva su front + back y una capacidad completa.
- **La sobredivisión:** "añadir el botón" / "conectar el botón" / "mostrar el resultado". Creas sobrecarga y dependencias donde no hacían falta. Una historia de 2 días no se divide.
- **El corte sin sentido:** "primera mitad" / "segunda mitad" de la funcionalidad. Arbitrario. Cada corte debe seguir **uno de los 8 patrones** con una justificación clara.
- **La dependencia dura:** "la Historia 2 no arranca hasta que la 1 esté 100% terminada y desplegada". Mata la paralelización. Divide para permitir trabajo independiente; si la dependencia es inevitable, prioriza y ordénalas.
- **Ignorar el "Para":** todas las divisiones comparten el mismo "para". Has partido la acción pero no el **resultado** → eso es descomposición en tareas, no división de historia. Cada división necesita su propio resultado de usuario.

---

## Frameworks de referencia

- **Richard Lawrence y Peter Green — _The Humanizing Work Guide to Splitting User Stories_** — origen de los 8 patrones de división.
- **Bill Wake — _INVEST in Good Stories_ (2003)** — el estándar de una buena historia (Independiente, Negociable, Valiosa, Estimable, Pequeña, Testable); toda división debe seguir cumpliéndolo.
- **Mike Cohn — _User Stories Applied_ (2004)** — técnicas clásicas de descomposición de historias.
- **Donald Reinertsen — _The Principles of Product Development Flow_ (2009)** — la economía del tamaño de lote pequeño: la razón de fondo por la que dividir acelera y abarata.
- **Corte vertical / walking skeleton** — el principio que conecta esta skill con el `mapa-de-historias-usuario`: rebanadas finas pero completas.

Que la IAgilidad te acompañe.
