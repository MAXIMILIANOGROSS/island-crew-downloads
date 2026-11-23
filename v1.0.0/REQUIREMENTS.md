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
