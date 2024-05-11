[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 04`](../README.md)

### 4.2. `LEFT` y `RIGHT JOIN`

<img src="imagenes/img01.png" width="50%" align="right" hspace=30>

<img src="imagenes/img02.png" width="50%" align="right" hspace=30>

*Recordemos del prework que...*

👉 `LEFT JOIN` y `RIGHT JOIN` son tipos de operaciones de combinación en SQL que permiten combinar registros de dos tablas basándose en una condición de coincidencia especificada. 

👉 La principal diferencia entre éstas instrucciones radica en cómo manejan los registros que no tienen correspondencia en la otra tabla:

- `LEFT JOIN` Devuelve todos los registros de la tabla izquierda (la primera mencionada en la consulta) y los registros coincidentes de la tabla derecha. Si no hay coincidencias en la tabla derecha, se devuelven `NULL` en las columnas correspondientes de esa tabla.

- `RIGHT JOIN` Devuelve todos los registros de la tabla derecha (la segunda mencionada en la consulta) y las filas coincidentes de la tabla izquierda. Si no hay coincidencias en la tabla izquierda, se devuelven `NULL` en las columnas correspondientes de esa tabla.

👉 En pocas palabras... `LEFT JOIN` asegura que todos los registros de la tabla izquierde esten presentes en el resultado, mientras que `RIGHT JOIN` asegura que todos los registros de la tabla derecha estén presentes en el resultado.

![img](../tema01/imagenes/img02.svg)

#### 🧐 Actividades

- [`Ejemplo 2`](ejemplo02/README.md)
- [`Reto 2`](reto02/README.md)

<br/>

[`Anterior`](../tema01/reto01/README.md) | [`Siguiente`](ejemplo02/README.md)
