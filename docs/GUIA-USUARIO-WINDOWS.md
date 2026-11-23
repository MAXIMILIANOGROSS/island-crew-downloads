# Guía de usuario — Windows (RC3)

Esta guía describe cómo está diseñado el instalador. **Los pasos no se han comprobado todavía en un Windows real.** Si algo no coincide, avísanos en hola@islandcrew.es.

1. **Descargar** el instalador desde la fuente oficial.
2. **Verificar la integridad.** En PowerShell: `Get-FileHash .\IslandCrewSuite-Setup-1.0.0-RC3-win-x64.exe -Algorithm SHA256` y compara con `SHA256SUMS`. Si no coincide, no lo ejecutes.
3. **Entender qué es RC3:** una versión candidata, previa a la final, pendiente de pruebas en Windows.
4. **Ejecutar** el instalador con doble clic.
5. **Advertencias de Windows.** El instalador no está firmado, así que SmartScreen puede avisar. No las ignores sin más: continúa solo si el hash coincide y la descarga es de la fuente oficial. Si Windows o tu antivirus lo bloquean, no lo fuerces: escríbenos.
6. **Completar la instalación.** Si falta el Visual C++ Redistributable, el instalador lo dirá y no instalará nada; instálalo desde Microsoft y repite.
7. **Abrir** Island Crew Suite desde el Escritorio o el menú Inicio.
8. **Carpeta de datos.** En el paso 2 del asistente puedes elegir una carpeta (también en un disco externo); el Centro y las aplicaciones usarán esa carpeta. Si no existe o el disco no está conectado, el Centro te lo avisará en lugar de mostrar ceros.
9. **Abrir las aplicaciones:** Carta Viva, Cabra Social (Publicaciones y Anuncios) y el Centro de Control.
10. **Guardar datos** con elementos de prueba antes de usar datos reales.
11. **Cerrar** las ventanas.
12. **Reiniciar** el equipo.
13. **Comprobar** que lo guardado sigue ahí.
14. **Copia de seguridad:** copia la carpeta de datos (`%APPDATA%\IslandCrewSuite` por defecto) a otro disco. Contiene tus claves de IA protegidas para tu usuario de Windows.
15. **Desinstalar** desde «Aplicaciones instaladas» o el menú Inicio.
16. **Qué permanece:** tus datos y configuración. Se elimina solo el programa, los accesos directos y su registro de desinstalación.
