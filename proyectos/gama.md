# GAMA
**C# · ASP.NET Core MVC · Arquitectura por capas**

## Problema y solución

Sistema web para organizar participantes, actividades, avisos, contactos de emergencia, controles de salud, medicamentos y voluntariado. El código distribuye responsabilidades entre presentación, lógica de negocio, acceso a datos y abstracciones.

## Capacidades observadas en el código

- Módulos de participantes, actividades, salud y voluntarios.
- Registro e inicio de sesión con contraseñas procesadas mediante BCrypt.
- Administración de usuarios y asignación de roles.
- Controlador de usuarios restringido al rol Administrador.
- Protección antifalsificación en la acción de asignación de roles.

## Evidencia revisada

La revisión corresponde al commit `e7c2a5cbbce8c900b6c736675f1dc6e9ff0b7664` de la rama `master`. Se inspeccionaron la estructura de la solución y los flujos de creación de usuario, validación de contraseña y administración de roles.

Fuentes de código — requieren acceso al repositorio privado:

- [Registro y hash de contraseñas](https://github.com/AndersonGamboaGamboa/GAMA/blob/e7c2a5cbbce8c900b6c736675f1dc6e9ff0b7664/GAMA.LogicaDeNegocio/Usuarios/CrearUsuario/CrearUsuarioLN.cs)
- [Validación del inicio de sesión](https://github.com/AndersonGamboaGamboa/GAMA/blob/e7c2a5cbbce8c900b6c736675f1dc6e9ff0b7664/GAMA.LogicaDeNegocio/Usuarios/ValidarLoginLN/ValidarLoginLN.cs)
- [Administración de usuarios y roles](https://github.com/AndersonGamboaGamboa/GAMA/blob/e7c2a5cbbce8c900b6c736675f1dc6e9ff0b7664/GAMA.UI/Controllers/UsuariosController.cs)

## Estado de verificación

**Incluido como caso de arquitectura y código; funcionamiento completo todavía no verificado.** No se compiló ni se ejecutó la aplicación en esta revisión. No se encontró un README ni una suite de pruebas en el árbol examinado, y la consulta de GitHub Actions no mostró ejecuciones.

Para preparar una demostración reproducible, falta documentar el arranque y la base de datos, compilar la solución, preparar datos ficticios y verificar un recorrido de participantes y actividades con distintos roles. Los controles observados no equivalen a una auditoría completa de seguridad.

## Qué permite discutir en una entrevista

Separación entre presentación, negocio y persistencia; contratos entre capas; autenticación con hash de contraseñas y autorización por roles. La contribución individual debe precisarse si hubo trabajo en equipo.

[Repositorio privado](https://github.com/AndersonGamboaGamboa/GAMA) · [Volver al portafolio](../README.md)
