[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas WHERE`](../README.md)

#### Ejemplo 3

##### Objetivos 🎯

- Realizar algunas consultas usando subconsultas dentro de la cláusula `WHERE`.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Queremos obtener el nombre de los usuarios que realizaron pedidos en una fecha específica (`'2024-04-15'`). Para lograrlo, utilizamos una subconsulta en la cláusula `WHERE` para filtrar los usuarios según esta condición.

```sql
SELECT user_id
FROM Pedidos
WHERE fecha_pedido = '2024-04-15';
```

Esta subconsulta selecciona los IDs de usuario (`user_id`) de la tabla `Pedidos` donde la fecha del pedido es igual a `'2024-04-15'`. Es decir, devuelve una lista de usuarios que realizaron pedidos en esa fecha específica.

Con esto podemos construir la consulta principal:

```sql
SELECT nombre
FROM Usuarios
WHERE user_id IN (SELECT user_id
                  FROM Pedidos
                  WHERE fecha_pedido = '2024-04-15');

```

---
> **Nota:** *La cláusula `IN` se utiliza en SQL para verificar si un valor determinado coincide con cualquiera de los valores proporcionados en una lista o subconsulta. Funciona de manera similar al operador `OR`, pero proporciona una forma más eficiente y legible de expresar la misma lógica. Mientras que el operador `OR` se utiliza para combinar múltiples condiciones en una expresión lógica, la cláusula `IN` se utiliza específicamente para comparar un valor con una lista de valores.*
---

La cláusula `WHERE` de la consulta principal utiliza la condición `IN` para filtrar los usuarios cuyos IDs (`user_id`) están presentes en la lista de IDs de usuario devueltos por la subconsulta. Esto asegura que sólo seleccionemos los usuarios que realizaron pedidos en la fecha específica.

La consulta principal devuelve el nombre de los usuarios que cumplieron con la condición especificada en la subconsulta, es decir, aquellos que realizaron pedidos en la fecha `'2024-04-15`.

Con este enfoque, hemos utilizado una subconsulta en la cláusula `WHERE` para filtrar los resultados de la consulta principal según la condición especificada. Esto nos permite realizar consultas más complejas y obtener resultados más especificos con base en condiciones dinámicas.

[`Anterior`](../README.md) | [`Siguiente`](../reto03/README.md)
