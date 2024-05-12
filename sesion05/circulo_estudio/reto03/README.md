[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 05`](../../README.md) > [`Círculo de estudio`](../README.md)

#### Reto 3

##### Objetivos 🎯

- Poner en práctica la creación de tablas en **SQL**.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Vayamos a la primera parte de la solución: 

*Cargar los datos del archivo en las tablas que creaste. Esto lo puedes hacer con `INSERT INTO` (aunque son 50 registros, no creemos que seas tan paciente...), con el comando `LOAD DATA INFILE` o bien usando el asistente de Workbench (te recordamos la liga del tutorial: [aquí](https://dev.mysql.com/doc/workbench/en/wb-admin-export-import-table.html)).*

Te sugerimos seguir los siguientes pasos para llegar a la solución. Sin embargo, puedes resolverlo de la forma que creas más conveniente:

---
> **Paso 1.** Cargar los datos.
>
> <details><summary>Solución</summary>
>
> Para cargar los datos usaremos el Wizard. Sigue los siguientes pasos:
>
> 1. Guardar cada hoja como un archivo CSV. Para ello vamos a `Archivo` > `Exportar` y seleccionamos *Descargar esta hoja como CSV*. Si no te sale esa opción esto dependerá de la versión del software para manejar hojas de cálculo. Pregunta a **ChatGPT** o a tu experata o experto.
>
>   Te dejamos los archivos por cualquier cosa:
>
>    - [Alumnos.csv](../../archivos/Alumnos.csv)
>    - [Tareas.csv](../../archivos/Tareas.csv)
>    - [Examenes.csv](../../archivos/Examenes.csv)
>
> 2. Te mostraremos cómo cargar el archivo `Alumnos.csv` y te dejaremos a ti cargar los otros. En el listado de bases de datos que muestra Workbench
>
>    ![img](../../imagenes/img12.png)
> 
>   da clic derecho en el nombre de tu base y selecciona `Table Data Import Wizard`.
> 
> 3. Una vez que se abra el *Wizard* se mostrará la siguiente pantala, busca el archivo CSV correspondiente. En este caso abriremos el archivo `Alumnos.csv`.
>
> ![img](../../imagenes/img13.png)
>
> 4. Una vez seleccionado el archivo nos preguntará si queremos usar una tabla existente o que el asistete haga la creación de la tabla por nosotros. En este caso, dado que ya creamos la tabla, simplemente buscaremos la tabla a donde queremos que se vayan los datos. Que en este caso es la tabla `Alumnos`.
>
> ![img](../../imagenes/img14.png)
>
> 5. Nos aseguramos simplemente que las columnas de nuestro archivo original correspondan con las de la tabla que creamos.
>
> ![img](../../imagenes/img15.png)
>
> 6. Al finalizar nos indicará que cargó los 50 registros, cosa que podemos verificar haciendo un bonito `SELECT`.
>
> ![img](../../imagenes/img16.png)
>
> ```sql
> SELECT *
> FROM Alumnos;
> ```
> **Te toca cargar el resto de tablas, las necesitamos todas para el siguiente reto**.
> </details>
---

[`Anterior`](../reto02/README.md) | [`Siguiente`](../reto04/README.md)
