# Actualización de Island Crew Suite

**No hay actualizador automático ni aviso de nuevas versiones.** Las actualizaciones son manuales: descargas el ZIP nuevo y vuelves a instalar encima.

1. **Saber qué versión tienes.** La versión es la del ZIP que descargaste (aparece en su nombre y en el archivo `LEEME.txt` de su carpeta). El programa instalado no muestra todavía un número de versión.
2. **Buscar nuevas versiones.** Consulta la página de descargas o la sección Releases del repositorio `island-crew-downloads`. Cada versión tiene su ZIP, su SHA-256 y su `CHANGELOG.md`.
3. **Copia de seguridad (antes de actualizar).** Con Finder, copia a otro disco o carpeta:
   - La carpeta `~/Library/Application Support/IslandCrewSuite` (contiene `config.json` y `claves.json`; este último guarda tus claves de IA sin cifrar, así que guarda la copia en un lugar privado). Para llegar: Finder → menú Ir → mantén la tecla Opción → Biblioteca.
   - Tu carpeta de datos, si elegiste una distinta (por ejemplo, la de tu disco externo).
4. **Descarga y verifica** el ZIP nuevo como en la guía de instalación (paso 2: SHA-256).
5. **Actualiza.** Cierra los programas de la Suite. Descomprime el ZIP nuevo y abre su `Instalar-Mac.command` con clic derecho → Abrir. El instalador sustituye solo la carpeta `programa`; tu configuración, tus claves y tus datos no se tocan.
6. **Verifica.** Abre Island Crew Suite y comprueba que el Centro muestra tus datos y que Carta Viva, Publicaciones y Anuncios se abren.
7. **Si algo falla.** Vuelve a instalar el ZIP anterior (si lo guardaste) y, si hiciera falta, restaura la copia de seguridad copiando de nuevo las carpetas del paso 3.

Qué se ha probado: reinstalar encima de una instalación existente conservando configuración, claves y datos (mismo número de archivos tras reinstalar). La actualización entre dos versiones distintas todavía no se ha podido probar porque solo existe la 1.0.0.
