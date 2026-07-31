# Seminario de Tecnologías de la Información

Repositorio con los documentos LaTeX desarrollados para los foros académicos del curso.

## Estructura del proyecto

### Foro académico 1

**Diseño de encuestas efectivas para la obtención de datos de calidad**

- [`encuestas_de_calidad.tex`](Foro-academico-1/encuestas_de_calidad.tex): archivo fuente principal.
- [`references.bib`](Foro-academico-1/references.bib): referencias bibliográficas.
- [`encuestas_de_calidad.pdf`](Foro-academico-1/encuestas_de_calidad.pdf): documento compilado.

### Foro académico 2

**Diseño y buenas prácticas para el desarrollo de aplicaciones reactivas basadas en el Manifiesto Reactivo**

- [`disenio-reactivo.tex`](Foro-academico-2/disenio-reactivo.tex): archivo fuente principal.
- [`references.bib`](Foro-academico-2/references.bib): referencias bibliográficas.
- [`disenio-reactivo.pdf`](Foro-academico-2/disenio-reactivo.pdf): documento compilado.

## Requisitos

Para compilar los documentos se necesita:

- Una distribución LaTeX: `TeX Live`, `MiKTeX` o similar.
- `pdflatex`
- `biber`
- Opcionalmente `latexmk`, para automatizar la compilación.

Los documentos usan:

- `babel` con idioma español
- `biblatex` con `backend=biber`
- `hyperref`
- `geometry`
- `titlesec`
- `setspace`

## Cómo compilar

### Opción recomendada: `latexmk`

Ubícate en la carpeta del foro que quieras compilar y ejecuta `latexmk` con el nombre de su archivo principal.

Para el Foro académico 1:

```bash
cd Foro-academico-1
latexmk -pdf -interaction=nonstopmode -synctex=1 encuestas_de_calidad.tex
```

Para el Foro académico 2:

```bash
cd Foro-academico-2
latexmk -pdf -interaction=nonstopmode -synctex=1 disenio-reactivo.tex
```

Si quieres limpiar archivos auxiliares después de compilar:

```bash
latexmk -c
```

### Opción manual

Desde la carpeta correspondiente, sustituye `<documento>` por `encuestas_de_calidad` o `disenio-reactivo`:

```bash
pdflatex <documento>.tex
biber <documento>
pdflatex <documento>.tex
pdflatex <documento>.tex
```

## Resultado esperado

Al finalizar, se genera el PDF correspondiente:

- `Foro-academico-1/encuestas_de_calidad.pdf`
- `Foro-academico-2/disenio-reactivo.pdf`

También pueden aparecer archivos auxiliares como:

- `.aux`
- `.bbl`
- `.bcf`
- `.blg`
- `.log`
- `.out`
- `.toc`

## Notas

- Cada archivo principal asume que `references.bib` está en la misma carpeta.
- Si cambias el nombre del `.tex`, recuerda ajustar también los comandos de compilación.
