[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 05`](../../README.md) > [`Normalización de datos`](../README.md)

#### Ejemplo 2

##### Objetivos 🎯

- Analizar si una base de datos se encuentra normalizados.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

En este ejemplo validareos si la base de datos `tienda` que hemos empleado a lo largo del módulo se encuentra normalizadas y lo haremos analizando cada una de las formas normales. Usaremos el diagrama entidad-relación que generamos en el [Ejemplo 1](../../tema01/ejemplo01/README.md). Te sugerimos tenerlo a la mano en todo el ejemplo.

![img](../../imagenes/img06.png)

##### 1ra Forma Normal (1FN)
Establece que los valores de cada columna deben ser atómicos, es decir, no deben tener estructura interna. Esto significa que cada celda en una tabla debe contener un sólo valor y no debe estar compuesta por múltiples valores separados por comas u otros delimitadores.

Nuestra base de datos cumple con esta forma normal, lo cual podemos validar revisando el diagrama entidad-relación. Todos los campos son atómicos.

Algunas personas consideran que las fechas no son valores atómicos por lo que deberíamos separar el día, el mes y el año. Sin embargo, los gestores de bases de datos más populares (como **MySQL**) han añadido operaciones para manipular estos valores por separado sin necesidad de desglosar estos datos y tratar a las fechas (`DATE`) como valores atómicos.

##### 2da Forma Normal (2FN)
Establece que una tabla debe cumplir con la primera forma normal :white_check_mark: y además, todos los campos que no sean llaves depen depender completamente de la llave primaria de la tabla. Esto significa que no debe haber dependencias parciales, es decir, cada atributo no llave depe depender de toda la clave primera y no de sólo una parte de ella.

En este caso analizaremos un campo de la tabla `Usuarios`:

- El campo `nombre` depende completamente de la llave `user_id`, pues por ejemplo si tuvieramos el nombre "Pedrito" :zap: en dos registros, podemos saber perfectamente a qué usuario por medio de la llave. 

Lo mismo pasa con el resto de campos en todas las tablas, lo cual puedes comprobar. La receta para entenderlo es *si tomo un campo y no me queda claro a qué registro pertenece al añadir la llave primaria no cumple con la segunda forma normal*.

##### 3ra Forma Normal (3FN)

Establece que una tabla debe cumplir con la segunda forma normal :white_check_mark: y además, ningún campo no llave debe depender transitivamente de la llave primaria de la tabla, es decir, ningún campo no llave debe depende de otro campo mas que de la llave primaria.

En este caso analizaremos un caso que suele ser un punto de confusión en el diseño de muchas bases de datos hoy en día.

En la tabla `Usuarios`, nuevamente, tenemos un campo llamado `correo_electronico`. Este campo puede tener una transitividad, por ejemplo, supongamos que obtenemos varios usuarios con la edad `18`, si los relacionamos con el correo podemos distinguir perfectamente a qué usuario nos referimos y de hecho podemos obtener la llave primaria a partir del correo electrónico.

A simple vista, podemos decir que la base de datos tiene una tabla que no cumple con la 3FN. Sin embargo, muchos sistemas hoy en día permiten el registro de más de un usuario con el mismo correo electrónico, lo cuál haría que el correo electrónico no pueda generar transitividades hacia la llave primaria. Consideraremos que esa funcionalidad es permitida en nuestra base :wink: y por lo tanto cumple la 3FN.

##### 4ta Forma Normal (4FN) y / 5ta Forma Normal (5FN)

La cuarta y quinta forma normal se consideran formas normales avanzadas y abordan situaciones más específicas y complejas en cuanto a la estructura y la integridad de los datos. Nuestra base no está en esos casos.

Las primeras tres formas normales son fundamentales para eliminar redundancias y anomalías en los datos, lo que promueve la consistencia y la integridad de la base de datos. Por lo tanto, es común que las personas encargadas del diseño de bases de datos se centren en alcanzar al menos la tercera forma normal para garantizar una base de datos bien estructurada y eficiente.

Sin embargo, en ciertos casos, especialmente en bases de datos más grandes y complejas, puede ser necesario diseñar más allá de las tres primeras formas normales para abordar requisitos específicos de negocio, optimizar el rendimiento o cumplir con estándares de calidad de datos más rigurosos.

[`Anterior`](../README.md) | [`Siguiente`](../../tema03/README.md)