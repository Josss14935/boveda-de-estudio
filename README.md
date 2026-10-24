# Bóveda de estudio
### Claude Code + Obsidian + NotebookLM

Esqueleto del sistema con el que llevo mi último semestre de Derecho: grabo la clase, NotebookLM la
vuelve interrogable, Claude Code la procesa y la verifica, y en Obsidian queda solo lo que yo pienso.

Viene **vacío**: estructura de carpetas, plantillas, prompts y dos comandos. Tus apuntes los pones tú.

> Hecho por José Serrano (Quito) y compartido en Imperio Agéntico. Está pensado para Derecho, pero
> sirve para cualquier carrera con clases, lecturas y exámenes: más abajo explico qué cambiar.

---

## Cómo funciona

| Capa | Para qué | Regla |
|---|---|---|
| **La plataforma de tu universidad** | Fuente de verdad: syllabus, lecturas, calificaciones | Solo lectura |
| **NotebookLM** | El archivo interrogable. Un cuaderno por materia con el syllabus, las lecturas y los audios de clase | El respaldo completo vive aquí |
| **Obsidian** | Tu pensamiento | Nada entra que no hayas escrito tú, salvo la transcripción en bruto |
| **Claude Code** | Mueve todo: procesa la clase, verifica artículos y fechas, mantiene un cuaderno por materia | Nunca escribe tus definiciones |
| **Calendario o Todoist** (opcional) | El *cuándo*: lecturas, entregas, exámenes | La bóveda guarda el *por qué* |

> Google renombró NotebookLM como **Gemini Notebook** en julio de 2026. Funciona igual; aquí lo sigo
> llamando NotebookLM.

## Qué hay aquí

```
CLAUDE.md                        Las reglas que lee Claude Code al abrir la carpeta
LEEME - Sistema del semestre.md  Cómo funciona todo: capas, rituales y modo mínimo
Prompts NotebookLM.md            El prompt de extracción y cinco más
Deuda.md                         Lo que quedó sin procesar, sin culpa
.claude/commands/
  procesar-clase.md              /procesar-clase: de la extracción a la nota verificada
  repaso.md                      /repaso: preguntas y examen desde tus notas, solo lectura
00 Inbox/                        Donde caen las notas nuevas
10 Materias/                     Una carpeta por materia, con su nota, su cuaderno y CLASES/
20 Conceptos/                    Una nota por concepto. Vacías hasta que las escribas tú
30 Fuentes/                      Fichas de lecturas, casos y jurisprudencia
40 Semestres anteriores/         Lo que ya sabes
50 Normativa/                    Textos oficiales completos: la única fuente para citar un artículo
99 Plantillas/                   Ocho plantillas
```

## Instalación (15 minutos)

1. **Descarga** el repositorio (botón verde **Code → Download ZIP**, o `git clone`) y pon la carpeta
   donde vivirá. Yo la tengo en iCloud para verla en el celular.
2. **Ábrela en Obsidian** como bóveda: *Abrir carpeta como bóveda*.
3. En los **Ajustes de Obsidian**:
   - Complementos principales → activa **Plantillas** → carpeta de plantillas: `99 Plantillas`.
   - Archivos y enlaces → ubicación para notas nuevas: `00 Inbox`.
   - No instales más complementos todavía. Empezar feo es parte del diseño.
4. **Crea un cuaderno en NotebookLM por cada materia** y súbele el syllabus y las lecturas.
5. **Abre Claude Code en la carpeta**, completa la sección «Quién soy» de `CLAUDE.md` y escríbele:
   > Lee CLAUDE.md y el LEEME. Vamos a hacer el ritual de arranque con mis materias.

## Los rituales

- **Arranque (2 horas, una vez):** por materia, su nota con la evaluación y los temas del syllabus, y
  una nota de concepto **vacía** por cada tema prometido. Desde ahí el semestre deja de ser "tomar
  apuntes" y pasa a ser llenar un esqueleto que ya existe.
- **Diario (10 minutos):** en clase, máximo 10 líneas: preguntas, énfasis del profesor y desacuerdos.
  Al salir, el audio a NotebookLM. El mismo día, `/procesar-clase`.
- **Semanal (90 minutos):** 2 a 4 conceptos por materia pasan de vacío a borrador. Se escriben de
  memoria; NotebookLM solo verifica.
- **Modo mínimo:** semana colapsada = grabar, subir y una línea en `Deuda`. Está permitido. El sistema
  tiene que sobrevivir tu peor semana, no lucirse la primera.

## Las cinco reglas que lo hacen funcionar

1. **Nunca "resume la clase".** El prompt de extracción pide 10 categorías y termina con *"si una
   categoría no aparece, escribe ninguno"*. Ese "ninguno" te confirma que **no** hubo anuncio de
   examen; un resumen nunca te dice eso.
2. **El concepto es la unidad, no la clase.** Un mismo concepto aparece en tres materias. Organizado
   por clase, lo escribes tres veces; organizado por concepto, se acumula entre materias y semestres.
3. **Se verifica todo número.** Las transcripciones de audio se equivocan con artículos, fechas y
   nombres. Cada artículo citado se comprueba contra el texto oficial antes de darlo por bueno.
4. **Las definiciones las escribes tú.** Claude crea las notas de concepto vacías y nunca las llena.
   La IA prepara, diagnostica y verifica; no piensa en tu lugar.
5. **Si tu syllabus prohíbe la IA, ahí no se usa.** Lo anotas en `CLAUDE.md` y Claude lo respeta.

## Procesar clases: manual o automático

**Manual (el recomendado):** subes el audio a NotebookLM desde la web, corres el prompt de extracción y
le pasas el resultado a `/procesar-clase`. Claude hace el resto: la nota, la verificación, los
conceptos nuevos y el cuaderno.

**Automático (opcional, bajo tu riesgo):** hay una librería no oficial, `notebooklm-py`, que le deja a
Claude Code subir audios y preguntarle al cuaderno por su cuenta. Usa APIs internas no documentadas de
Google, así que puede romperse sin aviso — a mí se me rompió cuando cambió el dominio — y conviene
usarla con una cuenta de Google dedicada, no con la que guarda tus grabaciones.

## Si no estudias Derecho

- `50 Normativa` pasa a ser tus textos oficiales: normas técnicas, manuales de referencia, guías.
- En `Plantilla - Concepto`, «Fundamento normativo» es la fuente que lo respalda, y «Distinción con
  la figura vecina» sirve para cualquier par de conceptos que se confunden.
- `/repaso` responde **desde tus notas y no desde su conocimiento general**: en un examen cuenta lo que
  dijo tu profesor, no lo que dice internet.

## Lo que no se delega

Escribir las notas de concepto. Los audios y los quizzes de NotebookLM preparan y diagnostican; la
definición sale de tu cabeza o no sirve.

---

## Licencia

[CC BY 4.0](LICENSE): puedes copiarlo, adaptarlo y compartirlo, también con fines comerciales, siempre
que cites a José Serrano como autor original, enlaces la licencia e indiques si hiciste cambios.

Si lo usas o lo mejoras, cuéntamelo en Imperio Agéntico.
