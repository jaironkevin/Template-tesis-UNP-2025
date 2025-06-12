# Plantilla para tesis UNP con R, RStudio y Quarto

Esta plantilla está diseñada para facilitar la redacción de tesis de pregrado siguiendo los estándares establecidos por la Universidad Nacional de Piura (UNP), Perú. Ha sido desarrollada usando **Quarto**, **R** y **RStudio**, generando una salida profesional en formato **PDF** utilizando el motor `xelatex`.

## Características principales

- **Formato académico estilo UNP**:
  - Tamaño de papel A4 con márgenes personalizados según reglamento.
  - Interlineado de 1.5 líneas y sangría de 1.27 cm.
  - Tipografía oficial: *Times New Roman*.
  - Numeración de capítulos en romanos y secciones/subsecciones en arábigos.

- **Control total del diseño LaTeX** mediante un archivo `Preamble.tex`:
  - Personalización de encabezados, pies de página y numeración.
  - Estilo para títulos de capítulos, secciones y subsecciones.
  - Índices de contenido, tablas y figuras con títulos centrados y formato modificado.
  - Numeración corrida de figuras y tablas a lo largo del documento.
  - Capítulos con títulos en formato "CAPÍTULO I: Introducción", entre otros.

- **Compatibilidad con bibliografía y citación**:
  - Soporte para `biblatex` y estilo de citación APA con archivo `.bib` y `.csl`.

- **Estilo visual profesional**:
  - Posicionamiento fijo de figuras y tablas (`fig-pos: "H"`).
  - Títulos de figuras y tablas en parte superior, con estilo APA modificado.
  - Notas al pie de figuras/tablas usando comando personalizado `\pie{}`.

## Requisitos

- R (versión reciente)
- RStudio
- Quarto
- LaTeX (se recomienda TinyTeX o TeXLive)
- Paquetes adicionales de LaTeX definidos en `Preamble.tex`

## Archivos principales

- `index.qmd`: documento principal de la tesis.
- `Preamble.tex`: contiene toda la personalización avanzada en LaTeX.
- `references.bib`: base de datos de referencias.
- `apa.csl`: estilo de citación APA 7.
- `sections.qmd`: contiene las secciones del cuerpo de la tesis, organizadas modularmente.

## Ejemplo de cabecera en `index.qmd`

```yaml
title: "Mi Tesis"
subtitle: "Para graduarme"
author: "Jairon Ojeda"
date: "2024/12/31"
format:
  pdf:
    pdf-engine: xelatex
    citation-package: biblatex
    keep-tex: true
    documentclass: book
    classoption: oneside
    number-sections: true
    toc: false
    lang: es
    geometry: "paperwidth=210mm, paperheight=297mm, left=3cm, right=2.5cm, top=2.5cm, bottom=2.5cm"
    fig-pos: "H"
execute:
  echo: false
  warning: false
fig-cap-location: top
include-in-header: Preamble.tex
bibliography: references.bib
csl: apa.csl
link-citations: true
```
Créditos
Plantilla elaborada por Jairon Ojeda para la elaboración profesional de tesis en la UNP, optimizada para su uso con RStudio y Quarto. Aporta control total sobre estilo, formato, citación y estructura tipográfica exigida por la universidad.
