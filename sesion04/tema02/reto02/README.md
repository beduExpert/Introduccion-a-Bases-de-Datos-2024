[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`LEFT y RIGHT JOIN`](../README.md)

#### Reto 2

##### Objetivos 🎯

- Aplicar `LEFT JOIN` o `RIGHT JOIN` para combinar información de múltiples tablas relacionadas en una base de datos.

- Utilizar `GROUP BY` para agregar y resumir datos de manera significativa.

- Reforzar la comprensión de los conceptos de `JOIN` y `GROUP BY` y su aplicación en consultas complejas. 

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Muestra todos los usuarios y, si tienen pedidos, muestra también el pedido_id.
Queremos que aparezcan incluso los usuarios que nunca han realizado un pedido.

💡 Pista
Necesitas:
- Usuarios
- Pedidos
- LEFT JOIN

**Ejercicio: LEFT JOIN para combinar usuarios, pedidos y detalles de pedidos**
as necesarias para obtener información sobre los usuarios, los pedidos y los detalles de los pedidos, como el nombre del usuario, la fecha del pedido, el nombre del producto y la cantidad comprada.

- Utiliza `GROUP BY` para agrupar los resultados por usuario y fecha del pedido, y calcular el total de productos comprados por cada usuario en cada fecha.

- ¿Cómo prodrías resolver este ejercicio con `RIGHT JOIN`?


Se espera que con este ejercicio comprendas cómo utilizar `LEFT JOIN` y/o `RIGHT JOIN` para combinar información de múltiples tablas relacionadas en una base de datos, y cómo utilizar `GROUP BY` para agregar y resumir datos de manera significativa. Además se espera que comprendas la importancia de entender la estructura de las tablas y las relaciones entre ellas para realizar consultas avanzadas. Este ejercicio te permitirá practicar la aplicación de cruces y `GROUP BY` en escenarios reales y desarrollar habilidades para realizar análisis sofísticados de datos.


[`Anterior`](../ejemplo02/README.md) | [`Siguiente`](../../tema03/README.md)
