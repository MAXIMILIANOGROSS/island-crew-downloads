# Desinstalación de Island Crew Suite

**El desinstalador nunca borra tus datos.** Solo quita los programas.

## Desinstalar
1. Abre la carpeta `IslandCrewSuite-1.0.0-macos-arm64` (la del ZIP).
2. Clic derecho sobre `Desinstalar-Mac.command` → **Abrir**.
3. Verás el mensaje «Island Crew Suite desinstalada. Tus cartas y datos NO se han borrado.»

Se eliminan: la carpeta del programa (`~/Library/Application Support/IslandCrewSuite/programa`) y los lanzadores (Island Crew Suite, Carta Viva, Publicaciones y Anuncios) de `~/Applications` y del Escritorio.

## Qué se conserva
- **Configuración y claves:** `config.json` y `claves.json` en `~/Library/Application Support/IslandCrewSuite`.
- **Tus datos y documentos:** cartas, vídeos, publicaciones y música en la carpeta que elegiste en el asistente.
- **Tus copias de seguridad.**

**Atención:** si en el asistente no elegiste otra carpeta, tus datos están dentro de `~/Library/Application Support/IslandCrewSuite`. En ese caso, no borres esa carpeta salvo que quieras eliminar también tus datos y claves. Haz antes una copia de seguridad.

## Si ya no tienes el ZIP
Cierra los programas y, con Finder, elimina a mano: la carpeta `programa` dentro de `~/Library/Application Support/IslandCrewSuite` y los cuatro lanzadores de `~/Applications` (y del Escritorio). Nada más es necesario.

Qué se ha probado: desinstalación en una cuenta aislada, con datos y configuración conservados, sin lanzadores ni accesos rotos y sin procesos residuales.
