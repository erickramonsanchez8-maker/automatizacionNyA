# Automatización NyA

Herramienta para convertir reportes de ventas de mostrador en el concentrado de folios solicitado.

## Publicar con GitHub Pages

En el repositorio, abre **Settings → Pages**. En **Build and deployment**, selecciona **Deploy from a branch**. En **Branch**, elige `main` y la carpeta `/(root)`, y pulsa **Save**. GitHub publicará `index.html` y la carpeta `vendor`.

Dirección prevista: https://erickramonsanchez8-maker.github.io/automatizacionNyA/

## Uso

1. Abre la página publicada.
2. Selecciona el reporte original `.xls`, `.xlsx` o `.csv`, o arrástralo al área de carga.
3. Revisa fecha, cantidad de documentos, total e importe neto.
4. Pulsa **Descargar Excel formateado**.

El procesamiento se realiza en el navegador. Los archivos no se envían a un servidor. El lector de Excel está incluido localmente en `vendor/xlsx.full.min.js`, por lo que no depende de un CDN.

## Formato de salida

El libro generado conserva la estructura de referencia: fecha en `B1`, folios en la columna `B`, importes en la columna `C`, total de documentos y suma, y cálculo final de `Total / 1.16`. El importe neto real del reporte se muestra aparte en la página, ya que puede diferir cuando existen ventas exentas o tasas distintas.
