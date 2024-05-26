[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 07`](../README.md)

### 7.4. Asociación de colecciones

<img src="https://github.com/beduExpert/A1-Introduccion-a-Bases-de-Datos-MASIVO2021/raw/main/Sesion-07/imagenes/imagen2.jpg" width="50%" align="right" hspace=30>

*Recordemos del prework que...*

👉 De la misma forma en que __SQL__ incluye distintos tipos de *join*.

👉 En __MongoDB__ se tiene la operación `$lookup` que permite relacionar colecciones.

👉 Es una agregación y su sintaxis es la siguiente:

```json
{
   $lookup:
     {
       from: <collection to join>,
       localField: <field from the input documents>,
       foreignField: <field from the documents of the "from" collection>,
       as: <output array field>
     }
}
```

#### 🧐 Actividades

- [`Ejemplo 4`](ejemplo03/README.md)
- [`Reto 4`](reto01/README.md)

[`Anterior`](../tema03/reto03/README.md) | [`Siguiente`](ejemplo04/README.md)
