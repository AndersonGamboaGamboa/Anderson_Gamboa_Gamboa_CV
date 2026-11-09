# Porcino Manager
**TypeScript · React Native · Expo · Node.js · PostgreSQL**

## Problema y solución

Organiza el engorde porcino por corrales: ingreso de animales, alimentación, medicamentos, costos y ventas. Separa la aplicación móvil del servidor y mantiene reglas de negocio en módulos independientes de la interfaz.

## Capacidades observadas

- Control de existencias de alimento y medicamentos.
- Ventas parciales y por animal con validación de cantidades.
- Cálculos de costos y redondeos; protección frente a sobreventa.
- Identificación sanitaria individual y restricciones por retiro registrado.
- Cliente API con manejo de sesión, tiempo de espera y descarga de PDF.

## Evidencia comprobada

El 9 de noviembre de 2026 se ejecutaron **47 pruebas existentes de la parte móvil: 47 aprobadas y 0 fallidas**, con Node.js 24.13.1. Cubren dominio, alimentación, entradas, salud individual, ventas, persistencia mediante sustitutos y cliente API.

Fuente revisada: commit `518572727f43c3abaf236afeefbc0429e8446037`. Se usaron los archivos originales, sin modificar las pruebas ni su implementación. Esta ejecución no incluye las pruebas del servidor ni una compilación de APK.

## Alcance pendiente

El README documenta APK y servidor desplegados, pero esas afirmaciones no se revalidaron en esta revisión. También registra operaciones de negocio y compartir documentos pendientes de ensayo completo en teléfono. El sistema requiere conexión para guardar; no se presenta como una aplicación con sincronización sin conexión. Falta comprobar la instalación y el recorrido de extremo a extremo para una demostración.

## Qué permite discutir en una entrevista

Modelado del dominio, prevención de movimientos duplicados, integridad de costos, pruebas independientes de la interfaz y manejo de fallos de red.

[Repositorio privado](https://github.com/AndersonGamboaGamboa/corral) · [Volver al portafolio](../README.md)
