# Hoja rápida — probar Island Crew Suite RC3 en un Windows real

Rellena una cruz y escribe el resultado. Para el registro completo con evidencias usa `HOJA_DE_REGISTRO_PRUEBAS_WINDOWS_RC3.md`.

**Datos:** fecha ____ · equipo ____ · Windows (10/11, versión) ____ · x64 sí/no ____ · físico o máquina virtual ____ · tester ____

## Instalación
- [ ] Windows identificado y arquitectura x64 confirmada
- [ ] Hash del instalador comprobado (`Get-FileHash` frente a `SHA256SUMS`)
- [ ] Instalador ejecutado (anota el aviso de SmartScreen)
- [ ] Instalación finalizada sin error
- [ ] Accesos directos creados (Inicio y Escritorio)

## Funcionamiento
- [ ] Centro de Control abre
- [ ] Carta Viva abre
- [ ] Publicaciones abre
- [ ] Anuncios abre
- [ ] El asistente funciona
- [ ] Selección de una carpeta de datos propia en el asistente: el Centro y las apps usan esa carpeta (RC3 lo corrige respecto a RC2)
- [ ] Carpeta de datos inexistente o disco desconectado: el Centro avisa en vez de mostrar ceros
- [ ] Carta Viva: «abrir carpeta» y vista previa de la carta funcionan
- [ ] Guardar un elemento de prueba con datos ficticios
- [ ] Reinicio y persistencia de lo guardado
- [ ] Sin errores críticos

## Desinstalación
- [ ] Desinstalador ejecutado
- [ ] Aplicaciones y accesos directos eliminados
- [ ] Sin procesos abiertos
- [ ] Datos conservados (según diseño)
- [ ] Reinstalación comprobada (opcional)

**Resultado:** PASS / FAIL / BLOCKED · **Error:** ________ · **Captura adjunta:** sí/no · **Firma:** ________
