# smartfarming

Tablero público de relaciones de precios (hacienda, insumos agrícolas, labores, tierra) de SF-07 Mercados, publicado con GitHub Pages: https://pacetta.github.io/smartfarming/

## Cómo se actualiza

El HTML es autocontenido (no tiene build ni dependencias): es la salida directa de un generador en R/Quarto que lee la hoja "Datos Base" del Excel madre y la vuelca en `index.html`.

1. Cargar el mes nuevo en "Datos Base" del Excel, guardar y cerrar.
2. En RStudio, abrir `rel_precios_tabla_public.qmd` (carpeta `Tableros/rel_precios/` de la base de datos) y hacer Render. Genera `index.html` directo en esta carpeta.
3. Correr `publicar.ps1` (en esta carpeta) para subir el cambio a GitHub.

A diferencia del tablero interno (`rel_precios_tabla.qmd`), esta versión solo incluye las ~19 series de precios que el tablero realmente muestra — no toda la hoja "Datos Base" — porque el repo es público.
