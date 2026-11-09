# Ganado Manager
**C# · ASP.NET Core · .NET MAUI · Entity Framework Core · MySQL**

## Problema y solución

Centraliza fichas de animales, movimientos de compra y venta, pesajes, inventarios de alimentos y medicamentos y resultados económicos por finca. La solución separa API, dominio, aplicación, infraestructura y cliente móvil.

## Capacidades observadas

- Fincas privadas con separación de datos por propietario.
- Compras y ventas asociadas al historial del animal.
- Alimentación e inventarios con asignación de costos.
- Cola local de operaciones con identificadores estables para reintentos.
- Pruebas de recorridos de negocio, aislamiento, sesiones y sincronización.

## Evidencia comprobada

La ejecución de GitHub Actions [42528318415](https://github.com/AndersonGamboaGamboa/GANADO_MANAGER/actions/runs/42528318415), asociada al commit `837de669aebe9dc93b7844ba44c8bb7349e88717`, terminó correctamente. Sus pasos **Fast regression tests** y **MySQL integration tests** están aprobados.

Se inspeccionó el recorrido de pruebas que enlaza compra, alimentación, medicamento, pesaje y venta, incluyendo rechazo de entradas inválidas y prevención de duplicados. La ejecución de CI se verificó en GitHub; no se volvió a ejecutar localmente.

## Alcance pendiente

La evidencia anterior no acredita la experiencia completa en un teléfono ni la compilación/firma de iOS. El README conserva pendientes de dispositivos y producción, y debe reconciliarse con las mejoras posteriores y la integración MySQL ya disponible. Para una presentación práctica conviene preparar un recorrido con datos ficticios y registrar su resultado en Android.

## Qué permite discutir en una entrevista

Separación de responsabilidades, consistencia de inventarios, reintentos idempotentes, aislamiento de datos y pruebas contra una base relacional real.

[Repositorio privado](https://github.com/AndersonGamboaGamboa/GANADO_MANAGER) · [Volver al portafolio](../README.md)
