---
tipo: control
---

# Prompts para NotebookLM

## Regla de oro

Un cuaderno **por materia**, no uno global. Fuentes de cada cuaderno: syllabus + lecturas asignadas +
audios de clase de esa materia. Un cuaderno único mezcla materias y las respuestas se contaminan.

Para los controles de lectura, un cuaderno **aparte** con solo las lecturas evaluadas: así los audios y
los quizzes salen centrados y no se contaminan con las clases.

## Antes de nada: dónde NO se puede usar

Lee el apartado de IA de cada syllabus. Si una materia la prohíbe, anótalo en `CLAUDE.md` y respétalo:
ahí no se sube nada. Lo que arriesga una sanción académica es el trabajo evaluado.

## Los audios no entran a la bóveda

Los resúmenes en audio **se quedan en NotebookLM y se escuchan desde ahí**. Pesan decenas de MB y la
bóveda se sincroniza a todos tus dispositivos. En la bóveda queda solo la anotación de que existen.

---

## 1. Extracción dirigida (el prompt diario)

> Úsalo SIEMPRE en lugar de "resume la clase".

```
De la clase X extrae, únicamente si aparece de forma explícita:

1. Puntos donde el profesor enfatizó, repitió o dijo que es importante
2. Correcciones o matices que hizo a la lectura asignada
3. Distinciones entre figuras (X vs. Y) y el criterio que usó para distinguirlas
4. Artículos, normas, fallos o autores citados — textualmente
5. Ejemplos concretos que dio
6. Anuncios sobre evaluación, entregas, fechas o alcance del examen
7. Preguntas de compañeros y cómo las respondió
8. Inventario completo de figuras, instituciones y conceptos nombrados en la clase,
   filtrando por importancia. Lista plana, incluye los mencionados de paso o sin
   desarrollo. Ante la duda, inclúyelo.
9. En base a las demás fuentes añade datos relevantes relacionados a la clase a modo de
   bulletpoints. Y en caso de no estar seguro, genera preguntas; recuerda indicar de qué
   fuente y qué parte de la fuente extraes el contenido, en caso de que se deba comprobar.
10. Pendientes para la siguiente clase: leer alguna lectura, estudiar para un examen, etc.

Cita y explícalos en caso de ser necesario. Si una categoría no aparece, escribe "ninguno".
```

El "ninguno" es la parte útil: te confirma la ausencia. Un resumen narrativo nunca te dice que *no*
hubo anuncio de examen.

**Lo que da cada categoría nueva:**
- **La 8, el inventario.** Convierte la transcripción en trabajo de bóveda: de ahí salen las notas de
  concepto nuevas, incluso las que no estaban en el syllabus.
- **La 9, el cruce con las demás fuentes.** Verifica contra el syllabus y las lecturas, y deja el
  rastro de dónde sale cada dato.
- **La 10, los pendientes.** Hace que la nota siga sirviendo después de la clase.

**Advertencia:** la transcripción puede equivocarse con fechas, cifras y nombres propios. Lo que venga
del audio se comprueba contra el documento oficial antes de darlo por bueno.

---

## 2. Verificación de una nota de concepto

```
Según las fuentes de este cuaderno, ¿qué se dijo sobre [CONCEPTO]?
Indica la clase o lectura de origen. Si hubo definiciones distintas
entre la lectura y la clase, señala la diferencia explícitamente.
```

## 3. Rastreo transversal (antes de un examen)

```
¿En qué clases apareció [CONCEPTO] y cómo evolucionó su tratamiento
a lo largo del curso?
```

## 4. Generación de preguntas (dos semanas antes)

```
A partir del syllabus y las clases de la unidad [N], genera 15 preguntas
de examen al nivel de exigencia de la materia: aplicación a casos y
distinción entre figuras, no definiciones memorísticas.
No incluyas las respuestas.
```

Respóndelas **de memoria** y solo después abre las notas de concepto.

## 5. Detección de huecos

```
Lista los temas del syllabus que aparecen poco o nada desarrollados
en los audios de clase de este cuaderno.
```

Esos temas suelen ser "lectura autónoma evaluable". Son la trampa clásica.

## 6. Preparación de un control de lectura

```
De las lecturas asignadas al control [N] extrae:

1. La tesis de cada autor en una frase, indicando de quién es cada una.
2. Todos los nombres propios con su dato verificable al lado: ciudad, año, país, número
   de instrumento, número de ley.
3. Las distinciones entre figuras que aparezcan, con su criterio.
4. Diez afirmaciones textuales que podrían convertirse en pregunta de sí o no.

No parafrasees en el punto 4: cita.
```

Con eso se llena `Plantilla - Control de lectura`. La columna de "versión falsa" la escribes tú: es lo
que te hace reconocer la trampa.

### La receta que funcionó para los controles

1. **Dos días antes**, subir las lecturas del control a su cuaderno.
2. Un **resumen en audio por lectura**, para escuchar en el transporte: es tiempo que no competía con
   nada.
3. Un **quiz**, respondido de memoria. El audio fija; el quiz detecta lo que no quedó.
4. **El día antes**, la nota del control: tesis por autor, datos duros y la tabla de "lo que dice el
   texto / la versión falsa".
5. Lo que falles se corrige **en la nota de concepto**, no en la del control.

---

## Lo que NO se le pide a NotebookLM

- Que escriba tus notas de concepto. Eso lo escribes tú o no sirve.
- Opinión jurídica o interpretación propia.
- Verificar si una norma está vigente. Para eso vas al texto oficial.
- Nada de las materias donde el syllabus prohíbe la IA.
