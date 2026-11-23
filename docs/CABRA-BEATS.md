# Cabra Beats 1.0.0 para Mac

**Cabra Beats** es la fábrica de música de Island Crew Suite: crea canciones y jingles, portadas, vídeos con la letra y prepara la subida a YouTube. Funciona en tu propio Mac.

## Antes de empezar

- Mac con **chip Apple** (M1 o posterior) y **16 GB de memoria** o más. No funciona en Mac con Intel.
- **30 GB libres** en el disco (puedes usar un disco externo, ver más abajo).
- Conexión a internet durante la instalación: se descargan unos 20 GB.
- La **suite Island Crew Suite 1.0.0** ya instalada en este Mac.

## Instalar en 4 pasos

1. Si aún no lo has hecho, instala la suite (ZIP de Mac de la suite → `Instalar-Mac.command`).
2. Descomprime el ZIP de Cabra Beats (`IslandCrewSuite-CabraBeats-1.0.0-macos-arm64.zip`).
3. Haz **clic derecho (o Control + clic) sobre `Instalar-Cabra-Beats-Mac.command` → Abrir → Abrir**. macOS avisa porque el programa aún no lleva firma de pago de Apple.
4. Espera a que termine (puede tardar bastante según tu conexión). Al acabar verás «Terminado» y una lista de comprobaciones.

Después abre **Island Crew Suite** y pulsa **Cabra Beats**.

## Qué se descarga y de dónde

Los motores **no van dentro de este paquete**: el instalador los descarga de sus webs oficiales y los instala en tu Mac.

| Motor | Para qué sirve | Origen |
|---|---|---|
| ACE-Step 1.5 y sus modelos | Crea la música | GitHub y Hugging Face (ACE-Step) |
| Kokoro | Voz | Hugging Face (hexgrad) |
| Ollama y el modelo `qwen2.5:7b` | Letras con IA local | ollama.com |

Cada uno tiene su propia licencia: mira `LICENCIAS-Y-AVISOS`.

## Guardar los motores en un disco externo

Si tu disco interno va justo de espacio, puedes usar un disco externo. **Debe estar formateado como APFS o «Mac OS Plus (con registro)»**: con exFAT, FAT o NTFS la instalación falla y el instalador te lo avisará. Abre Terminal y ejecuta (cambia la ruta por la de tu disco):

```
bash /ruta/a/Instalar-Cabra-Beats-Mac.command /Volumes/TuDisco/IslandCrewAI
```

## Qué no incluye esta versión

- La **voz clonada (RVC)** no está en esta versión.
- Las funciones que usan servicios externos (Gemini, YouTube, Pixabay, Pexels) dependen de tus propias claves y cuotas, y no están garantizadas.
- El programa **no publica por ti**: prepara el material y la subida la confirmas tú.
- Solo se ha probado en un Mac con chip Apple M4 y macOS 26.4.1.

## Si algo falla

El instalador deja un registro en `~/IslandCrewAI/instalar-cabra-beats.log`. Puedes volver a ejecutarlo: no repite lo que ya está instalado. Escribe a **hola@islandcrew.es** con ese archivo.

## Desinstalar los motores

Cabra Beats y sus motores no se borran al desinstalar la suite. Si quieres quitarlos, borra la carpeta `~/IslandCrewAI` (modelos y motores, unos 20 GB) y, para las letras, abre Terminal y ejecuta `ollama rm qwen2.5:7b`. Tus canciones están en tu carpeta de música, no se borran.

## Créditos y firma de tus creaciones

En la parte superior de la pantalla de Cabra Beats hay una tarjeta **«Créditos y firma»**. Por defecto **no se añade nada** a tu contenido.

- **Tus créditos:** lo que escribas se añade al final de la descripción de YouTube, a la ficha y a la tarjeta final del videoclip. Vacío = nada.
- **Firma de Island Crew:** casilla desactivada por defecto. Si la activas, se añade «Hecho con Cabra Beats · Island Crew».
- **Licencia de YouTube:** «Ninguna» por defecto. Solo se envía si eliges otra.
- La app nunca añade «todos los derechos reservados» por su cuenta.

## Autoría y soporte

Software de Maximiliano Olmos Sánchez para Island Crew Marketing. Todos los derechos reservados; el uso gratuito se concede mediante la licencia libre de la suite. Soporte: **hola@islandcrew.es**.
