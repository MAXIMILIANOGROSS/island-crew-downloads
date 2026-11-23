# Compatibilidad multiplataforma

| Plataforma | Paquete | Estado | Observaciones |
|---|---|---|---|
| macOS Apple Silicon (macOS 26.4.1, equipo de desarrollo) | ZIP 1.0.0 ARM64 | PARCIAL (validado en el equipo de desarrollo y en entornos aislados) | Instalación, reinstalación, ruta con espacios, desinstalación, Hub y datos probados. Clics nativos del asistente y escritura de datos por las apps: NO TESTED. |
| Segundo Mac limpio | ZIP 1.0.0 ARM64 | NO TESTED | Procedimiento en `REQUISITOS-Y-COMPATIBILIDAD.md`. |
| macOS Intel | — | NO COMPATIBLE | El paquete es arm64 y no se ha probado en Intel. |
| Windows 10 x64 | Setup 1.0.0-RC3 | NO TESTED | **INSTALADOR DISPONIBLE — RC3 — PENDIENTE DE VALIDACIÓN EN WINDOWS REAL.** Sin prueba física. |
| Windows 11 x64 | Setup 1.0.0-RC3 | NO TESTED | Ídem. |

Windows no figura como incompatible: simplemente no está validado. Esta matriz solo cambiará con pruebas reales.

Diferencias entre los dos paquetes: la versión Windows RC3 incorpora las correcciones de la carpeta de datos, los avisos del Centro y la identidad del asistente de macOS. Faltan por comprobar en un Windows real el instalador, el desinstalador y todas las aplicaciones. Ver `Windows/ESTADO-VALIDACION-WINDOWS-RC3.md`.
