[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`UNION e INTERSECT`](../README.md)

#### Ejemplo 3

##### Objetivos 🎯

- Utilizar `UNION` e `INTERSECT` para combinar y comparar conjuntos de resultados de consultas SQL.

- Comprender cómo funcionan `UNION` e `INTERSECT` y cuándo es apropiado utilizar cada uno.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos realizar un análisis de los clientes que han realizado pedidos y los clientes que han comprado productos de una categoría específica. Para ello, utilizaremos `UNION` e `INTERSECT` para combinar y comparar conjuntos de resultados de consultas SQL.

###### `UNION` para combinar clientes que han realizado pedidos

- Utilizaremos `UNION` para combinar los clientes que han realizado pedidos en la tabla `Pedidos`.

- Seleccionaremos el nombre y el apellido de los clientes de la tabla `Usuarios` que tienen pedidos registrados en la tabla `Pedidos`.

```sql
SELECT nombre, 
       apellido
FROM Usuarios
WHERE user_id IN (SELECT DISTINCT user_id FROM Pedidos)

UNION

SELECT nombre, 
       apellido
FROM Usuarios
WHERE user_id IN (SELECT DISTINCT user_id FROM Detalles_Pedido);
```

###### `INTERSECT` para comparar clientes que han comprado productos de una categoría específica

- Utilizaremos `INTERSECT` para comparar los clientes que han comprado productos de una categoría específica en la tabla `Productos`.

- Seleccionaremos el nombre y el apellido de los clientes de la tabla Usuarios que han comprado productos de la categoría `"Electrónicos"`.

```sql
SELECT nombre, 
       apellido
FROM Usuarios
WHERE user_id IN (SELECT user_id FROM Pedidos)

INTERSECT

SELECT U.nombre, U.apellido
FROM Usuarios                          AS U
JOIN Detalles_Pedido DP 
  ON U.user_id = DP.user_id
JOIN Productos                         AS P 
  ON DP.producto_id = P.producto_id
JOIN Categorias_Producto               AS CP 
  ON P.categoria_id = CP.categoria_id
WHERE CP.nombre_categoria = 'Electrónicos';
```

###### Conclusiones

- `UNION` combina conjuntos de resultados de consultas SQL y elimina duplicados.

- `INTERSECT` compara conjuntos de resultados de consultas SQL y devuelve las filas comunes a ambas consultas.

- La combinación de `UNION` e `INTERSECT` nos permite realizar análisis complejos y comparaciones entre conjuntos de datos en una base de datos relacional.

[`Anterior`](../README.md) | [`Siguiente`](../reto03/README.md)
