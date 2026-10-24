---
description: Procesar una clase grabada, de la extracción de NotebookLM a la nota verificada y el cuaderno al día.
argument-hint: [materia] [fecha AAAA-MM-DD] — y pega la extracción de NotebookLM
---

Procesa la clase de **$ARGUMENTS**, siguiendo la «Regla al procesar una clase» de `CLAUDE.md`.

1. **Busca la nota.** Lista `10 Materias/<materia>/CLASES/`. Si ya hay una nota de esa fecha, se llame
   como se llame, editas esa. Si no, la creas desde `99 Plantillas/Plantilla - Clase.md`.
2. **La extracción.** Si el estudiante pegó la salida del prompt 1 de `Prompts NotebookLM.md`, va tal
   cual a «Transcripción (NotebookLM)». Si no la pegó, pídesela. No la inventes ni transcribas en local.
3. **Verifica.** Cada artículo, norma, fecha de evaluación, cifra y nombre propio de la extracción,
   contra `50 Normativa`, el syllabus o el documento oficial. El resultado va a la tabla
   «⚠️ Verificación»: ✅ coincide · ⚠️ corregido (con lo correcto) · ⬜ no se pudo comprobar.
4. **Conceptos.** Los de la categoría 8 que todavía no tengan nota se crean **vacíos** en
   `20 Conceptos/` desde la plantilla y se enlazan en «Conceptos». No se escribe ninguna definición.
5. **Pendientes.** Los de la categoría 10 y los anuncios de la 6 van a «Pendientes de esta clase». Si
   hay un calendario o Todoist conectado, propón las fechas; no las crees sin permiso.
6. **Cuaderno.** Integra lo nuevo en el cuaderno de la materia, en la sección de su tema (no al final
   por fecha), con `⚖️` `🎯` `⬜` `📌`. Añade una fila al registro.
7. **No toques** «Apuntes en clase» ni «En una frase».

Cierra con cinco líneas: qué nota tocaste, qué se corrigió al verificar, qué conceptos nuevos hay y qué
quedó pendiente.
