[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 07`](../README.md)

### 7.3 Agrupamientos

<img src="https://github.com/beduExpert/A1-Introduccion-a-Bases-de-Datos-MASIVO2021/raw/main/Sesion-07/imagenes/imagen1.jpg" width="50%" align="right" hspace=30 vspace=30>

*Recordemos del prework que...*

👉 Al igual que en __SQL__ en __MongoDB__ podemos realizar agrupamientos. Se realizan mediante la agregación `$group` y tienen la siguiente sintaxis:

```json
{
  $group:
    {
      _id: <expression>, // Group By Expression
      <field1>: { <accumulator1> : <expression1> },
      ...
    }
 }
```

#### 🧐 Actividades

- [`Ejemplo 3`](ejemplo03/README.md)
- [`Reto 3`](reto03/README.md)

<br/>

[`Anterior`](../tema02/ejemplo02/README.md) | [`Siguiente`](ejemplo03/README.md)
