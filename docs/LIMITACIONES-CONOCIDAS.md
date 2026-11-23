# Limitaciones conocidas — Island Crew Suite 1.0.0

1. **Solo macOS con chip Apple.** Sin versión para Intel ni para Windows en esta descarga. Windows quedará disponible cuando se haya probado en un ordenador real.
2. **Sin firma de desarrollador de Apple ni notarización.** macOS mostrará un aviso al abrir el instalador; hay que usar clic derecho → Abrir. Es normal en software sin firma de pago.
3. **Cabra Beats (Mac 1.1.0) necesita descargar sus motores** (unos 20 GB), 16 GB de memoria y 30 GB libres. La generación de música de principio a fin todavía no está confirmada. No incluye voz clonada (RVC) y no existe para Windows.
4. **Probado en una sola configuración:** macOS 26.4.1 en un Mac con Apple M4. Otras versiones no probadas.
5. **Las claves de IA se guardan en un archivo local** de tu usuario (`claves.json`, permisos de lectura solo para ti) y **no en el Llavero de macOS**. No se envían a Island Crew. Mantén tu Mac protegido y no compartas esa carpeta.
6. **Funciones con servicios externos** (Gemini, Groq, YouTube, Meta, Pixabay, Pexels) no están garantizadas: dependen de tus claves, cuotas y de las condiciones de cada proveedor. Su integración con cuentas reales no se ha probado en esta versión.
7. **El programa no publica por ti** en redes sociales: prepara el material y la subida la haces tú.
8. **ffmpeg incluido** es una compilación de terceros con componentes GPL; ver `THIRD-PARTY-NOTICES.txt`.
9. Carpeta de control: el programa crea `~/IslandCrewAI` (archivos pequeños de estado y, si conectas YouTube, tus credenciales de YouTube con permisos restringidos).
