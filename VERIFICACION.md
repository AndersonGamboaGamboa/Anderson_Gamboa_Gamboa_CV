# Alcance de las evidencias

Fecha: 9 de noviembre de 2026.

| Proyecto | Comprobación realizada | Resultado | No cubierto |
|---|---|---|---|
| Ganado Manager | Lectura de código y del resultado de CI del commit 837de66 | Regresión e integración MySQL aprobadas | Nueva ejecución local, interfaz y dispositivos |
| Porcino Manager | 9 archivos de pruebas móviles existentes sobre la fuente revisada | 47 aprobadas, 0 fallidas | Servidor, lint, tipos, exportación y APK |
| Cosecha Manager | 3 archivos de pruebas existentes de dominio/ajustes/estado de cuenta | 13 aprobadas, 0 fallidas | Resto de la suite, lint, tipos, exportación, autenticación y dispositivos |
| GAMA | Inspección del árbol y código de registro, login y administración del commit e7c2a5c | Se observaron capas, BCrypt y autorización administrativa; sin ejecución | Compilación, pruebas automatizadas, base de datos e interfaz |

| Escuela Fausto Herrera Cordero | Carga en Chrome de 56 páginas, 33 comprobaciones de sintaxis y 2 escenarios funcionales | Todas las páginas respondieron 200; 1 página con error JS, 38 referencias locales incorrectas; login y persistencia simulados | Flujos completos, backend, seguridad operativa y comportamiento móvil |

[Detalle del prototipo escolar y procedencia](proyectos/fausto-gestion-academica.md).

## Reproducción de las pruebas locales

Desde la raíz de un checkout de Porcino Manager, con Node.js 24:

```sh
node --experimental-strip-types --test mobile/tests/*.test.ts
```

Desde un checkout de Cosecha Manager con sus dependencias instaladas:

```sh
node --experimental-strip-types --test tests/domain.test.ts tests/adjustments.test.ts tests/worker-statement.test.ts
```

En la revisión se descargaron los archivos necesarios a un directorio aislado. Para Cosecha se instaló únicamente Zod 4.6.7, suficiente para ese subconjunto; no se realizó una instalación completa del proyecto. Node emitió un aviso de detección del tipo de módulo en Cosecha, sin fallos de pruebas.

Para Ganado Manager, consultar la [ejecución verificada](https://github.com/AndersonGamboaGamboa/GANADO_MANAGER/actions/runs/42528318415) y el workflow de esa revisión.

## Interpretación

Las pruebas aprobadas respaldan los comportamientos que ejercitan. No prueban que todas las pantallas, integraciones externas o instalaciones funcionen. No se modificaron bases de datos ni servicios productivos durante la revisión.

Las descripciones funcionales adicionales proceden del código inspeccionado y de la documentación de cada proyecto. La existencia de un README, un APK mencionado o una URL de servidor no se trató como prueba de funcionamiento.

Ganado Manager, Porcino Manager, Cosecha Manager y GAMA son privados. El prototipo escolar es público y tiene una copia atribuida en este repositorio. Los resultados publicados aquí son un resumen; revisar el código o las ejecuciones originales requiere acceso.

[Volver al portafolio](README.md)
