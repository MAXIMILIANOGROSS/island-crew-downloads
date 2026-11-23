# Instalación de Island Crew Suite 1.1.0 (macOS, chip Apple)

**Antes de empezar:** necesitas un Mac con chip Apple (M1 o posterior) y unos 600 MB libres. No hace falta ser administrador ni tener Python instalado.

1. **Descarga.** Descarga `IslandCrewSuite-1.1.0-macos-arm64.zip` desde la página de descargas (Releases del repositorio `island-crew-downloads`). Cuando la descarga esté publicada, esa página mostrará el enlace; hasta entonces no hay descarga pública.
2. **Verifica el archivo.** Abre la app Terminal y escribe `shasum -a 256 ` (con un espacio al final), arrastra el ZIP a la ventana y pulsa Intro. El resultado debe ser idéntico al SHA-256 que aparece en la página de descargas y en el archivo `SHA256SUMS`. Si no coincide, no lo abras y vuelve a descargarlo.
3. **Descomprime.** Haz doble clic en el ZIP. Se crea la carpeta `IslandCrewSuite-1.1.0-macos-arm64`. No muevas archivos fuera de ella: el instalador necesita la carpeta completa.
4. **Instala.** Dentro de la carpeta, haz clic derecho en `Instalar-Mac.command` → **Abrir** → **Abrir**. macOS avisa porque la aplicación no está notarizada por Apple; es normal. Si no se abre, abre Terminal, escribe `bash ` (con espacio), arrastra `Instalar-Mac.command` y pulsa Intro.
5. **Abre la Suite.** Al terminar se abre Island Crew Suite (el Centro de Control). Después la encuentras en la carpeta *Aplicaciones* de tu usuario (`~/Applications`) y en el Escritorio, junto a Carta Viva, Publicaciones y Anuncios.
6. **Configura tus datos.** En el asistente, el paso 2 te deja elegir la carpeta donde se guardarán tus cartas y contenidos (puede estar en un disco externo). En el paso 3 pega el texto de la licencia libre publicado en la página de descargas.
7. **Comprueba que funciona.** El Centro de Control debe abrirse en su propia ventana. Si ya tienes datos en la carpeta elegida, verás sus recuentos (restaurantes, platos, vídeos, publicaciones). Si la carpeta no existe o el disco está desconectado, el Centro muestra una alerta «No se encuentra la carpeta de datos»: los ceros no serían reales.

Qué se ha probado: instalación, reinstalación encima, desinstalación y lectura del Centro en macOS 26.4.1 con chip Apple. Otras versiones de macOS no se han probado.

## Cabra Beats (música)

Al final de la instalación se te ofrece descargar los motores de Cabra Beats (unos 20 GB). Puedes aceptar o hacerlo más tarde con `Instalar-Motores-Cabra-Beats.command`. Requisitos y detalles: [Cabra Beats](CABRA-BEATS.md).
