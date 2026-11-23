# Preguntas frecuentes

**¿Es gratuita?** Sí. No hay pagos, suscripciones ni registro. Se usa con una licencia libre incluida en la página de descargas.

**¿Dónde se almacenan mis datos?** En la carpeta que eliges en el paso 2 del asistente. Si no eliges ninguna, en `~/Library/Application Support/IslandCrewSuite`. Tu configuración (`config.json`) y tus claves de IA (`claves.json`, sin cifrar, con lectura solo para tu usuario) están siempre en esa carpeta. Los datos no se envían a Island Crew.

**¿Necesito Internet?** La instalación no descarga nada: todo va en el ZIP. Los programas funcionan en tu Mac; solo usan Internet las funciones que conectan con servicios externos (Google Gemini/YouTube, Groq, Meta, Pixabay, Pexels), con tus propias claves. La licencia se comprueba sin conexión.

**¿Cómo hago una copia de seguridad?** Copia con Finder la carpeta `~/Library/Application Support/IslandCrewSuite` y tu carpeta de datos a otro disco. Guárdala en un lugar privado, porque incluye tus claves.

**¿Cómo actualizo?** Descarga el ZIP nuevo, verifica su SHA-256 y ejecuta su instalador encima. Mira `ACTUALIZACION.md`. No hay actualizador automático.

**¿Cómo verifico la descarga?** `shasum -a 256 archivo.zip` en Terminal y compara con el SHA-256 publicado (`SHA256SUMS`). Mira `VERIFICAR-INTEGRIDAD.md`.

**¿Cómo desinstalo?** Con `Desinstalar-Mac.command` (clic derecho → Abrir). No borra tus datos. Mira `DESINSTALACION.md`.

**¿Qué hago si no se abre?** (1) Usa clic derecho → Abrir sobre el instalador o el lanzador. (2) Si sigue sin abrir, usa Terminal: `bash ` + arrastrar `Instalar-Mac.command` + Intro. (3) Comprueba que tu Mac tiene chip Apple: en Intel no funciona. (4) Escribe a hola@islandcrew.es indicando tu versión de macOS.

**¿Qué ocurre si selecciono una carpeta de datos externa?** Funciona: el Centro y las aplicaciones leen y guardan en esa carpeta. Si el disco no está conectado cuando abres el Centro, aparece la alerta «No se encuentra la carpeta de datos» y los contadores muestran 0; conecta el disco y vuelve a abrir el Centro.

**¿Funciona en Windows o en Mac con Intel?** Este paquete es solo para macOS con chip Apple y no funciona en Mac con Intel. Existe un instalador de Windows candidato (sin firmar), pero no se ha probado en Windows y aún no se distribuye.

**¿Incluye Cabra Beats?** No.

**¿Por qué el Centro muestra cero?** Casi siempre porque el Centro no está leyendo la carpeta donde están tus datos. Comprueba: (1) que la carpeta de datos existe y el disco externo está conectado; (2) que tu usuario tiene permiso de lectura sobre ella; (3) que la carpeta elegida es la que contiene tus vídeos, cartas y publicaciones (la ruta se guarda en `config.json`, clave `datos`). Si algo falla, el Centro muestra una alerta que lo explica (carpeta no encontrada, unidad desconectada, sin permiso o solo lectura). Si no aparece ninguna alerta y todo es cero, esa carpeta aún no tiene contenido.

**¿Cómo cambio la carpeta de datos?** Vuelve a abrir el asistente de Island Crew Suite y elige otra carpeta en el paso 2, o edita `config.json` (clave `datos`). La variable de entorno `ICREW_DATOS` tiene prioridad sobre `config.json`. Tus datos antiguos no se mueven solos: cópialos tú a la nueva carpeta.

**¿Y si el disco externo se desconecta?** Conéctalo de nuevo y reabre el Centro. Mientras esté desconectado, el Centro avisa; no interpretes los ceros como pérdida de datos.

**¿Qué pasa si reinstalo?** Se sustituye solo el programa. Tu configuración, tus claves y tus datos se conservan.
