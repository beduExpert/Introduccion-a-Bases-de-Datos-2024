[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas SELECT`](../README.md)

#### Ejemplo 1

##### Objetivos 🎯

- Demostrar cómo utilizar subconsultas dentro de la cláusula `SELECT`.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos mostrar el nombre y correo electrónico de los usuarios junto con el total de pedidos que han realizado.


```sql
SELECT nombre,
       correo_electronico,
       (SELECT COUNT(*)
       	FROM Pedidos
       	WHERE Pedidos.user_id = Usuario.user_id) AS total_pedidos
FROM Usuarios;
```

<details><summary>Salida</summary>


<table border=1>
<tr>
<td bgcolor=silver class='medium'>nombre</td>
<td bgcolor=silver class='medium'>correo_electronico</td>
<td bgcolor=silver class='medium'>total_pedidos</td>
</tr>

<tr>
<td class='normal' valign='top'>Juan</td>
<td class='normal' valign='top'>juan@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Maria</td>
<td class='normal' valign='top'>maria@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Carlos</td>
<td class='normal' valign='top'>carlos@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Ana</td>
<td class='normal' valign='top'>ana@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Pedro</td>
<td class='normal' valign='top'>pedro@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Laura</td>
<td class='normal' valign='top'>laura@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Diego</td>
<td class='normal' valign='top'>diego@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Sofia</td>
<td class='normal' valign='top'>sofia@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Elena</td>
<td class='normal' valign='top'>elena@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Alejandro</td>
<td class='normal' valign='top'>alejandro@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Marina</td>
<td class='normal' valign='top'>marina@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Javier</td>
<td class='normal' valign='top'>javier@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Lucia</td>
<td class='normal' valign='top'>lucia@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Manuel</td>
<td class='normal' valign='top'>manuel@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Luisa</td>
<td class='normal' valign='top'>luisa@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Miguel</td>
<td class='normal' valign='top'>miguel@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Carmen</td>
<td class='normal' valign='top'>carmen@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Raul</td>
<td class='normal' valign='top'>raul@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Patricia</td>
<td class='normal' valign='top'>patricia@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>Daniel</td>
<td class='normal' valign='top'>daniel@example.com</td>
<td class='normal' valign='top'>1</td>
</tr>
</table>

</details>

En este ejemplo:

1. La subconsulta `SELECT` se encuentra dentro de la lista de selección.

2. La subconsulta cuenta el número de pedidos para cada usuario utilizando `COUNT(*)`.

3. La condición `WHERE` dentro de la subconsulta asegura que sólo se cuenten los pedidos del usuario correspondiente al usuario en la fila actual de la tabla `Usuarios`.

4. El resultado de la subconsulta, es decir, el total de pedidos para cada usuario, se muestra como una columna llamada `total_pedidos` junto con el nombre y el correo electrónico del usuario en la consulta principal.

[`Anterior`](../README.md) | [`Siguiente`](../reto01/README.md)
