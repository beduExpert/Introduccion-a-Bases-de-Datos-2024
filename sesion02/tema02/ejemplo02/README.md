[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 02`](../../README.md) > [`Agrupamientos`](../README.md)

#### Ejemplo 2

##### Objetivos 🎯

- Demostrar cómo se pueden realizar consultas aprovechando las funciones de agregación y agrupamiento para analizar datos dentro de una tabla.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos obtener la cantidad total de pedidos realizados por cada usuario en la tabla "Pedidos". Podemos usar la cláusula `GROUP BY` para agrupar los pedidos por usuario y la función de agregación `COUNT` para conter el número de pedidos por usuario.

```sql
SELECT user_id, 
       COUNT(*) AS Total_Pedidos
FROM Pedidos
GROUP BY user_id;
```
<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>user_id</td>
<td bgcolor=silver class='medium'>Total_Pedidos</td>
</tr>

<tr>
<td class='normal' valign='top'>1</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>2</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>4</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>5</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>7</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>8</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>9</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>10</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>11</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>12</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>13</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>14</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>15</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>16</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>17</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>18</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>19</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>20</td>
<td class='normal' valign='top'>1</td>
</tr>
</table>


</details>

Veamos otras consultas del mismo tipo.

**Consulta:** Total de ventas por producto.

```sql
SELECT producto_id, 
       SUM(cantidad) AS Total_Ventas
FROM Detalles_Pedido
GROUP BY producto_id;
```

<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>producto_id</td>
<td bgcolor=silver class='medium'>Total_Ventas</td>
</tr>

<tr>
<td class='normal' valign='top'>1</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>2</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>3</td>
</tr>

<tr>
<td class='normal' valign='top'>4</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>5</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>4</td>
</tr>

<tr>
<td class='normal' valign='top'>7</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>8</td>
<td class='normal' valign='top'>3</td>
</tr>

<tr>
<td class='normal' valign='top'>9</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>10</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>11</td>
<td class='normal' valign='top'>3</td>
</tr>

<tr>
<td class='normal' valign='top'>12</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>13</td>
<td class='normal' valign='top'>4</td>
</tr>

<tr>
<td class='normal' valign='top'>14</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>15</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>16</td>
<td class='normal' valign='top'>3</td>
</tr>

<tr>
<td class='normal' valign='top'>17</td>
<td class='normal' valign='top'>2</td>
</tr>

<tr>
<td class='normal' valign='top'>18</td>
<td class='normal' valign='top'>4</td>
</tr>

<tr>
<td class='normal' valign='top'>19</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>20</td>
<td class='normal' valign='top'>2</td>
</tr>
</table>

</details>

**Consulta:** Promedio de edad de los usuarios por mes de registro.

```sql
SELECT MONTH(fecha_registro)  AS Mes_Registro, 
       AVG(edad)              AS Promedio_Edad
FROM Usuarios
GROUP BY MONTH(fecha_registro);
```

<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>Mes_Registro</td>
<td bgcolor=silver class='medium'>Promedio_Edad</td>
</tr>

<tr>
<td class='normal' valign='top'>1</td>
<td class='normal' valign='top'>28.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>2</td>
<td class='normal' valign='top'>33.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>25.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>4</td>
<td class='normal' valign='top'>35.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>5</td>
<td class='normal' valign='top'>32.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>33.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>7</td>
<td class='normal' valign='top'>30.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>8</td>
<td class='normal' valign='top'>26.5000</td>
</tr>

<tr>
<td class='normal' valign='top'>9</td>
<td class='normal' valign='top'>29.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>10</td>
<td class='normal' valign='top'>31.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>11</td>
<td class='normal' valign='top'>26.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>12</td>
<td class='normal' valign='top'>34.0000</td>
</tr>
</table>

</details>

---
> **Nota:** *La función `MONTH` de MySQL extrae el componente de mes de una fecha dada. Por ejemplo, si le proporcionas una fecha como argumento, te devolverá el número del mes correspondiente a esa fecha. Es útil cuando necesitas trabajar con fechas y solo te interesa extraer la información del mes.*
---

**Consulta:** Cantidad de pedidos por día de la semana.

```sql
SELECT DAYOFWEEK(fecha_pedido) AS Dia_Semana, 
       COUNT(*)                AS Total_Pedidos
FROM Pedidos
GROUP BY DAYOFWEEK(fecha_pedido)
ORDER BY Dia_Semana;
```

<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>Dia_Semana</td>
<td bgcolor=silver class='medium'>Total_Pedidos</td>
</tr>

<tr>
<td class='normal' valign='top'>1</td>
<td class='normal' valign='top'>6</td>
</tr>

<tr>
<td class='normal' valign='top'>2</td>
<td class='normal' valign='top'>6</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>4</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>1</td>
</tr>

<tr>
<td class='normal' valign='top'>7</td>
<td class='normal' valign='top'>3</td>
</tr>
</table>

</details>

---
> **Nota:** *La función `DAYOFWEEK` de MySQL devuelve el día de la semana correspondiente a una fecha dada, donde el lunes se representa como 1 y el domingo como 7. Por ejemplo, si le proporcionas una fecha, la función te dirá qué día de la semana es, desde el lunes hasta el domingo. Es útil para realizar análisis basados en los días de la semana en conjuntos de datos que contienen fechas.*
---

[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)
