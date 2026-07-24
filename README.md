# Seminario de Tecnologías de la Información

Repositorio con el documento LaTeX del ensayo **"Diseño de encuestas efectivas para la obtención de datos de calidad"**.

## Estructura del proyecto

- `Foro-academico-1/encuestas_de_calidad.tex`: archivo principal del documento.
- `Foro-academico-1/references.bib`: base de datos bibliográfica utilizada por `biblatex`.
- `Foro-academico-1/encuestas_de_calidad.pdf`: versión compilada del documento.

## Requisitos

Para compilar el archivo se necesita:

- Una distribución LaTeX: `TeX Live`, `MiKTeX` o similar.
- `pdflatex`
- `biber`
- Opcionalmente `latexmk`, para automatizar la compilación.

El documento usa:

- `babel` con idioma español
- `biblatex` con `backend=biber`
- `hyperref`
- `geometry`
- `titlesec`
- `setspace`

## Cómo compilar

### Opción recomendada: `latexmk`

Desde la carpeta `Foro-academico-1`:

```bash
latexmk -pdf -interaction=nonstopmode -synctex=1 encuestas_de_calidad.tex
```

Si quieres limpiar archivos auxiliares después de compilar:

```bash
latexmk -c
```

### Opción manual

Desde la carpeta `Foro-academico-1`:

```bash
pdflatex encuestas_de_calidad.tex
biber encuestas_de_calidad
pdflatex encuestas_de_calidad.tex
pdflatex encuestas_de_calidad.tex
```

## Resultado esperado

Al finalizar, se genera:

- `encuestas_de_calidad.pdf`

También pueden aparecer archivos auxiliares como:

- `.aux`
- `.bbl`
- `.bcf`
- `.blg`
- `.log`
- `.out`
- `.toc`

## Notas

- El archivo principal asume que `references.bib` está en la misma carpeta.
- Si cambias el nombre del `.tex`, recuerda ajustar también los comandos de compilación.
