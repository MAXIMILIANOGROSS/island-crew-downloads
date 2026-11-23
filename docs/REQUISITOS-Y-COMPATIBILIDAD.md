# Requisitos y compatibilidad

## Requisitos
- Mac con **chip Apple (M1 o posterior)**. El instalador se detiene en Mac con Intel.
- Unos 600 MB libres en disco (el paquete descomprimido ocupa unos 110 MB).
- Conexión a internet solo para las funciones que usan servicios externos (claves de IA, publicar la carta). Carta Viva, el calendario y los vídeos se generan en tu Mac.
- Sin permisos de administrador: se instala en tu usuario.
- No hace falta instalar Python ni ffmpeg: van incluidos.

## Compatibilidad verificada

| Sistema | Resultado |
|---|---|
| macOS 26.4.1, Mac mini Apple M4 | Instalación, desinstalación, reinstalación y arranque de Centro de Control, Carta Viva y Cabra Social: comprobados |
| Otras versiones de macOS | **No probadas.** El instalador declara macOS 11 como mínimo técnico, sin verificación |
| Mac con Intel | No incluido en esta versión |
| Windows | No disponible todavía (sin pruebas en un equipo real) |

Solo se afirma compatibilidad con lo que se ha probado. Si lo usas en otra versión de macOS y falla, escríbenos a hola@islandcrew.es.

## Dependencias incluidas
Python 3.11 (runtime autónomo), Pillow, segno (códigos QR) y ffmpeg. Detalle y licencias en `THIRD-PARTY-NOTICES.txt`.

## Servicios externos opcionales (con tus propias claves o cuentas)
Google Gemini y Groq (textos, traducciones), Google/YouTube y Meta (conexiones, si las configuras), Pixabay/Pexels (imágenes). Ninguno es obligatorio para abrir los programas. Su uso se rige por las condiciones de cada proveedor y por las cuotas de tu propia cuenta.

## Matriz de compatibilidad (estado real de las pruebas)

| Entorno | Estado | Nota |
|---|---|---|
| macOS Apple Silicon (máquina de desarrollo, macOS 26.4.1) | PARCIAL | Instalación, reinstalación, ruta distinta, ruta con espacios, entorno mínimo, desinstalación y Hub probados. Clics nativos del asistente, escritura de datos por las apps y descarga por URL pública: NO TESTED. |
| Segundo Mac limpio (Apple Silicon) | NO TESTED | Ver procedimiento manual abajo. |
| macOS con chip Intel | NO COMPATIBLE | El paquete es solo arm64 y no se ha probado en Intel. |
| Windows 10 | NO TESTED | Existe un instalador Windows candidato (1.0.0-RC3, sin firmar) construido y revisado solo desde macOS; nunca se ha ejecutado en Windows y no forma parte de este paquete macOS. |
| Windows 11 | NO TESTED | Existe un instalador Windows candidato (1.0.0-RC3, sin firmar) construido y revisado solo desde macOS; nunca se ha ejecutado en Windows y no forma parte de este paquete macOS. |

## Procedimiento manual para probar en un segundo Mac

1. Usa un Mac con chip Apple y un usuario sin Island Crew instalado.
2. Descarga el ZIP y comprueba su SHA-256 con `shasum -a 256` frente a `SHA256SUMS`.
3. Descomprime, ejecuta `Instalar-Mac.command` (clic derecho, Abrir) y anota cualquier aviso de macOS.
4. Abre el asistente: pega la licencia libre, elige carpeta de datos, guarda claves.
5. Abre el Centro, Carta Viva, Publicaciones y Anuncios.
6. Con una carpeta de datos vacía, comprueba que el Centro no muestra alertas falsas; desconecta un disco externo y comprueba el aviso.
7. Ejecuta `Desinstalar-Mac.command` y comprueba que tus datos siguen ahí y que se puede reinstalar.
8. Anota PASS/FAIL por paso y envíalo a hola@islandcrew.es.
