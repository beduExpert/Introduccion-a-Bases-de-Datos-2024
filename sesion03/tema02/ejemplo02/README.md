[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas FROM`](../README.md)

#### Ejemplo 2

##### Objetivos 🎯

- Demostrar cómo se pueden realizar consultas aprovechando las subconsultas dentro de la cláusula `FROM`.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos encontrar los productos cuyo promedio de solicitudes (ventas) sea mayor a 2. Analicemos esta consulta por partes.

Primero, necesitamos saber, cuantas solicitudes se han hecho por cada pedido. Esto puede hacer con la columna `cantidad` de la tabla `Detalles_Pedido`. Ahora, para obtener el promedio por cada producto, podemos usar la función de agregación `AVG` y la cláusula `GROUP BY`:

```sql
SELECT producto_id,
       AVG(cantidad) AS cantidad_promedio
FROM Detalles_Pedido
GROUP BY producto_id;
```
<details><summary>Salida</summary>

<table border=1>
<tr>
<td bgcolor=silver class='medium'>producto_id</td>
<td bgcolor=silver class='medium'>cantidad_promedio</td>
</tr>

<tr>
<td class='normal' valign='top'>1</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>2</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>4</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>5</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>4.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>7</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>8</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>9</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>10</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>11</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>12</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>13</td>
<td class='normal' valign='top'>4.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>14</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>15</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>16</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>17</td>
<td class='normal' valign='top'>2.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>18</td>
<td class='normal' valign='top'>4.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>19</td>
<td class='normal' valign='top'>1.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>20</td>
<td class='normal' valign='top'>2.0000</td>
</tr>
</table>


</details>

Podemos usar los resultados obtenidos como tabla temporal y consultar sobre dicha tabla cuáles son aquellos pedidos que tienen una cantidad promedio mayor a 2.

**Importante**: Cuando hacemos consultas de este tipo, es necesario colocar un alias a la subconsulta, de lo contrario MySQL reportará un error.

```sql
SELECT *
FROM (SELECT producto_id, AVG(cantidad) AS cantidad_promedio 
      FROM Detalles_Pedido 
      GROUP BY producto_id) AS subconsulta
WHERE subconsulta.cantidad_promedio > 2;    
```

<details><summary>Salida</summary>

<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"><title>Data</title>
</head>
<body>
<table border=1>
<tr>
<td bgcolor=silver class='medium'>producto_id</td>
<td bgcolor=silver class='medium'>cantidad_promedio</td>
</tr>

<tr>
<td class='normal' valign='top'>3</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>6</td>
<td class='normal' valign='top'>4.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>8</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>11</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>13</td>
<td class='normal' valign='top'>4.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>16</td>
<td class='normal' valign='top'>3.0000</td>
</tr>

<tr>
<td class='normal' valign='top'>18</td>
<td class='normal' valign='top'>4.0000</td>
</tr>
</table>
</body></html>


</details>

Quizá mientras desarrollemos el ejemplo, haya pasado por tu mente...

**Esto se puede hacer con `HAVING`...**

```sql
SELECT producto_id, 
       AVG(cantidad) AS cantidad_promedio 
FROM Detalles_Pedido 
GROUP BY producto_id
HAVING AVG(cantidad) > 2;    
```

Y tienes toda la razón. Esto sólo habla de que hay más de una manera de resolver el mismo problema pero apoyándonos de distintos comandos. La decisión de qué comando utilizar en cada ocasión dependerá de varios factores como la eficiencia de la consulta, el número de años de experiencia que lleves escribiendo consultas o las necesidades del proyecto o problema en particular. 

Algunas herramientas en la nube limitan los recursos que usas por ejemplo. En estos casos elegir de forma adecuada la cláusula o el tipo de consulta a usar es esencial. Sin embargo, dado que estamos aprendiendo por primera vez estos conceptos, no te preocupes mucho por esto de momento. :smile:

[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)
