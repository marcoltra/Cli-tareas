# tareas

Mi herramienta de línea de órdenes para automatizar tareas repetitivas con ficheros.

## Spec (versión 0 · 26/10/2026)
1. **Problema:** cada semana pierdo tiempo ordenando a mano mi carpeta de Descargas, que se llena de PDFs de clase e instaladores que ya no uso, y mis apuntes de DAM están mezclados sin separar por asignatura.
2. **Para quién:** para mí y para cualquier estudiante con las descargas y los apuntes desordenados.
3. **Cómo se usa:** `tareas ORDEN [CARPETA] [opciones]` desde cualquier terminal.
4. **Órdenes de la semana 1:** `tareas --help`, `tareas version`, `tareas listar [CARPETA]`.
5. **Órdenes previstas:** `tareas acciones`, `tareas validar`, `tareas ejecutar NOMBRE --simular`.
6. **Mis 3 acciones (borrador):** ordenar-pdfs (mover los PDF de Descargas a mi carpeta de apuntes), limpiar-instaladores (borrar .exe, .msi y .zip con más de 14 días, preguntando antes), ordenar-apuntes (mover cada apunte a la carpeta de su asignatura según su nombre).
7. **Nunca hará:** borrar sin preguntar ni tocar ficheros fuera de la carpeta que le indique.
8. **Plataformas:** Linux primero; también Windows y macOS.
9. **Códigos de salida:** 0 bien · 1 fallo al ejecutar · 2 uso incorrecto · 3 configuración inválida.
10. **Instalación:** `uv tool install --editable .` (lo completo en la semana 4).