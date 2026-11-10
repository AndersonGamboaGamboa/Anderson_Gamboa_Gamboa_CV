# Procedencia de esta copia

- Original: https://github.com/JorgeAlfaro29/Fausto-Gestion-Academica
- Rama de referencia: `main`.
- Commit: `8c748cba321182afbb3675e20dc6e53c3d9cef64`.
- Fecha de copia y revisión: 9 de noviembre de 2026.
- Trabajo académico colaborativo; se conserva la atribución al equipo y el README original.

Los 99 archivos originales se copiaron sin cambios. Este documento se añadió para identificar la procedencia. El historial completo permanece en el repositorio original. No se encontró un archivo de licencia en esa revisión; esta copia no añade una licencia ni declara derechos exclusivos sobre el proyecto.

## Ejecutar el prototipo localmente

Desde esta carpeta, con Python 3 disponible:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Abrir `http://127.0.0.1:8000/pages/web/Inicio.html` para el sitio institucional o `http://127.0.0.1:8000/IniciarSesion.html` para la interfaz administrativa.

Servir esta carpeta como raíz es importante: hay recursos con rutas absolutas como `/icons/` y `/js/`. Bootstrap, tipografías y otras dependencias se cargan desde servicios externos y requieren conexión. No hay proceso de compilación ni backend en esta versión.

El acceso es simulado y algunos cambios solo duran hasta recargar. Usar únicamente datos ficticios. No se publica una instancia operativa ni se conecta con sistemas de la escuela.

Consulta la [ficha y los límites de verificación](../../proyectos/fausto-gestion-academica.md).
