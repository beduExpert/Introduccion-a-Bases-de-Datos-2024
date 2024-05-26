[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 06`](../README.md)

### 6.3 Consultas básicas

*Recordemos del prework que...*

👉 En **MongoDB** los datos son almacenados en *colecciones* que incluyen doucmentos.

👉 Estos documentos se representan usando el formato de intercambio de información **JSON**.

👉 El formato **JSON** se conforma de un conjunto de elementos de la forma *clave-valor* separados por comas y delimitados por llaves.

👉 Los tipos de datos de **JSON** son:

- Números
- Booleanos
- Cadenas
- Arreglos
- Objetos

👉 Para realizar consultas u otras operaciones en **MongoDB** debe usarse este formato a manera de lenguaje (no es un lenguaje por sí mismo, pero lo usuaremos como si lo fuera). 

👉 En particular, para realizar proyecciones, se usa este formato. Debe indicarse el campo a proyectar y colocar un 1 si queremos mostrarlo o 0 en caso contrario.

```json
{campo: 0}
{campo: 1}
```

👉 Al igual que las proyeccciones, los filtros se construyen usando **JSON**.

👉 En su forma más simple se debe escribir el nombre del campo, dos puntos y el valor que queremos filtrar.

👉 Existen varias funciones que se pueden combinar con los filtros y las iremos estudiando en las sesiones faltantes.

```json
{campo: "valor"}
```

#### 🧐 Actividades

- [`Ejemplo 3`](ejemplo03/README.md)
- [`Reto 1`](reto01/README.md)

<br/>

[`Anterior`](../tema02/ejemplo02/README.md) | [`Siguiente`](ejemplo03/README.md)
