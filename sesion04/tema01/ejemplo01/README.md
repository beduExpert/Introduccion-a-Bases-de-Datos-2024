[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`INNER JOIN`](../README.md)

#### Ejemplo 1

##### Objetivos 🎯

- Utilizar `INNER JOIN` para combinar información de dos tablas relacionadas en una base de datos.

##### Requisitos 📋

- MySQL Workbench instalado.

- Conocimientos básicos de SQL, incluyendo la sintaxis de `INNER JOIN` y la estructura de las tablas.

##### Desarrollo 🚀

Supongamos que tenemos una tienda en línea y queremos obtener información sobre los pedidos realizados por nuestros usuarios, incluyendo dus nombres y detalles de los productos que compraron.

1. Primero, debemos identificar qué columnas nos gustaría incluir en nuestro resultado. En este caso, queremos el nombre del usuario, la fecha del pedido y el total del pedido.

2. Utilizamos la cláusula `INNER JOIN` para combinar las tablas de `Usuarios` y `Pedidos` basándonos en la columna `user_id` que actúa como *llave foránea* (hablaremos de esto la próxima sesión) en la tabla `Pedidos` y la *llave primaria* en la tabla `Usuarios`.

3. Especificamos la condición de coincidencia utilizando utilizando la cláusula `ON`, donde indicamos que los `user_id` de ambas tablas deben ser iguales para que se incluyan en el resultado.

4. Seleccionamos las columnas deseadas de ambas tablas y ejecutamos la consulta.

##### Consulta SQL

```sql
SELECT Usuarios.nombre, 
       Usuarios.apellido, 
       Pedidos.fecha_pedido, 
       Pedidos.total_pedido
FROM Usuarios
INNER JOIN Pedidos 
  ON Usuarios.user_id = Pedidos.user_id;
```

Recordemos además que la palabra reservada `INNER` es opcional en MySQL: 

```sql
SELECT Usuarios.nombre, 
       Usuarios.apellido, 
       Pedidos.fecha_pedido, 
       Pedidos.total_pedido
FROM Usuarios
JOIN Pedidos 
  ON Usuarios.user_id = Pedidos.user_id;
```

También que si queremos, podemos poner un *alias* a los nombres de tablas.

En ocasiones necesitamos simplificar lo más que se pueda la sintaxis de las consultas para encontrar errores y facilitar la *depuración*.

```sql
SELECT u.nombre, 
       u.apellido, 
       p.fecha_pedido, 
       p.total_pedido
FROM Usuarios AS u
JOIN Pedidos  AS p
  ON u.user_id = p.user_id;
```

Nunca pierdas de vista la legibilidad cuando escribas una consulta.

<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>nombre</td>
<td bgcolor=silver class='medium'>apellido</td>
<td bgcolor=silver class='medium'>fecha_pedido</td>
<td bgcolor=silver class='medium'>total_pedido</td>
</tr>

<tr>
<td class='normal' valign='top'>Juan</td>
<td class='normal' valign='top'>Perez</td>
<td class='normal' valign='top'>2023-03-10</td>
<td class='normal' valign='top'>50.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Maria</td>
<td class='normal' valign='top'>Gomez</td>
<td class='normal' valign='top'>2023-03-12</td>
<td class='normal' valign='top'>70.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Carlos</td>
<td class='normal' valign='top'>Lopez</td>
<td class='normal' valign='top'>2023-04-15</td>
<td class='normal' valign='top'>90.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Ana</td>
<td class='normal' valign='top'>Martinez</td>
<td class='normal' valign='top'>2023-05-20</td>
<td class='normal' valign='top'>60.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Pedro</td>
<td class='normal' valign='top'>Rodriguez</td>
<td class='normal' valign='top'>2023-06-25</td>
<td class='normal' valign='top'>80.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Laura</td>
<td class='normal' valign='top'>Sanchez</td>
<td class='normal' valign='top'>2023-07-30</td>
<td class='normal' valign='top'>120.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Diego</td>
<td class='normal' valign='top'>Garcia</td>
<td class='normal' valign='top'>2023-08-05</td>
<td class='normal' valign='top'>100.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Sofia</td>
<td class='normal' valign='top'>Hernandez</td>
<td class='normal' valign='top'>2023-09-10</td>
<td class='normal' valign='top'>150.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Elena</td>
<td class='normal' valign='top'>Diaz</td>
<td class='normal' valign='top'>2023-10-15</td>
<td class='normal' valign='top'>110.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Alejandro</td>
<td class='normal' valign='top'>Torres</td>
<td class='normal' valign='top'>2023-11-20</td>
<td class='normal' valign='top'>130.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Marina</td>
<td class='normal' valign='top'>Ruiz</td>
<td class='normal' valign='top'>2023-12-25</td>
<td class='normal' valign='top'>70.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Javier</td>
<td class='normal' valign='top'>Flores</td>
<td class='normal' valign='top'>2024-01-30</td>
<td class='normal' valign='top'>90.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Lucia</td>
<td class='normal' valign='top'>Gutierrez</td>
<td class='normal' valign='top'>2024-02-05</td>
<td class='normal' valign='top'>100.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Manuel</td>
<td class='normal' valign='top'>Vazquez</td>
<td class='normal' valign='top'>2024-03-10</td>
<td class='normal' valign='top'>120.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Luisa</td>
<td class='normal' valign='top'>Moreno</td>
<td class='normal' valign='top'>2024-04-15</td>
<td class='normal' valign='top'>80.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Miguel</td>
<td class='normal' valign='top'>Jimenez</td>
<td class='normal' valign='top'>2024-05-20</td>
<td class='normal' valign='top'>150.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Carmen</td>
<td class='normal' valign='top'>Castillo</td>
<td class='normal' valign='top'>2024-06-25</td>
<td class='normal' valign='top'>110.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Raul</td>
<td class='normal' valign='top'>Navarro</td>
<td class='normal' valign='top'>2024-07-30</td>
<td class='normal' valign='top'>140.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Patricia</td>
<td class='normal' valign='top'>Garcia</td>
<td class='normal' valign='top'>2024-08-05</td>
<td class='normal' valign='top'>100.00</td>
</tr>

<tr>
<td class='normal' valign='top'>Daniel</td>
<td class='normal' valign='top'>Sanchez</td>
<td class='normal' valign='top'>2024-09-10</td>
<td class='normal' valign='top'>130.00</td>
</tr>
</table>


</details>

##### Conclusiones

- `INNER JOIN` nos permite combinar información de dos tablas relacionadas en una base de datos.

- La cláusula `ON` especifica la condición de coincidencia para la combinación de filas.

- Este tipo de `JOIN` nos ayuda a obtener datos relacionados de manera eficiente y precisa, lo que facilita el análisis y la extracción de información de nuestras bases de datos.

[`Anterior`](../README.md) | [`Siguiente`](../reto01/README.md)
