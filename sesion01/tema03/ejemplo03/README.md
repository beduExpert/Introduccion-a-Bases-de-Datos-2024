[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 01`](../../README.md) > [`Filtrado básico`](../README.md)

#### Ejemplo 3

##### Objetivos 🎯

- Realizar algunas consultas sencillas.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Veamos algunos ejemplos de filtros.

1. Usuarios mayores a 30 años:

   ```sql
   SELECT * 
   FROM Usuarios
   WHERE edad > 30;
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
   <td class='normal' valign='top'>7</td>
   <td class='normal' valign='top'>Diego</td>
   <td class='normal' valign='top'>Garcia</td>
   <td class='normal' valign='top'>33</td>
   <td class='normal' valign='top'>diego@example.com</td>
   <td class='normal' valign='top'>2023-07-08</td>
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
   <td class='normal' valign='top'>16</td>
   <td class='normal' valign='top'>Miguel</td>
   <td class='normal' valign='top'>Jimenez</td>
   <td class='normal' valign='top'>36</td>
   <td class='normal' valign='top'>miguel@example.com</td>
   <td class='normal' valign='top'>2024-04-28</td>
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
   <td class='normal' valign='top'>20</td>
   <td class='normal' valign='top'>Daniel</td>
   <td class='normal' valign='top'>Sanchez</td>
   <td class='normal' valign='top'>31</td>
   <td class='normal' valign='top'>daniel@example.com</td>
   <td class='normal' valign='top'>2024-08-09</td>
   </tr>
   </table>
   </details>


2. Productos cuyo precio es menor a 100:

   ```sql
   SELECT * 
   FROM Productos
   WHERE precio < 100;
   ```

   <details><summary>Salida</summary>


   <table border=1>
   <tr>
   <td bgcolor=silver class='medium'>producto_id</td>
   <td bgcolor=silver class='medium'>nombre_producto</td>
   <td bgcolor=silver class='medium'>descripcion</td>
   <td bgcolor=silver class='medium'>precio</td>
   <td bgcolor=silver class='medium'>stock_disponible</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>1</td>
   <td class='normal' valign='top'>Producto 1</td>
   <td class='normal' valign='top'>Descripción del producto 1</td>
   <td class='normal' valign='top'>10.00</td>
   <td class='normal' valign='top'>100</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>2</td>
   <td class='normal' valign='top'>Producto 2</td>
   <td class='normal' valign='top'>Descripción del producto 2</td>
   <td class='normal' valign='top'>15.00</td>
   <td class='normal' valign='top'>150</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>3</td>
   <td class='normal' valign='top'>Producto 3</td>
   <td class='normal' valign='top'>Descripción del producto 3</td>
   <td class='normal' valign='top'>20.00</td>
   <td class='normal' valign='top'>120</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>4</td>
   <td class='normal' valign='top'>Producto 4</td>
   <td class='normal' valign='top'>Descripción del producto 4</td>
   <td class='normal' valign='top'>25.00</td>
   <td class='normal' valign='top'>90</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>5</td>
   <td class='normal' valign='top'>Producto 5</td>
   <td class='normal' valign='top'>Descripción del producto 5</td>
   <td class='normal' valign='top'>30.00</td>
   <td class='normal' valign='top'>80</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>6</td>
   <td class='normal' valign='top'>Producto 6</td>
   <td class='normal' valign='top'>Descripción del producto 6</td>
   <td class='normal' valign='top'>35.00</td>
   <td class='normal' valign='top'>110</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>7</td>
   <td class='normal' valign='top'>Producto 7</td>
   <td class='normal' valign='top'>Descripción del producto 7</td>
   <td class='normal' valign='top'>40.00</td>
   <td class='normal' valign='top'>70</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>8</td>
   <td class='normal' valign='top'>Producto 8</td>
   <td class='normal' valign='top'>Descripción del producto 8</td>
   <td class='normal' valign='top'>45.00</td>
   <td class='normal' valign='top'>100</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>9</td>
   <td class='normal' valign='top'>Producto 9</td>
   <td class='normal' valign='top'>Descripción del producto 9</td>
   <td class='normal' valign='top'>50.00</td>
   <td class='normal' valign='top'>130</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>10</td>
   <td class='normal' valign='top'>Producto 10</td>
   <td class='normal' valign='top'>Descripción del producto 10</td>
   <td class='normal' valign='top'>55.00</td>
   <td class='normal' valign='top'>95</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>11</td>
   <td class='normal' valign='top'>Producto 11</td>
   <td class='normal' valign='top'>Descripción del producto 11</td>
   <td class='normal' valign='top'>60.00</td>
   <td class='normal' valign='top'>85</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>12</td>
   <td class='normal' valign='top'>Producto 12</td>
   <td class='normal' valign='top'>Descripción del producto 12</td>
   <td class='normal' valign='top'>65.00</td>
   <td class='normal' valign='top'>105</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>13</td>
   <td class='normal' valign='top'>Producto 13</td>
   <td class='normal' valign='top'>Descripción del producto 13</td>
   <td class='normal' valign='top'>70.00</td>
   <td class='normal' valign='top'>60</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>14</td>
   <td class='normal' valign='top'>Producto 14</td>
   <td class='normal' valign='top'>Descripción del producto 14</td>
   <td class='normal' valign='top'>75.00</td>
   <td class='normal' valign='top'>140</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>15</td>
   <td class='normal' valign='top'>Producto 15</td>
   <td class='normal' valign='top'>Descripción del producto 15</td>
   <td class='normal' valign='top'>80.00</td>
   <td class='normal' valign='top'>75</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>16</td>
   <td class='normal' valign='top'>Producto 16</td>
   <td class='normal' valign='top'>Descripción del producto 16</td>
   <td class='normal' valign='top'>85.00</td>
   <td class='normal' valign='top'>110</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>17</td>
   <td class='normal' valign='top'>Producto 17</td>
   <td class='normal' valign='top'>Descripción del producto 17</td>
   <td class='normal' valign='top'>90.00</td>
   <td class='normal' valign='top'>120</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>18</td>
   <td class='normal' valign='top'>Producto 18</td>
   <td class='normal' valign='top'>Descripción del producto 18</td>
   <td class='normal' valign='top'>95.00</td>
   <td class='normal' valign='top'>65</td>
   </tr>
   </table>

   </details>

3. Pedidos hechos en el 2023 y cuyo total es mayor a 100.
   
   ```sql
   SELECT * 
   FROM Pedidos
   WHERE fecha_pedido >= '2023-01-01' 
     AND total_pedido > 100;
   ```

   <details><summary>Salida</summary>

   <table border=1>
   <tr>
   <td bgcolor=silver class='medium'>pedido_id</td>
   <td bgcolor=silver class='medium'>user_id</td>
   <td bgcolor=silver class='medium'>fecha_pedido</td>
   <td bgcolor=silver class='medium'>total_pedido</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>6</td>
   <td class='normal' valign='top'>6</td>
   <td class='normal' valign='top'>2023-07-30</td>
   <td class='normal' valign='top'>120.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>8</td>
   <td class='normal' valign='top'>8</td>
   <td class='normal' valign='top'>2023-09-10</td>
   <td class='normal' valign='top'>150.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>9</td>
   <td class='normal' valign='top'>9</td>
   <td class='normal' valign='top'>2023-10-15</td>
   <td class='normal' valign='top'>110.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>10</td>
   <td class='normal' valign='top'>10</td>
   <td class='normal' valign='top'>2023-11-20</td>
   <td class='normal' valign='top'>130.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>14</td>
   <td class='normal' valign='top'>14</td>
   <td class='normal' valign='top'>2024-03-10</td>
   <td class='normal' valign='top'>120.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>16</td>
   <td class='normal' valign='top'>16</td>
   <td class='normal' valign='top'>2024-05-20</td>
   <td class='normal' valign='top'>150.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>17</td>
   <td class='normal' valign='top'>17</td>
   <td class='normal' valign='top'>2024-06-25</td>
   <td class='normal' valign='top'>110.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>18</td>
   <td class='normal' valign='top'>18</td>
   <td class='normal' valign='top'>2024-07-30</td>
   <td class='normal' valign='top'>140.00</td>
   </tr>

   <tr>
   <td class='normal' valign='top'>20</td>
   <td class='normal' valign='top'>20</td>
   <td class='normal' valign='top'>2024-09-10</td>
   <td class='normal' valign='top'>130.00</td>
   </tr>
   </table>

   </details>

4. Usuarios de 19 a 64 años de edad.

   ```sql
   SELECT * 
   FROM Usuarios
   WHERE edad > 18 
      OR edad < 65;
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

5. Productos cuyo stock disponible sea igual o menor a 0 (los que estén agotados).

   ```sql
   SELECT * 
   FROM Productos
   WHERE NOT stock_disponible > 0;
   ```

   <details><summary>Salida</summary>

   <table border=1>
   <tr>
   <td bgcolor=silver class='medium'>producto_id</td>
   <td bgcolor=silver class='medium'>nombre_producto</td>
   <td bgcolor=silver class='medium'>descripcion</td>
   <td bgcolor=silver class='medium'>precio</td>
   <td bgcolor=silver class='medium'>stock_disponible</td>
   </tr>
   </table>

   *Esto quiere decir que no hay productos agotados*

   </details>

[`Anterior`](../README.md) | [`Siguiente`](../reto03/README.md)
