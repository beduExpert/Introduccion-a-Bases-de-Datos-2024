[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../README.md)

### 5.4. Cargando los datos

<img src="imagenes/img01.png" width="50%" align="right" hspace=30>

*Recordemos del prework que...*

👉 `INSERT INTO` es una instrucción de **SQL** que se utiliza para insertar nuevos registros en una tabla existente. Su sintaxis básica es la siguiente:

   ```sql
   INSERT INTO nombre_tabla (columna1, columna2, ...)
   VALUES (valor1, valor2, ...);
   ```

   - `nombre_tabla`: Es el nombre de la tabla en la que se van a insertar los datos.
   - `columna1, columna2, ...`: Son los nombres de las columnas en los que se insertarán los valores.
   - `valor1, valor2, ...`: Son los valores que se van a insertar en las columnas correspondientes.

   Por ejemplo, para insertar un nuevo usuario en una tabla llamada "Usuarios", podríamos usar la siguiente sentencia `INSERT INTO`:

   ```sql
   INSERT INTO Usuarios (nombre, apellido, edad, correo_electronico, fecha_registro)
   VALUES ('Juan', 'Pérez', 30, 'juan@example.com', '2024-04-30');
   ```

👉 Por otro lado, `LOAD DATA INFILE` es una sentencia de **MySQL** que se utiliza para cargar datos de un archivo externo (como un archivo CSV o TEXT) en una tabla de la base de datos, su sintaxis básica es la siguiente:

```sql
LOAD DATA INFILE 'ruta_del_archivo' INTO TABLE nombre_tabla
FIELDS TERMINATED BY ',' ENCLOSED BY '"' LINES TERMINATED BY '\n';
```

- `ruta_del_archivo`: Es la ruta del archivo que contiene los datos a cargar.
- `nombre_tabla`: Es el nombre de la tabla en la que se cargarán los datos.
- `FIELDS TERMINATED BY ','`: Especifica el delimitador que separa los campos en el archivo (en este caso, una coma).
- `ENCLOSED BY '"'`: Especifica el carácter de encerramiento para los campos (en este caso, comillas dobles).
- `LINES TERMINATED BY '\n'`: Especifica el carácter que indica el final de cada línea en el archivo (en este caso, un salto de línea).

Por ejemplo, para cargar datos desde un archivo CSV llamado `datos.csv` en una tabla `Usuarios`, podríamos usar la siguiente sentencia `LOAD DATA INFILE`:

```sql
LOAD DATA INFILE 'datos.csv' INTO TABLE Usuarios
FIELDS TERMINATED BY ',' ENCLOSED BY '"' LINES TERMINATED BY '\n';
```

👉 Una tercera opción es usar un asistente para cargar los datos. En el caso de **Workbench** podríamos usar este por ejemplo: 

[Table Data Export and Import Wizard](https://dev.mysql.com/doc/workbench/en/wb-admin-export-import-table.html)


[`Anterior`](../tema02/reto03/README.md) | [`Siguiente`](../circulo_estudio/README.md)
