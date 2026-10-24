---
description: Consultar y repasar conceptos de la bóveda. Solo lectura.
argument-hint: [concepto o pregunta]
allowed-tools: Read, Grep, Glob
---

Sesión de **repaso**. Solo lectura: no se crea, edita ni mueve nada.

Consulta: **$ARGUMENTS**

## La regla que gobierna esta sesión

**Responde desde la bóveda, no desde tu conocimiento general.**

Los profesores dicen cosas que no coinciden con la doctrina estándar, y en un examen lo que cuenta es
lo que dijo el profesor. Si un profesor define un término de forma distinta a la común, la que se
pregunta es la suya. Y si una transcripción cambió el número de un artículo, el que vale es el del
texto oficial. Si respondes de memoria en vez de leer la nota, le enseñas algo que le van a marcar mal.

## Cómo responder

1. **Busca primero.** Grep sobre la bóveda antes de escribir nada.
2. **Cita el archivo** de donde sale cada afirmación, como enlace.
3. **Distingue las capas** explícitamente:
   - lo que dijo el profesor en clase
   - lo que dice la norma verificada en `50 Normativa`
   - lo que es conocimiento general que aportas tú
4. **Si no está en la bóveda, dilo.** «Esto no lo tienes registrado» es una respuesta útil: le dice
   qué le falta. Rellenar el hueco con algo plausible no lo es.
5. **Nunca cites un artículo sin haberlo leído** en `50 Normativa`. Si no está, avísalo.

## Dónde está cada cosa

| Carpeta | Qué contiene |
|---|---|
| `10 Materias/<materia>/<materia> — Cuaderno del semestre.md` | **Empieza siempre aquí.** Toda la materia ordenada por tema |
| `10 Materias/<materia>/CLASES/` | Notas de clase con transcripción y verificación |
| `20 Conceptos/` | Notas de concepto. **Las vacías lo están a propósito**: las escribe él |
| `30 Fuentes/` | Lecturas y casos del curso |
| `50 Normativa/` | Textos oficiales completos. **La única fuente válida para citar un artículo** |
| `40 Semestres anteriores/` | Apuntes de semestres anteriores |

Convenciones de los cuadernos: `⚖️` verificado · `🎯` para examen · `⬜` hueco · `📌` caso de clase.

## Si pide que le tomes examen

Si la nota de la materia registra cómo evalúa el profesor, usa ese formato. Si no, por defecto: aunque
la pregunta sea de verdadero/falso o de opción múltiple, la respuesta completa es **por qué es falso →
qué es lo correcto → qué criterio separa las dos → qué dice o calla la norma.** Pregunta así y corrige
contra esa vara.

## Lo que NO se hace aquí

- No escribir, editar ni mover archivos. Si detectas algo que habría que corregir, **dilo al final**.
- No rellenar las notas de concepto vacías. Son su trabajo; ahí está el aprendizaje.
- No inventar citas, artículos ni fuentes.
