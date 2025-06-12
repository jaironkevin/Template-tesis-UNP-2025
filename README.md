# Plantilla para tesis UNP con R, RStudio y Quarto

Esta plantilla está diseñada para facilitar la redacción de tesis de pregrado siguiendo los estándares establecidos por la Universidad Nacional de Piura (UNP), Perú. Ha sido desarrollada usando **Quarto**, **R** y **RStudio**, generando una salida profesional en formato **PDF** utilizando el motor `xelatex`.

El documento se realiza en el contexto de la tesis **“MODELO SARIMA Y RED NEURONAL RECURRENTE PARA ELPRONOSTICO DE LA PRODUCCIÓN DE MANGO EN EL VALLE DESAN LORENZO, 2024-2026”**, en la facultad de Ciencias, escuela Profesional de estadística.

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

## Estructura del Documento

Este proyecto de tesis está estructurado conforme a los estándares académicos exigidos por la universidad. La generación del documento se realiza en **RStudio** utilizando **Quarto**, con salida en PDF compilada mediante el motor **xelatex**. A continuación, se detalla la organización de los contenidos:

## 1. `\frontmatter`

Contiene los elementos preliminares, sin numeración de capítulos:

- **Portada**: `0_Portada.qmd`
- **Firmas de ejecutores**: `01_Firmas_ejecutores.qmd`
- **Declaración jurada**: `02_DJ1.qmd`
- **Firmas del jurado**: `04_Firmas_jurado.qmd`
- **Actas de sustentación**: `05_Acta_sustentacion1.qmd`, `05_Acta_sustentacion2.qmd`
- **Dedicatoria**: `1_Dedicatoria.qmd`
- **Agradecimientos**: `2_Agradecimientos.qmd`
- **Índice general**: `\tableofcontents`
- **Índice de tablas**: `\listoftables`
- **Índice de figuras**: `\listoffigures`
- **Resumen**: `3_Resumen.qmd`
- **Abstract (en inglés)**: `4_Abstract.qmd`

## 2. `\mainmatter`

Corresponde al contenido principal del trabajo. A partir de aquí se numeran los capítulos:

- **Capítulo 0: Introducción** (`Cap0_Introduccion.qmd`)
- **Capítulo 1: Aspectos de la problemática** (`Cap1_Aspectos_de_la_problematica.qmd`)
- **Capítulo 2: Marco teórico** (`Cap2_Marco_teorico.qmd`)
- **Capítulo 3: Marco metodológico** (`Cap3_Marco_metodologico.qmd`)
- **Capítulo 4: Resultados y discusión** (`Cap4_Resultados_y_discusion.qmd`)
- **Conclusiones**: `Conclusiones.qmd`
- **Recomendaciones**: `Recomendaciones.qmd`

*Nota:* Se incluyen comandos LaTeX como `\addtocontents{lof}{\protect\vspace{-2ex}}` para ajustar el espaciado en los índices de tablas y figuras.

## 3. `\appendix`

Sección de apéndices, útil para incluir anexos, cuestionarios, material complementario, cálculos extensos, etc.

## 4. `\backmatter`

Sección final del documento:

- **Referencias bibliográficas**: `Referencias_bibliograficas.qmd`
- **Anexos**: `Z_Anexos.qmd`


## Requisitos
- [R](https://www.r-project.org/) (versión reciente)
- [RStudio](https://posit.co/download/rstudio-desktop/)
- [Quarto](https://quarto.org/docs/get-started/)
- Una distribución de LaTeX:
  - Se recomienda [TinyTeX](https://yihui.org/tinytex/) o TeXLive
  - **Debe incluir el motor `xelatex`** para la correcta compilación del PDF
- Paquetes adicionales de LaTeX definidos en el archivo `Preamble.tex`


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
**Créditos**

Plantilla elaborada por Jairon Ojeda para la elaboración profesional de tesis en la UNP, optimizada para su uso con RStudio y Quarto. Aporta control total sobre estilo, formato, citación y estructura tipográfica exigida por la universidad.
