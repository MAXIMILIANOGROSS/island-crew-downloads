# Cabra Beats (incluida en la suite 1.1.0 para Mac)

**Cabra Beats** es la fábrica de música de Island Crew Suite: crea canciones y jingles, portadas, vídeos con la letra y prepara la subida a YouTube. Funciona en tu propio Mac.

> Desde la **1.1.0**, Cabra Beats viene **dentro de la suite**. Si usas la 1.0.0, actualiza con el ZIP de la 1.1.0; el paquete aparte de Cabra Beats 1.0.0 ya no hace falta.

## Antes de empezar

- Mac con **chip Apple** (M1 o posterior) y **16 GB de memoria** o más. No funciona en Mac con Intel.
- **30 GB libres** en un disco **APFS** o «Mac OS Plus (con registro)». No sirven exFAT, FAT ni NTFS.
- Conexión a internet para descargar los motores (unos 20 GB).

## Instalar

1. Instala la suite 1.1.0 (`Instalar-Mac.command`, ver [Instalación](INSTALACION.md)).
2. Al terminar, el instalador pregunta **«¿Descargar ahora los motores de Cabra Beats?»**. Escribe `s` y pulsa Intro. Puede tardar bastante.
3. Si dijiste que no, hazlo cuando quieras con doble clic (clic derecho → Abrir) en `Instalar-Motores-Cabra-Beats.command` (está en la carpeta del ZIP).
4. Abre **Island Crew Suite** y pulsa **Cabra Beats** (o abre el icono «Cabra Beats Island Crew»).

## Qué se descarga y de dónde

Los motores **no van dentro del ZIP**: el instalador los descarga de sus webs oficiales.

| Motor | Para qué sirve | Origen |
|---|---|---|
| ACE-Step 1.5 y sus modelos | Crea la música | GitHub y Hugging Face (ACE-Step) |
| Kokoro | Voz | Hugging Face (hexgrad) |
| Ollama y el modelo `qwen2.5:7b` | Letras con IA local | ollama.com |

Cada uno tiene su propia licencia: mira [Licencias y avisos](LICENCIAS-Y-AVISOS.md).

## Guardar los motores en un disco externo

El disco debe estar en **APFS** o «Mac OS Plus (con registro)». En Terminal (cambia la ruta):

```
bash /ruta/a/Instalar-Motores-Cabra-Beats.command /Volumes/TuDisco/IslandCrewAI
```

## Estado y límites

- La instalación completa de los motores se probó en un Mac limpio. **La generación de música de principio a fin todavía no está confirmada** (el Mac de pruebas se quedó sin espacio en el disco interno).
- No incluye la **voz clonada (RVC)**. No existe versión para Windows.
- Las funciones con servicios externos (Gemini, YouTube, Pixabay, Pexels) dependen de tus claves y cuotas.
- El programa **no publica por ti**: prepara el material y la subida la confirmas tú.
- Solo probado en un Mac con chip Apple M4 y macOS 26.4.1.

## Si algo falla

El instalador deja un registro en `~/IslandCrewAI/instalar-cabra-beats.log`. Puedes volver a ejecutarlo: no repite lo ya instalado. Escribe a **hola@islandcrew.es** con ese archivo.

## Desinstalar los motores

Desinstalar la suite no borra los motores ni tus canciones. Para quitar los motores, borra la carpeta `~/IslandCrewAI` (unos 20 GB) y, para las letras, ejecuta `ollama rm qwen2.5:7b`.

## Créditos y firma de tus creaciones

La tarjeta **«Créditos y firma»** de Cabra Beats controla lo que se añade a tu contenido. Por defecto no se añade nada: tus créditos se añaden solo si los escribes, la firma de Island Crew está desactivada y la licencia de YouTube es «Ninguna».

## Autoría y soporte

Software de Maximiliano Olmos Sánchez para Island Crew Marketing. Soporte: **hola@islandcrew.es**.
