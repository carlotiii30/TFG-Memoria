# Memoria del TFG

Este repositorio contiene la memoria del Trabajo de Fin de Grado (TFG). La memoria está escrita en **LaTeX** para garantizar una alta calidad tipográfica y facilitar la gestión de referencias, índices y otros elementos formales.

## Estructura del repositorio

- `memoria.tex`: Archivo principal de la memoria.
- `capitulos/`: Carpeta que contiene los capítulos de la memoria divididos en archivos `.tex`.
- `imagenes/`: Imágenes utilizadas en la memoria.
- `bibliografia.bib`: Archivo con las referencias bibliográficas.
- Otros archivos auxiliares de configuración LaTeX.

## Requisitos previos

Para compilar la memoria necesitas tener instalado:

- **LaTeX** (TeX Live, MikTeX, o similar)
- Un editor de texto recomendado: [TeXstudio](https://www.texstudio.org/), [Overleaf](https://www.overleaf.com/) (online), [VSCode](https://code.visualstudio.com/) con la extensión LaTeX Workshop, etc.

En sistemas basados en Debian/Ubuntu puedes instalar LaTeX con:

```bash
sudo apt update
sudo apt install texlive-full
```

## Compilación de la memoria

Para generar el PDF de la memoria sigue estos pasos desde la raíz del repositorio:

### Compilación manual

1. Ejecuta el siguiente comando:

    ```bash
    pdflatex memoria.tex
    bibtex memoria
    pdflatex memoria.tex
    pdflatex memoria.tex
    ```

   Esto generará un archivo `memoria.pdf` en el directorio actual.

### Compilación automática

También puedes usar el comando `latexmk` (incluido en `texlive-full`):

```bash
latexmk -pdf memoria.tex
```

Esto hará todo el proceso automáticamente y generará el PDF final.

## Notas

- Si añades nuevas imágenes, colócalas en la carpeta `imagenes/`.
- Si añades nuevos capítulos, agrégalos en la carpeta `capitulos/` y enlázalos desde `memoria.tex`.
- Las referencias bibliográficas se gestionan en el archivo `bibliografia.bib` y se citan en el texto usando `\cite{}`.

## Licencia

Este material tiene como objetivo servir de referencia para la elaboración de memorias académicas. Consulta la licencia específica en este repositorio para más detalles.
