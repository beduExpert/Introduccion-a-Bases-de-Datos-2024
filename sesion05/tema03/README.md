[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../README.md)

### Creación de tablas

*Recordemos del prework que...*

👉 La estructura básica de la instrucción `CREATE TABLE` en SQL se utiliza para crear una nueva tabla en una base de datos.

👉 Su sintaxis es la siguiente:

   ```sql
   CREATE TABLE nombre_tabla (
    columna1 tipo_dato restricciones,
    columna2 tipo_dato restricciones,
    ...
    FOREIGN KEY (llave_foranea) REFERENCES otra_tabla (columna_pk),
    ... 
   );
   ```

   - `nombre_tabla` Es el nombre que se le dará a la nueva tabla.
   - `columna1`, `columna2`, ... Son los nombres de las columnas que se van a crear en la tabla.
   - `tipo_dato` Es el tipo de datos que almacenará la columna (`varchar`, `int`, `date`, etc.).
   - `restricciones`: Son las restricciones que se pueden aplicar a la columna (`NOT NULL`, `UNIQUE`, `PRIMARY KEY`, etc.).
   - `FOREIGN KEY (llave_foranea) REFERENCES otra_tabla (columna_pk)` Define una llave foránea para asegurar la integridad referencial entre dos tablas.

#### 🧐 Actividades

- [`Ejemplo 3`](ejemplo03/README.md)

<br/>

[`Anterior`](../tema02/ejemplo02/README.md) | [`Siguiente`](ejemplo03/README.md)
