---
tipo: control
---

# Sistema del semestre — cómo funciona

## Las tres capas

| Capa | Función | Regla |
|---|---|---|
| Plataforma de la clase | Fuente de verdad | Solo lectura. No se toca. |
| NotebookLM | Archivo interrogable | El respaldo completo vive aquí. Un cuaderno por materia. |
| Obsidian | Tu pensamiento | Nada entra que no hayas escrito tú (salvo la transcripción en bruto). |

**"Que no se pase nada" ya está resuelto por la grabación.** La bóveda no es el archivo; es el
índice de lo que necesitas encontrar rápido. Volumen indiscriminado no es completitud: un documento
que nunca abres se pasa más cosas que uno corto que sí lees.

---

## Ritual diario (10 min)

1. **En clase:** abres la nota desde `Plantilla - Clase` y escribes en «Apuntes en clase», **máximo
   10 líneas**. Solo preguntas, énfasis del profesor y desacuerdos. No transcribas: estás grabando.
2. **Al salir:** el audio al cuaderno de la materia en NotebookLM. Fin.
3. **El mismo día:**
   - «En una frase», **de memoria**, antes de abrir nada. Veinte segundos: ¿qué se resolvió hoy? Si
     no te sale, la clase quedó floja.
   - «Conceptos»: primero los que recuerdes.
   - Corres el prompt de extracción (`Prompts NotebookLM`, prompt 1) y le pasas la salida a Claude
     con `/procesar-clase`.
   - Comparas lo que recordabas con lo que salió. **Esa brecha es el aprendizaje real.**

Si un día no haces el paso 3, lo anotas en [[Deuda]] y sigues. Sin culpa.

---

## Ritual semanal (90 min, anclado al fin de semana)

- 2 a 4 conceptos por materia pasan de vacío a borrador o consolidado.
- Se escriben **de memoria primero**; NotebookLM solo verifica (prompt 2).
- Se revisa [[Deuda]] y se aplica su regla de purga.

---

## Ritual de arranque (2 horas, al empezar el semestre)

Por cada materia:
1. Carpeta `10 Materias/<materia>/` con su subcarpeta `CLASES/`.
2. Nota de la materia desde `Plantilla - Materia`: la evaluación con fechas y la lista de temas del
   syllabus.
3. Una nota de concepto **vacía** por cada tema prometido, en `20 Conceptos/`.
4. El cuaderno, desde `Plantilla - Cuaderno del semestre`. Lo llena Claude.

Después de esto el semestre deja de ser "tomar apuntes" y pasa a ser llenar un esqueleto que ya
existe. Sabes en todo momento cuánto te falta.

---

## Por qué los conceptos se guardan aparte de las clases

La unidad atómica es el **concepto**, no la sesión. Un mismo concepto aparece en varias materias.
Organizado por clase, lo escribes tres veces y ninguna se conecta. Organizado por concepto, tus notas
se acumulan entre materias, entre semestres y en tu trabajo.

Las notas de clase son **fugaces**: sirven una semana. Las notas de concepto son **permanentes**: las
vas a abrir en el examen final, en el siguiente semestre y en el ejercicio profesional.

---

## Los cuadernos — la cuarta capa

**Un cuaderno por materia**: un solo documento con todo lo visto, **ordenado por tema y no por
fecha**, para estudiar antes de un examen sin saltar de nota en nota.

**Los mantiene Claude**, no tú. Cada vez que se procesa una clase o llega material nuevo, el cuaderno
se actualiza y queda constancia en su registro al pie. Si algo está mal, se lo dices y lo corrige; no
se editan a mano, para que no convivan dos versiones.

**Qué NO son.** No sustituyen tus apuntes en vivo ni tus notas de concepto. El cuaderno es el
**repaso**; la brecha se trabaja en la nota de cada clase, y la definición de cada concepto la sigues
escribiendo tú.

Convenciones: `⚖️` artículo verificado · `🎯` marcado para examen · `⬜` hueco pendiente ·
`📌` caso o ejemplo de clase.

---

## Modo mínimo

Semana colapsada = grabar + subir a NotebookLM + una línea en [[Deuda]].
Está permitido y está diseñado. El sistema tiene que sobrevivir tu peor semana, no lucirse en la
primera.

---

## Antes de borrar una lectura

Un PDF que se borra sin haber dejado nada detrás es conocimiento perdido. Antes de eliminarlo:
1. Ficha en `30 Fuentes/` con la referencia completa, para poder citarlo sin el archivo.
2. Notas de lectura escritas, no la ficha vacía.
3. Los conceptos que desarrolla, enlazados y creados aunque estén vacíos.

---

## Revisión de mitad de semestre

Responder tres preguntas con datos, no con sensación:
- ¿Cuántas clases quedaron sin procesar? (contar en [[Deuda]])
- ¿Cuántos conceptos siguen vacíos frente al total del syllabus?
- ¿Qué sección de la plantilla nunca llenas? → elimínala.
