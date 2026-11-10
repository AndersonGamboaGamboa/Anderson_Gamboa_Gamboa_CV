# Escuela Fausto Herrera Cordero · Gestión académica
**Proyecto académico colaborativo · HTML · CSS · JavaScript · Bootstrap**

Prototipo de interfaces para la gestión académica, administrativa y operativa de la institución educativa Fausto Herrera Cordero, Limón, Costa Rica.

![Portada del prototipo capturada durante la revisión](imagenes/fausto-inicio.png)

## Mi participación documentada

El historial vinculado a AndersonGamboaGamboa incluye el [commit de incorporación de módulos](https://github.com/JorgeAlfaro29/Fausto-Gestion-Academica/commit/35756ad76b621346c9ec03e5e24484e58fc88573), cuyo mensaje enumera prematrícula, permisos, tickets, activos, mantenimiento e insumos. También registra [ajustes de navegación](https://github.com/JorgeAlfaro29/Fausto-Gestion-Academica/commit/950a83e1af4fe982d20a00ebb40665f864cf70af).

Estas evidencias permiten presentar aportes concretos al trabajo del equipo, sin atribuir autoría exclusiva de toda la solución.

## Qué contiene

- Sitio institucional con inicio, servicios, contacto y prematrícula.
- Pantallas de matrícula, calificaciones, noticias, personal, permisos y otros módulos administrativos.
- Formularios, tablas, modales e interacciones de navegador.
- 99 archivos de la versión original, incluidos 56 documentos HTML.

## Verificación realizada el 9 de noviembre de 2026

Se revisó el commit `8c748cba321182afbb3675e20dc6e53c3d9cef64` en una copia local:

| Comprobación | Resultado |
|---|---|
| Carga de las 56 páginas en Chrome mediante servidor local | Todas respondieron HTTP 200 |
| Sintaxis de scripts externos y bloques inline | 33 comprobaciones sin errores de sintaxis |
| Errores de JavaScript al cargar | `EditarActivo.html` produjo `$ is not defined` |
| Referencias locales en HTML | 38 apariciones hacia 23 destinos distintos: 13 apariciones con diferencias de mayúsculas y 25 sin archivo de destino coincidente |
| Inicio de sesión con valores ficticios no registrados | Abre el menú; confirma que es una simulación, no autenticación real |
| Cambio de estado de una persona y recarga | El estado inicial reaparece; el cambio no persiste |

[Primera revisión](fausto-verificacion.json) · [Segunda verificación detallada](fausto-reverificacion.json).

La segunda verificación confirmó que los 99 archivos copiados coinciden con sus blobs originales en GitHub. Se utilizó un servidor local sensible a mayúsculas para evitar que Windows ocultara errores de rutas. El conteo de 38 es de apariciones de referencias en el texto HTML —incluye referencias dentro de scripts—, no de archivos únicos ni de clics fallidos.

También se comprobaron seis escenarios: formulario de acceso vacío bloqueado; acceso con valores ficticios; menú accesible en sesión nueva sin login; cambio de estado del personal que se revierte al recargar; alta de personal que desaparece al recargar; y confirmación de contacto sin solicitudes de red tras pulsar Enviar. Son comprobaciones de comportamiento observado, no seis certificaciones de funcionalidad correcta.

A 390 × 844 píxeles se midió desbordamiento horizontal en Inicio, Contacto y Menú; no se detectó en Login y Gestión de Personal. Es una comprobación limitada de cinco pantallas, no una auditoría completa de accesibilidad o diseño móvil.

El error de EditarActivo se debe a que usa jQuery sin cargar esa biblioteca. La segunda comprobación reprodujo el mismo error.

## Estado del proyecto

**Prototipo de frontend, no sistema escolar completo listo para producción.** La versión revisada no contiene backend ni integración de base de datos. No se encontraron llamadas `fetch`, `XMLHttpRequest`, `localStorage` o `sessionStorage` en los archivos HTML/JavaScript examinados. No se encontró suite de pruebas ni ejecuciones de GitHub Actions.

La comprobación de carga no valida todos los botones ni procesos. El formulario de contacto muestra una confirmación local sin enviar el mensaje; distintos módulos usan datos incorporados en el código. No utilizar datos personales reales ni contraseñas reales en esta demo.

Para convertirlo en aplicación operativa hacen falta autenticación y autorización del servidor, persistencia, validación de entradas, corrección de navegación y pruebas de los flujos completos. Las entradas interpoladas mediante `innerHTML` también requieren revisión antes de aceptar datos no confiables.

## Código y procedencia

- [Copia del código en este portafolio](../codigo/fausto-gestion-academica/)
- [Repositorio original del equipo](https://github.com/JorgeAlfaro29/Fausto-Gestion-Academica)
- [Procedencia e instrucciones para ejecutar](../codigo/fausto-gestion-academica/ORIGEN-PORTAFOLIO.md)

La copia conserva los archivos originales y sus límites; no se presenta como una versión corregida. No se modificó el repositorio del equipo.

[Volver al portafolio](../README.md)
