[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 04`](../../README.md) > [`UNION e INTERSECT`](../README.md)

#### Ejemplo 3

##### Objetivos 🎯

- Utilizar `UNION` para combinar y comparar conjuntos de resultados de consultas SQL.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Supongamos que queremos categorizar a nuestros usuarios de acuerdo al grupo de edad. Para ello añadiremos tres etiquetas a nuestra tabla de usuarios en una nueva columna a la que llamaremos `categoria` que dependerá de los rangos de edad:

- Adultos jóvenes (18 a 39)
- Adultos (40 a 59)
- Adultos mayores (60 en adelante)

Podemos usar `UNION` en este caso:

```sql
SELECT *,
       'Adulto joven' AS categoria
FROM Usuarios
WHERE edad BETWEEN 20 AND 39

UNION

SELECT *,
       'Adulto' AS categoria
FROM Usuarios
WHERE edad BETWEEN 40 AND 59

UNION

SELECT *,
       'Adulto mayor' AS categoria
FROM Usuarios
WHERE edad > 59
```

###### Conclusiones

- `UNION` combina conjuntos de resultados de consultas SQL y elimina duplicados.

[`Anterior`](../README.md) | [`Siguiente`](../reto03/README.md)
