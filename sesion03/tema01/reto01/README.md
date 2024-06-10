[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas SELECT`](../README.md)

#### Reto 1

##### Objetivos 🎯

- Demostrar cómo utilizar subconsultas en la cláusula `SELECT`.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

**Consulta:**   
Escribe una subconsulta que muestre el nombre de cada producto junto con su precio unitario y la cantidad total vendida de ese producto en todos los pedidos.

Algunos tipos para hacer la consulta:

1. Tu subconsulta deberá calcular la cantidad total vendida de cada producto sumando todas las cantidades vendidas en los detalles de los pedidos correspondientes al producto en la fila actual de la tabla `Productos`.

2. Tu subconsulta puede incluir una condición `WHERE` dentro de la subconsulta asegure que sólo se sumen las cantidades vendidas del producto correspondiente al producto en la fila actual de la tabla `Productos`.

3. Muestra el resultado de la subconsulta, es decir, la cantidad total venida de cada producto, como una columna llamada `cantidad_total_vendida` o algo similar junto con el nombre y el precio unitario del producto en la consulta principal.

[`Anterior`](../ejemplo01/README.md) | [`Siguiente`](../../tema02/README.md)
