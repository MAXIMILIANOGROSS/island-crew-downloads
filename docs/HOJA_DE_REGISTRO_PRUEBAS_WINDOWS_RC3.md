# Hoja de registro de pruebas Windows — ISLAND-CREW-WINDOWS-1.0.0-RC3
Candidata RC3. Instalador esperado: `6eccc2decd5dc41fdc57805f102a4f37aa0fde71e22d7ab7814c0a40ea94da24` (28429608 B), `IslandCrewSuite-Setup-1.0.0-RC3-win-x64.exe`. La RC2 queda sustituida.

**Regla:** ninguna fila se marca PASS sin evidencia real adjunta (captura, log o salida). Estados permitidos: WINDOWS PHYSICAL TEST PASS · MANUAL TEST PASS · FAIL · BLOCKED · NOT TESTED. Si se usa una VM, escribirlo en el entorno y no usar «PHYSICAL». Todo arranca en **NOT TESTED**. No firmar, publicar ni subir nada; no usar credenciales reales: en la prueba DPAPI solo el valor ficticio del propio script.
Los scripts de `Validacion` no se han ejecutado nunca en Windows: pueden fallar; si fallan, anotar el error (resultado FAIL o BLOCKED, no ocultarlo).

## 0. Datos del entorno (rellenar antes de empezar)
| Campo | Valor |
|---|---|
| Fecha y hora de inicio | |
| Persona que prueba | |
| Equipo (modelo) y tipo | ☐ físico ☐ VM (hipervisor: ) |
| Windows: edición, versión y build (`winver` / `Get-CimInstance Win32_OperatingSystem`) | |
| Arquitectura (debe ser x64) | |
| Cuenta usada: nombre y tipo (☐ usuario estándar ☐ administrador) | |
| Antivirus / Defender activo | |
| VC++ Redistributable x64 instalado (versión; el instalador exige ≥14.51) | |
| Navegador predeterminado y versión | |
| Carpeta de evidencias (p. ej. `resultados\` + capturas) | |

## 1. Registro de pruebas
| ID | Prueba | Procedimiento | Evidencia a adjuntar | Resultado | Fecha / notas |
|---|---|---|---|---|---|
| WR-01 | Verificación SHA-256 del instalador | `Get-FileHash .\IslandCrewSuite-Setup-1.0.0-RC3-win-x64.exe -Algorithm SHA256`; comparar con el valor de arriba y con `Validacion\SHA256-INSTALADOR.txt`. Si no coincide: detener y no instalar | Salida del comando (captura) | NOT TESTED | |
| WR-02 | Diagnóstico previo (solo lectura) | `powershell -NoProfile -ExecutionPolicy Bypass -File Diagnostico.ps1`, con y sin VC++ | Salida / fichero generado | NOT TESTED | |
| WR-03 | Sin VC++ ≥14.51 | (Solo si el equipo no lo tiene) lanzar el instalador: debe avisar y no instalar nada; el aviso solo indica `aka.ms/vc14/vc_redist.x64.exe` | Captura del aviso; comprobar que no existe `%LOCALAPPDATA%\IslandCrewSuite\programa\runtime` | NOT TESTED | |
| WR-04 | Aviso de SmartScreen (sin firma) | Ejecutar el .exe con doble clic como usuario | Captura del mensaje exacto | NOT TESTED | Esperado: avisa por no estar firmado |
| WR-05 | Instalación como usuario estándar | Con una cuenta SIN privilegios de administrador: instalar con el asistente (por usuario, sin elevación). Anotar si aparece petición UAC (no debería) | Capturas del asistente y de la pantalla de licencia (debe incluir los avisos de terceros); `%LOCALAPPDATA%\IslandCrewSuite\instalacion.log` | NOT TESTED | |
| WR-06 | Integridad de lo instalado | Revisar en `instalacion.log` el resultado de `verificar-instalacion.ps1` (235 ficheros esperados) | Fragmento del log | NOT TESTED | |
| WR-07 | Avisos de licencia instalados | Existen `Licencias\LICENCIAS.txt`, `AVISOS-DE-TERCEROS.txt`, `PROCEDENCIA-DE-LICENCIAS.txt`, `OpenSSL-3.5.9-LICENSE.txt` y `Licencias\TERCEROS\` (6 ficheros) en la carpeta instalada | Listado (`dir /s`) | NOT TESTED | |
| WR-08 | Accesos directos y entrada de desinstalación | Menú Inicio y Escritorio; entrada en «Aplicaciones instaladas» (clave HKCU) | Capturas | NOT TESTED | |
| WR-09 | Apertura: Centro de Control | Abrir desde el acceso directo | Captura de la ventana; hora | NOT TESTED | |
| WR-10 | Apertura: Carta Viva | Abrir desde el Centro de Control o el acceso directo | Captura | NOT TESTED | |
| WR-11 | Apertura: Publicaciones (Cabra Social) | Idem | Captura | NOT TESTED | |
| WR-12 | Apertura: Anuncios (Cabra Social) | Idem | Captura | NOT TESTED | Cabra Beats NO es para Windows |
| WR-13 | Ventanas y navegador | Para cada app: ¿se abre su propia ventana o el navegador predeterminado?; cerrar y reabrir; minimizar/restaurar; abrir dos a la vez; comprobar que cerrar una no cierra las demás; tras cerrar todo, no deben quedar procesos `pythonw.exe` (Administrador de tareas) | Capturas y nota de cuál es el comportamiento real | NOT TESTED | Anotar el comportamiento observado, no el esperado |
| WR-14 | Funciones básicas sin cuentas externas | En Carta Viva, Publicaciones y Anuncios: crear un elemento de prueba con datos ficticios y guardarlo | Capturas | NOT TESTED | Sin YouTube/Meta/IA reales |
| WR-15 | DPAPI — escribir | `python test_dpapi_windows.py CARPETA_SUITE escribir` (script en la carpeta de herramientas del titular, NO viene dentro de RC3; copiarlo aparte; CARPETA_SUITE = carpeta instalada que contiene `core.py`, bajo `%LOCALAPPDATA%\IslandCrewSuite\programa\app\scripts\suite`: confirmar la ruta real). Valor FICTICIO | Salida; comprobar que `claves.dpapi.json` no contiene texto plano | NOT TESTED | No simular |
| WR-16 | DPAPI — persistencia | Cerrar todo y reiniciar sesión o PC; `... leer` en proceso nuevo | Salida | NOT TESTED | |
| WR-17 | DPAPI — otra cuenta | Copiar `claves.dpapi.json` a una ruta legible; desde una SEGUNDA cuenta de Windows: `... ajeno RUTA`; debe FALLAR el descifrado | Salida de la segunda cuenta | NOT TESTED | |
| WR-18 | Datos de usuario creados | Confirmar que los datos viven en `%APPDATA%\IslandCrewSuite` y no en la carpeta del programa | Listado de ambas rutas | NOT TESTED | |
| WR-19 | Desinstalación | Desinstalar desde «Aplicaciones instaladas» o `uninstall.exe` | Capturas; log | NOT TESTED | |
| WR-20 | Conservación de datos | Tras desinstalar: `%APPDATA%\IslandCrewSuite` (y las claves) siguen intactos; la carpeta `programa` y los accesos directos han desaparecido; clave HKCU eliminada | Listados antes/después | NOT TESTED | |
| WR-21 | Reinstalación sobre datos existentes | Volver a instalar RC3; la app encuentra los datos y las claves anteriores | Capturas | NOT TESTED | |
| WR-22 | Script automático (opcional) | `Probar-Suite.ps1 -TipoEntorno fisico` y luego con `-Instalar` (instala/desinstala de verdad en el usuario actual) | Carpeta `resultados\` (informe .md/.json) | NOT TESTED | |
| WR-24 | Carpeta de datos personalizada | En el asistente elegir una carpeta distinta de la de por defecto (con espacios y acentos); crear un dato de prueba; reiniciar | El Centro y las apps leen/escriben en esa carpeta; captura | NOT TESTED | RC3 corrige un defecto de RC2 |
| WR-25 | Carpeta inexistente / unidad desconectada | Cambiar `datos` en `config.json` a una ruta que no existe (y, si es posible, a una unidad externa y desconectarla) | El Centro muestra la alerta; captura | NOT TESTED | |
| WR-26 | Carta Viva: abrir carpeta y vista previa | Pulsar los botones de abrir carpeta y ver la carta | Captura | NOT TESTED | RC2 usaba `open` de Mac |
| WR-23 | Antivirus | ¿Defender u otro AV bloquea o pone en cuarentena algo? | Captura / registro de protección | NOT TESTED | |

## 2. Incidencias
| N.º | Prueba | Descripción | Gravedad | Evidencia | Estado |
|---|---|---|---|---|---|
| | | | | | |

## 3. Entregables de la sesión de pruebas
Carpeta `resultados\`, `instalacion.log`, capturas numeradas por ID (WR-xx), esta hoja rellenada y la salida de `Diagnostico.ps1`.

## 4. Cierre
| Campo | Valor |
|---|---|
| Resultado global (solo si todas las filas tienen evidencia) | NOT TESTED |
| Firma / nombre de quien prueba y fecha | |
Aprobar o rechazar la distribución sigue siendo decisión del titular; esta hoja no autoriza publicar, firmar ni subir nada.
