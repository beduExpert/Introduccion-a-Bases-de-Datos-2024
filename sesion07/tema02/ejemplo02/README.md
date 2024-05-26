[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 07`](../../README.md) > [`Introducción a las agregaciones`](../README.md)

#### Ejemplo 2

##### Objetivos 🎯

- Entender el concepto de agregación y su similitud con los agrupamientos y subconsultas de __SQL__.

##### Requisitos 📋

1. MongoDB Compass instalado.

##### Desarrollo 🚀

Cuando revisamos __SQL__ usamos agrupamientos que aplicaban una función a una columna reduciéndola a un valor que podía ser una suma, un conteo o calcular un promedio, por ejemplo. 

En __MongoDB__ podemos realizar lo mismo mediante el uso de agregaciones. Las agregaciones, permiten realizar distintos filtros usando *capas*. Una capa es el resultado de la aplicación de algún filtro, proyección, agrupamiento, ordienamiento, etc. Cada capa puede usarse en una nueva capa. La primera capa siempre será la colección completa.

Al conjunto de capas generadas en una agregación se le conoce como *pipeline*.

Por ejemplo, queremos saber cuál es la propiedad con mayor número de servicios (`amenities`) de la colección `sample_airbnb.listingsAndReviews`. Para usar agregaciones, daremos clic en la pestaña `Aggregations` de Compass. 

- Primero debemos obtener la longitud del arreglo `amenities` para saber el número de servicios de cada documento. Para esto, seleccionamos `addFields` en la primera capa.

   Con `addFields` podemos agregar campos como resultado de aplicar funciones a otros campos de la colección. De esta forma agregaremos el tamaño del arreglo como columna.
   
   Llamaremos a este campo `servicios` y para calcularlo usaremos la función `$size`. 
   
   ```json
   {
      servicios: {$size: "$amenities"}
   }
   ```
   
   ![imagen](../../imagenes/img04.png)
   
- Como el único dato que nos interesa es el número de servicios, sólo proyectaremos este resultado, para esto crearemos una nueva capa con `Add Stage` y elegiremos `$project`. Proyectamos el campo `name` y  `servicios` poniendo un `1` y quitamos el campo `_id` poniendo un 0.

   ```json
   {
      name: 1,
      servicios: 1,
      _id: 0
   }
   ```
   
   ![imagen](../../imagenes/img05.png)
   
- Ahora lo ordenamos añadiendo otra capa y usando `$sort`, recuerda -1 para descendente, 1 para ascendente.

   ```json
   {
      servicios: -1
   }
   ```
   
   ![imagen](../../imagenes/img06.png)
   
- Finalmente, limitamos la consulta a un registro usando `$limit`.

   ```json
   {
      1
   }
   ```
   
   ![imagen](../../imagenes/img07.png)

[`Anterior`](../README.md) | [`Siguiente`](../reto02/README.md)