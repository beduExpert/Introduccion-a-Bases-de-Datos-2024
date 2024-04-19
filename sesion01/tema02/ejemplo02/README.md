[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 01`](../../README.md) > [`Selección de campos`](../README.md)

#### Ejemplo 2

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
   <details><summary>Salida</summary>
   <table border=1>
   <tr>
   <td bgcolor=silver class='medium'>nombre</td>
   <td bgcolor=silver class='medium'>correo_electronico</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Juan</td>
   <td class='normal' valign='top'>juan@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Maria</td>
   <td class='normal' valign='top'>maria@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Carlos</td>
   <td class='normal' valign='top'>carlos@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Ana</td>
   <td class='normal' valign='top'>ana@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Pedro</td>
   <td class='normal' valign='top'>pedro@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Laura</td>
   <td class='normal' valign='top'>laura@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Diego</td>
   <td class='normal' valign='top'>diego@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Sofia</td>
   <td class='normal' valign='top'>sofia@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Elena</td>
   <td class='normal' valign='top'>elena@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Alejandro</td>
   <td class='normal' valign='top'>alejandro@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Marina</td>
   <td class='normal' valign='top'>marina@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Javier</td>
   <td class='normal' valign='top'>javier@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Lucia</td>
   <td class='normal' valign='top'>lucia@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Manuel</td>
   <td class='normal' valign='top'>manuel@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Luisa</td>
   <td class='normal' valign='top'>luisa@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Miguel</td>
   <td class='normal' valign='top'>miguel@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Carmen</td>
   <td class='normal' valign='top'>carmen@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Raul</td>
   <td class='normal' valign='top'>raul@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Patricia</td>
   <td class='normal' valign='top'>patricia@example.com</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>Daniel</td>
   <td class='normal' valign='top'>daniel@example.com</td>
   </tr>
   </table>
   </details>

2. Ahora supongamos que queremos seleccionar todos los campos de la tabla Usuarios. Para ello, ejecutamos la siguiente consulta.

   ```sql
   SELECT *
   FROM Usuarios;
   ```
   <details><summary>Salida</summary>
   <table border=1>
   <tr>
   <td bgcolor=silver class='medium'>user_id</td>
   <td bgcolor=silver class='medium'>nombre</td>
   <td bgcolor=silver class='medium'>apellido</td>
   <td bgcolor=silver class='medium'>edad</td>
   <td bgcolor=silver class='medium'>correo_electronico</td>
   <td bgcolor=silver class='medium'>fecha_registro</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>1</td>
   <td class='normal' valign='top'>Juan</td>
   <td class='normal' valign='top'>Perez</td>
   <td class='normal' valign='top'>25</td>
   <td class='normal' valign='top'>juan@example.com</td>
   <td class='normal' valign='top'>2023-01-15</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>2</td>
   <td class='normal' valign='top'>Maria</td>
   <td class='normal' valign='top'>Gomez</td>
   <td class='normal' valign='top'>30</td>
   <td class='normal' valign='top'>maria@example.com</td>
   <td class='normal' valign='top'>2023-02-20</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>3</td>
   <td class='normal' valign='top'>Carlos</td>
   <td class='normal' valign='top'>Lopez</td>
   <td class='normal' valign='top'>28</td>
   <td class='normal' valign='top'>carlos@example.com</td>
   <td class='normal' valign='top'>2023-03-10</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>4</td>
   <td class='normal' valign='top'>Ana</td>
   <td class='normal' valign='top'>Martinez</td>
   <td class='normal' valign='top'>35</td>
   <td class='normal' valign='top'>ana@example.com</td>
   <td class='normal' valign='top'>2023-04-05</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>5</td>
   <td class='normal' valign='top'>Pedro</td>
   <td class='normal' valign='top'>Rodriguez</td>
   <td class='normal' valign='top'>40</td>
   <td class='normal' valign='top'>pedro@example.com</td>
   <td class='normal' valign='top'>2023-05-12</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>6</td>
   <td class='normal' valign='top'>Laura</td>
   <td class='normal' valign='top'>Sanchez</td>
   <td class='normal' valign='top'>27</td>
   <td class='normal' valign='top'>laura@example.com</td>
   <td class='normal' valign='top'>2023-06-20</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>7</td>
   <td class='normal' valign='top'>Diego</td>
   <td class='normal' valign='top'>Garcia</td>
   <td class='normal' valign='top'>33</td>
   <td class='normal' valign='top'>diego@example.com</td>
   <td class='normal' valign='top'>2023-07-08</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>8</td>
   <td class='normal' valign='top'>Sofia</td>
   <td class='normal' valign='top'>Hernandez</td>
   <td class='normal' valign='top'>22</td>
   <td class='normal' valign='top'>sofia@example.com</td>
   <td class='normal' valign='top'>2023-08-15</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>9</td>
   <td class='normal' valign='top'>Elena</td>
   <td class='normal' valign='top'>Diaz</td>
   <td class='normal' valign='top'>29</td>
   <td class='normal' valign='top'>elena@example.com</td>
   <td class='normal' valign='top'>2023-09-30</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>10</td>
   <td class='normal' valign='top'>Alejandro</td>
   <td class='normal' valign='top'>Torres</td>
   <td class='normal' valign='top'>31</td>
   <td class='normal' valign='top'>alejandro@example.com</td>
   <td class='normal' valign='top'>2023-10-25</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>11</td>
   <td class='normal' valign='top'>Marina</td>
   <td class='normal' valign='top'>Ruiz</td>
   <td class='normal' valign='top'>26</td>
   <td class='normal' valign='top'>marina@example.com</td>
   <td class='normal' valign='top'>2023-11-03</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>12</td>
   <td class='normal' valign='top'>Javier</td>
   <td class='normal' valign='top'>Flores</td>
   <td class='normal' valign='top'>34</td>
   <td class='normal' valign='top'>javier@example.com</td>
   <td class='normal' valign='top'>2023-12-18</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>13</td>
   <td class='normal' valign='top'>Lucia</td>
   <td class='normal' valign='top'>Gutierrez</td>
   <td class='normal' valign='top'>32</td>
   <td class='normal' valign='top'>lucia@example.com</td>
   <td class='normal' valign='top'>2024-01-22</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>14</td>
   <td class='normal' valign='top'>Manuel</td>
   <td class='normal' valign='top'>Vazquez</td>
   <td class='normal' valign='top'>37</td>
   <td class='normal' valign='top'>manuel@example.com</td>
   <td class='normal' valign='top'>2024-02-09</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>15</td>
   <td class='normal' valign='top'>Luisa</td>
   <td class='normal' valign='top'>Moreno</td>
   <td class='normal' valign='top'>23</td>
   <td class='normal' valign='top'>luisa@example.com</td>
   <td class='normal' valign='top'>2024-03-14</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>16</td>
   <td class='normal' valign='top'>Miguel</td>
   <td class='normal' valign='top'>Jimenez</td>
   <td class='normal' valign='top'>36</td>
   <td class='normal' valign='top'>miguel@example.com</td>
   <td class='normal' valign='top'>2024-04-28</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>17</td>
   <td class='normal' valign='top'>Carmen</td>
   <td class='normal' valign='top'>Castillo</td>
   <td class='normal' valign='top'>24</td>
   <td class='normal' valign='top'>carmen@example.com</td>
   <td class='normal' valign='top'>2024-05-30</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>18</td>
   <td class='normal' valign='top'>Raul</td>
   <td class='normal' valign='top'>Navarro</td>
   <td class='normal' valign='top'>39</td>
   <td class='normal' valign='top'>raul@example.com</td>
   <td class='normal' valign='top'>2024-06-17</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>19</td>
   <td class='normal' valign='top'>Patricia</td>
   <td class='normal' valign='top'>Garcia</td>
   <td class='normal' valign='top'>28</td>
   <td class='normal' valign='top'>patricia@example.com</td>
   <td class='normal' valign='top'>2024-07-20</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>20</td>
   <td class='normal' valign='top'>Daniel</td>
   <td class='normal' valign='top'>Sanchez</td>
   <td class='normal' valign='top'>31</td>
   <td class='normal' valign='top'>daniel@example.com</td>
   <td class='normal' valign='top'>2024-08-09</td>
   </tr>
   </table>
   </details>

3. De forma general, las instrucciones para realizar consultas hasta este punto y que se pueden aplicar con cualquier otro gestor de bases de datos son:

   - Abrir tu herramienta de gestión de bases de datos (por ejemplo, MySQL Workbench).
   - Conéctate a tu servidor de base de datos.
   - Abre una nueva pestaña o ventana de consulta.
   - Escribe tu consulta.
   - Haz clic en el botón "Ejecutar" o presiona la combinación de teclas correspondiente para ejecutar la consulta.
   - Verifica los resultados en el panel de resultados de la herramienta. - Deberías ver una lista de todos los registros de la tabla Usuarios, incluyendo todos los campos.



[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)
