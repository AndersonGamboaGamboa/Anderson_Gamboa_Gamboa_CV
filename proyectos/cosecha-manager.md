# Cosecha Manager
**TypeScript · React Native · Expo · Node.js · PostgreSQL**

## Problema y solución

Registra recolección de café y pagos por finca y trabajador. Modela semanas de trabajo, tarifas, cantidades fraccionarias, jornadas retenidas y saldos que deben conservarse entre pagos.

## Capacidades observadas

- Fincas y trabajadores con historial.
- Fechas de trabajo y de pago diferenciadas.
- Redondeo del pago conservando el remanente.
- Ajustes de transporte y ahorro adicional.
- Estado de cuenta individual y búsqueda de trabajadores.

## Evidencia comprobada

El 9 de noviembre de 2026 se ejecutaron **13 pruebas existentes: 13 aprobadas y 0 fallidas**, correspondientes a `domain.test.ts`, `adjustments.test.ts` y `worker-statement.test.ts`.

Se verifican, entre otros casos, el pago de ₡75.000 y saldo de ₡2.000 a partir de ₡77.000, la idempotencia del cierre, cambios de mes/año, tarifas originales de jornadas retenidas y ajustes sin alterar el historial.

Fuente: commit `6c54c90ab97f792b00f965f8a830491dbcb2dd21`. Entorno de revisión: Node.js 24.13.1 y Zod 4.6.7. No se sustituyó la lógica ni se modificaron las pruebas.

## Alcance pendiente

La revisión ejecutó solo ese subconjunto, no autenticación, base de datos, interfaz ni compilación Android. El README señala validaciones físicas y configuración externa pendientes; recomienda un dispositivo de escritura por cuenta. Su encabezado de versión y el de `package.json` difieren, por lo que conviene unificar la documentación antes de distribuir una demo.

## Qué permite discutir en una entrevista

Reglas monetarias explícitas, conservación de saldos, pruebas de calendario, trazabilidad de pagos y separación entre dominio e interfaz.

[Repositorio privado](https://github.com/AndersonGamboaGamboa/cosecha) · [Volver al portafolio](../README.md)
