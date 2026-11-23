# Verificar la integridad de la descarga

Antes de instalar, comprueba que el archivo es exactamente el publicado por Island Crew.

1. Abre la app *Terminal*.
2. Ve a la carpeta donde descargaste el ZIP, por ejemplo: `cd ~/Downloads`
3. Calcula su huella: `shasum -a 256 IslandCrewSuite-1.1.0-macos-arm64.zip`
4. Compárala con la que aparece en el archivo `SHA256SUMS` (en las notas de la versión y en la página de descargas). **Tienen que ser idénticas.**

Atajo: con `SHA256SUMS` en la misma carpeta, ejecuta `shasum -a 256 -c SHA256SUMS`; debe responder `OK`.

Si no coinciden, no instales el archivo: bórralo, descárgalo de nuevo desde el sitio oficial y, si persiste, escribe a hola@islandcrew.es.

Nota: la huella demuestra que el archivo no ha cambiado respecto al publicado; no sustituye a la firma de desarrollador de Apple, que esta versión no lleva.
