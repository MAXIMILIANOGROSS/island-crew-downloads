# Preguntas frecuentes — Windows

**¿Funciona en Windows?** Existe un instalador para Windows 10/11 de 64 bits (RC3), pero todavía no se ha probado en un equipo Windows real.

**¿Está probado el instalador?** No en Windows. Se ha revisado su integridad y estructura desde macOS. Se publicará un resultado de pruebas cuando haya un equipo disponible.

**¿Por qué aparece como RC3?** Porque es una versión candidata, pendiente de validar. No es la versión final.

**¿Por qué Windows muestra advertencias de seguridad?** Porque el instalador no está firmado. Verifica el SHA-256 antes de ejecutarlo y no ignores alertas sin comprobar el origen.

**¿Dónde se guardan los datos?** Por defecto en `%APPDATA%\IslandCrewSuite`. El programa está en `%LOCALAPPDATA%\IslandCrewSuite\programa`.

**¿Cómo cambio la carpeta de datos?** En el paso 2 del asistente o editando `config.json` (clave `datos`). `ICREW_DATOS` tiene prioridad. Tus datos antiguos no se mueven solos: cópialos tú a la nueva carpeta.

**¿Qué pasa si desconecto un disco?** El Centro de Control muestra una alerta («unidad de datos no conectada» o «no se encuentra la carpeta de datos»); los ceros no son pérdida de datos. Conéctalo y reabre el Centro.

**¿Cómo hago copia de seguridad?** Copia la carpeta de datos a otro disco.

**¿Cómo actualizo?** Ejecuta el instalador nuevo: detecta la instalación previa, la desinstala conservando tus datos e instala encima.

**¿Cómo desinstalo? ¿Qué pasa con mis datos?** Desde «Aplicaciones instaladas» o el menú Inicio. Tus datos se conservan.

**¿Cómo recupero mis datos?** Reinstala y se reutilizará la carpeta de datos existente, o copia tu copia de seguridad a la carpeta de datos.

**¿Qué hago si una aplicación no abre?** Reinicia el equipo, comprueba el Visual C++ Redistributable y envía `%LOCALAPPDATA%\IslandCrewSuite\instalacion.log` a hola@islandcrew.es.

**¿Incluye Cabra Beats?** No.

**¿Por qué el Centro muestra cero?** Normalmente porque no encuentra o no puede leer la carpeta de datos. Mira la alerta del Centro, comprueba que la carpeta existe y que el disco está conectado. Si no hay alerta, la carpeta aún no tiene contenido.
