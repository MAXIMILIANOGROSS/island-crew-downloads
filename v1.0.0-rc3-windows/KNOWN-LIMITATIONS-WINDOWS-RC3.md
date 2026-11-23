# Estado de validación — Island Crew Suite 1.0.0-RC3 (Windows x64)

**INSTALADOR DISPONIBLE — RC3 — PENDIENTE DE VALIDACIÓN EN WINDOWS REAL.**

- Windows 10 x64: NO TESTED. Windows 11 x64: NO TESTED.
- El instalador RC3 se ha construido y revisado únicamente desde macOS. Nunca se ha ejecutado en Windows.
- No está firmado con Authenticode: Windows SmartScreen puede mostrar un aviso.
- No incluye Cabra Beats.

## Qué cambia respecto a la RC2 (6 ficheros del programa; el instalador y el desinstalador son los mismos)
1. La carpeta de datos elegida en el asistente se respeta (`config.json`, clave `datos`). La variable `ICREW_DATOS` sigue teniendo prioridad.
2. El Centro de Control avisa si la carpeta de datos no existe, si la unidad no está conectada o si no se puede leer, en lugar de mostrar ceros sin explicación.
3. Carta Viva: los botones que abren una carpeta o la vista previa usaban el comando `open` de Mac y fallaban en Windows; ahora usan el mecanismo multiplataforma de la suite.
4. El asistente incorpora la identidad visual (mascota y fondo) de la versión macOS.
5. Se han quitado los textos que mencionaban un disco concreto del autor.

## Qué se ha comprobado (sin Windows real)
- 235 ficheros instalables con SHA-256 coincidente; sin claves ni datos personales; el EXE tiene cabecera válida y hash propio.
- 14 comprobaciones automáticas de la lógica de datos con rutas de Windows simuladas desde macOS (prioridad `ICREW_DATOS` > `config.json` > carpeta por defecto, espacios y acentos, configuración corrupta, carpeta inexistente, vacía y sin permiso). Esto **no** sustituye a una prueba en Windows.

## Limitaciones conocidas de esta RC3
1. Necesita el «Microsoft Visual C++ Redistributable 2015-2022 (x64)» (14.51 o superior), que no se incluye. El instalador avisa y no instala si falta.
2. El aviso de «carpeta de datos de solo lectura» no está disponible en Windows (el sistema no permite comprobarlo de forma fiable); los avisos de carpeta inexistente, unidad desconectada y sin lectura sí.
3. La detección de unidad desconectada por letra de unidad (por ejemplo `Z:`) se ha probado solo como lógica, no con un disco real.
4. Los scripts de validación incluidos nunca se han ejecutado en Windows y pueden fallar.
5. Quedan en el paquete algunos recursos gráficos de Cabra Beats que no se usan.
6. La RC2 queda sustituida por esta RC3 y se conserva internamente.
