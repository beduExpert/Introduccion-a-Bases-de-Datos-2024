#### Ejemplo 2: Selección de campos

##### Objetivos 🎯

- Realizar algunas consultas sencillas.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

1. Supongamos que queremos seleccionar todos los usuarios de la tabla `Usuarios` y mostrar sus nombres y correos electrónicos. Para ello, ejecutaremos la siguiente consulta:

   ```sql
   SELECT nombre, correo_electronico
   FROM Usuarios;
   ```

---
> 🧐 *__Participación en clase__*   
> ¿Qué resultados trae la consulta anterior? ¿Puedes compartir con el grupo?
---

2. Ahora supongamos que queremos seleccionar todos los campos de la tabla Usuarios. Para ello, ejecutamos la siguiente consulta.

   ```sql
   SELECT *
   FROM Usuarios;
   ```

---
> 🧐 *__Participación en clase__*   
> ¿Qué resultados trae la consulta anterior? ¿Puedes compartir con el grupo?
---

3. De forma general, las instrucciones para realizar consultas hasta este punto y que se pueden aplicar con cualquier otro gestor de bases de datos son:

   - Abrir tu herramienta de gestión de bases de datos (por ejemplo, MySQL Workbench).
   - Conéctate a tu servidor de base de datos.
   - Abre una nueva pestaña o ventana de consulta.
   - Escribe tu consulta.
   - Haz clic en el botón "Ejecutar" o presiona la combinación de teclas correspondiente para ejecutar la consulta.
   - Verifica los resultados en el panel de resultados de la herramienta. - Deberías ver una lista de todos los registros de la tabla Usuarios, incluyendo todos los campos.



[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)
