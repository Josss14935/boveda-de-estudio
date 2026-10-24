# CLAUDE.md — Bóveda de estudio

Este archivo lo lee Claude Code cada vez que se abre esta carpeta. Es el contrato de trabajo: qué es
la bóveda, qué se toca y qué no.

## Quién soy
<!-- Completa estas líneas antes de la primera sesión -->
- Nombre:
- Carrera y semestre:
- Materias de este semestre:
- Materias donde el syllabus **prohíbe usar IA** (ninguna, o cuáles):

## Al iniciar una sesión
1. Leer `LEEME - Sistema del semestre.md` y `Deuda.md`.
2. Leer el cuaderno de la materia de la que se va a hablar:
   `10 Materias/<materia>/<materia> — Cuaderno del semestre.md`.
3. Confirmar en pocas líneas qué hay pendiente y cuáles son los próximos vencimientos.

## Las capas
- **La plataforma de la universidad** es la fuente de verdad. Solo lectura.
- **NotebookLM** es el archivo interrogable: un cuaderno por materia.
- **Obsidian** es el pensamiento del estudiante. Nada entra que no haya escrito él, salvo la
  transcripción en bruto.

## Lo que nunca se toca
- En las notas de clase, las secciones que escribe el estudiante: **«Apuntes en clase»** y
  **«En una frase»**.
- Las **definiciones de `20 Conceptos/`**. Cuando aparece un concepto nuevo, se crea su nota **vacía**
  desde `99 Plantillas/Plantilla - Concepto.md` y se enlaza. Nada más.
- Cualquier texto que haya escrito el estudiante: no se reescribe, no se resume, no se corrige. Si
  hay un error, se le dice.
- Nada se borra de la bóveda.

## Regla al procesar una clase
1. Listar `10 Materias/<materia>/CLASES/` y comprobar si ya existe una nota de esa fecha, **se llame
   como se llame**: el estudiante suele crearla durante la clase.
2. Si existe, se edita esa; nunca se crea una paralela. Si no existe, se crea desde
   `99 Plantillas/Plantilla - Clase.md` con el nombre `N. AAAA-MM-DD — <Materia> — <Tema>.md`.
3. Se rellenan la transcripción (la extracción de 10 categorías), los enlaces a conceptos, la tabla
   **⚠️ Verificación** y los **pendientes**.
4. Se actualiza el cuaderno de la materia y su registro al pie.

El paso a paso está en `/procesar-clase`.

## Regla al citar
Toda cita que entre a un trabajo del estudiante (ensayo, tesis, ficha) se verifica al 100 % antes de
escribirla. Verificada significa las cuatro cosas a la vez:
1. **Existe.** Autor, obra, año y editorial o revista son reales y coinciden entre sí.
2. **Está donde se dice.** La página, el artículo o el párrafo contienen eso: se abre y se mira.
3. **Dice eso.** Entre comillas, es literal. Si es paráfrasis, no se le hace decir al autor más de lo
   que dijo.
4. **Lleva su rastro.** Enlace, DOI o ruta al PDF junto a la cita.

Si una falla, la cita no entra: se marca ⬜ «no verificada» con lo que falta. Una cita plausible pero
no comprobada vale menos que un hueco declarado. Si la verificación se vuelve un bucle, se corta y se
reporta el hueco; no se rellena con una fuente parecida.

## Verificar artículos y fechas
Las transcripciones de audio fallan con los números: cambian un artículo por otro, parten artículos y
destrozan nombres. Todo artículo citado en clase se comprueba contra `50 Normativa` y se marca ⚖️ en
el cuaderno. Las fechas de evaluación, contra el syllabus. Si algo no está en la bóveda, se avisa: no
se cita de memoria.

## Los cuadernos del semestre
Uno por materia, en `10 Materias/<materia>/`, ordenado **por tema y no por fecha**, para estudiar
antes de un examen sin saltar de nota en nota. Los mantiene Claude: cada clase procesada o material
nuevo se integra en su tema y queda una fila en el registro al pie. El estudiante no los edita a mano,
para que no convivan dos versiones; si algo está mal, lo dice y se corrige.

Convenciones: `⚖️` artículo verificado · `🎯` marcado para examen · `⬜` hueco pendiente ·
`📌` caso o ejemplo de clase.

## NotebookLM
- Un cuaderno por materia. Nunca uno global: mezcla materias y contamina las respuestas.
- Los audios que genera (los podcasts) no se guardan en la bóveda: pesan mucho. Solo se anota que
  existen y cómo se llaman.
- Si NotebookLM no está disponible, se dice de entrada. **No se transcribe en local** (Whisper u otro)
  sin permiso del estudiante: cuesta mucho tiempo y muchos tokens.
- En las materias donde el syllabus prohíbe la IA, se hace lo que el estudiante haya decidido arriba.
  Nunca se le escribe un trabajo evaluado de esas materias.

## Antes de borrar una lectura del computador
Sus conceptos tienen que estar en la bóveda: ficha en `30 Fuentes/` con la referencia completa, notas
de lectura escritas y los conceptos enlazados. Sin preguntar solo se puede mandar a la papelera lo que
es un duplicado exacto o una versión superada de una norma. Nunca se borra para siempre.
