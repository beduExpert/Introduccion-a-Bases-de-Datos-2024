[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`Variantes`](../README.md)

#### Ejemplo 4

##### Objetivos 🎯

- Demostrar cómo usar `CROSS JOIN` para generar todas las combinaciones posibles entre dos conjuntos de datos.

- Comprender el impacto de `CROSS JOIN` en el tamaño del conjunto de resultados y la importancia de su uso prudente.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos generar todas las posibles combinaciones entre usuarios y productos para analizar las preferencias de compra de cada usuario. Utilizaremos `CROSS JOIN` para realizar esta tarea.

Utilizaremos `CROSS JOIN` para combinar cada usuario con cada producto disponible en la base de datos.

Seleccionaremos el nombre del usuario y nombre del producto para cada combinación generada.

```sql
SELECT U.nombre, 
       P.nombre_producto
FROM       Usuarios  AS U
CROSS JOIN Productos AS P;
```

`CROSS JOIN` genera todas las combinaciones posibles entre los conjuntos de datos especificados, multiplicando el número de registros en el conjunto de resultados.

Es importante usar `CROSS JOIN` con precaución, ya que puede resultar en conjuntos de resultados muy grandes y consultas ineficientes si no se controla adecuadamente.

`CROSS JOIN` puede se útil en situaciones específicas, como la generación de combinaciones o la creación de matrices de datos, pero debe utilizarse con cuidado para evitar problemas de rendimiento y resultados inesperados.

**¡Con esto concluimos el material de la Sesión 4!**

[`Anterior`](../README.md) | [`Siguiente`](../../../sesion05/README.md)

