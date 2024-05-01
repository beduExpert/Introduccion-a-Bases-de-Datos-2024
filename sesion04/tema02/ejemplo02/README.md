[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`LEFT y RIGHT JOIN`](../README.md)

#### Ejemplo 2

##### Objetivos 🎯

- Utilizar `LEFT JOIN` y `RIGHT JOIN` para combinar información de dos tablas relacionadas en una base de datos.

- Comprender la diferencia entre `LEFT JOIN` y `RIGHT JOIN` y cuándo es apropiado utilizar cada uno.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos realizar un análisis de los pedidos y los productos vendidos en nuestra tienda en línea. Para ello necesitamos combinar información de las tablas `Pedidos` y `Detalles_Pedido` con la tabla `Productos`.

1. **`LEFT JOIN` para analizar pedidos y usuarios**

- Utilizaremos `LEFT JOIN` para combinar la tabla `Usuarios` con la tabla `Pedidos`, de manera que obtengamos todos los registros de la tabla `Usuarios` y los registros coincidentes de la tabla `Pedidos`, si los hay.

- Seleccionaremos las columnas necesarias para obtener información sobre los usuarios y sus pedidos, como el nombre del usuario, la fecha del pedido y el total del pedio.

```sql
SELECT u.nombre, 
       u.apellido, 
       p.fecha_pedido, 
       p.total_pedido
FROM      Usuarios AS u
LEFT JOIN Pedidos  AS p 
  ON u.user_id = p.user_id;
```

2. **`RIGHT JOIN` para analizar pedidos y productos y pedidos**

- Utilizaremos `RIGHT JOIN` para combinar la tabla `Productos` con la tabla `Detalles_Pedido` de manera que obtengamos todos los registros de la tabla `Productos` y los registros coincidentes de la tabla `Detalles_Pedido`, si las hay.

- Seleccionaremos las columnas necesarias para obtener información sobre los productos y los detalles de los pedidos, como el nombre del producto, la cantidad vendida y el precio unitario.

```sql
SELECT p.nombre_producto, 
       dp.cantidad, 
       dp.precio_unitario
FROM       Productos p
RIGHT JOIN Detalles_Pedido dp 
  ON p.producto_id = dp.producto_id;
```

##### Conclusiones

- `LEFT JOIN` y `RIGHT JOIN` son herramientas útiles para combinar información de dos tablas relacionadas en una base de datos.

- `LEFT JOIN` se utiliza cuando queremos incluir todas los registros de la tabla izquierda en el resultado, mientras que `RIGH JOIN` se utiliza cuando queremos incluir todos las registros de la tabla derecha.

- Al comprender la diferencia entre `LEFT JOIN` y `RIGHT JOIN`, podemos elegir la opción más adecuada según los requerimientos de nuestra consulta.

[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)
