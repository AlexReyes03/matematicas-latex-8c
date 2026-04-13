# matematicas-latex-8c

Repositorio LaTeX del proyecto integrador de **Matemáticas para Ingeniería II** (grupo **8 C** en portada y metadatos). El documento maestro es `matematicas_ingenieria.tex`; la estructura replica la del cuatrimestre anterior (`matematicas_ingenieria_anterior.tex`): mismos paquetes, portada, índices y capítulos por unidad.

## Cómo compilar

Compila `matematicas_ingenieria.tex` con un motor que soporte `inputenc`/`babel` (por ejemplo **pdfLaTeX**). Asegúrate de que existan los logos referenciados en la portada:

- `img/logo-utez.png`
- `img/logo-datid.png`

## Estructura del documento maestro

Orden fijo del archivo (convención del equipo; al añadir avances, respétalo para que los merges y revisiones sean predecibles).

| Bloque | Comentario en el `.tex` | Contenido |
|--------|-------------------------|-----------|
| Preámbulo | `PAQUETES`, `CONFIGURACIONES` | `report` 12pt, `letterpaper`, matemáticas, figuras, hipervínculos, encabezados, numeración de ecuaciones/figuras/tablas por capítulo. |
| Metadatos | `INFORMACIÓN DEL DOCUMENTO` | `\title`, `\author`, `\date{\today}` (fecha autogenerada al compilar). |
| Portada | `PORTADA` | Logos UTEZ / DATID, datos de carrera, título del integrador, materia, profesor, **grupo**, lista de integrantes, ciudad y **`\today`**. |
| Índices | `ÍNDICES` | `\tableofcontents`, `\listoffigures` y `\cleardoublepage` entre ellos (igual que el archivo anterior). |
| **Unidad I** | `UNIDAD I` | Primer `\chapter{Unidad I}`. **Aquí empieza el trabajo de la Unidad 1.** |
| **Unidad II** | `UNIDAD II` | Segundo `\chapter{Unidad II}`. **Aquí empieza el trabajo de la Unidad 2.** |
| **Unidad III** | `UNIDAD III` | Tercer `\chapter{Unidad III}`. **Aquí empieza la Unidad 3** (reservada; dejar en blanco hasta que quien la cubra agregue contenido). |
| Referencias | `REFERENCIAS` | `thebibliography`; usar `\bibitem{clave}` y citar con `\cite{clave}`. |

Los títulos `\chapter{Unidad I}` (etc.) son genéricos: cuando el temario esté cerrado, renómbralos por ejemplo a `\chapter{Unidad I: Ecuaciones diferenciales}` sin mover el bloque de comentarios que delimita cada unidad.

## Convenciones al implementar avances

1. **Secciones:** dentro de cada capítulo, usa `\section{}`, `\subsection{}`, `\subsubsection{}` como en el documento anterior.
2. **Ecuaciones:** entornos `equation`, `align`, etc.; etiquetas `\label{eq:...}` y referencias `\eqref{eq:...}`.
3. **Figuras:** carpeta `img/`; `\includegraphics` con rutas relativas al `.tex`; `\caption` y `\label{fig:...}`.
4. **Referencias bibliográficas:** solo en el bloque final; no mezclar estilos arbitrarios (mantener formato tipo `thebibliography` del ejemplo anterior salvo que el curso pida otro).
5. **Unidad III:** no añadir texto en ese capítulo si no es tu responsabilidad; coordina con el integrante asignado antes de modificar ese bloque.

## Material auxiliar en el repo

Archivos como `ejercicios_unidad1.md` y `ejercicios_unidad2.md` son apuntes en Markdown (bien legibles para revisión o para asistir a la redacción en LaTeX); no sustituyen al PDF final del integrador.

## Archivo de referencia (cuatrimestre pasado)

`matematicas_ingenieria_anterior.tex` sirve como referencia de **estilo y extensión** de secciones; no copiar su contenido académico al documento nuevo, solo la estructura y buenas prácticas que necesites.
