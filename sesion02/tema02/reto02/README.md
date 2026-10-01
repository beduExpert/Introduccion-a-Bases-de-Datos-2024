[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 02`](../../README.md) > [`Agrupamientos`](../README.md)

#### Reto 2

##### Objetivos 🎯

- Integrar el uso de funciones de agregación y agrupamiento en consultas SQL.
- Utilizar `SUM()` para obtener totales.
- Utilizar `GROUP BY` para agrupar información.
- Utilizar `HAVING` para filtrar resultados agrupados.
- Utilizar `ORDER BY` para ordenar los resultados.
- Resolver consultas a partir de preguntas de análisis de datos.

##### Requisitos 📋

- MySQL Workbench instalado.
- Base de datos `tienda` disponible.
- Conocimientos básicos de:
  - `SELECT`
  - `FROM`
  - `WHERE`
  - `GROUP BY`
  - `HAVING`
  - `ORDER BY`
  - Funciones de agregación (`SUM`, `COUNT`, `AVG`, `MIN`, `MAX`).

##### Desarrollo 🚀

A partir de las tablas disponibles en la base de datos `tienda`, realiza las siguientes consultas:

**Consulta 1:**  
Obtén el total de unidades vendidas por producto. Muestra el identificador del producto y la cantidad total de unidades vendidas.

**Consulta 2:**  
Obtén únicamente los productos cuya cantidad total de unidades vendidas sea mayor a 10.

**Consulta 3:**  
Ordena los resultados de la consulta anterior de mayor a menor, mostrando primero los productos con mayor cantidad de unidades vendidas.

**Consulta 4:**  
Integra los conceptos anteriores en una sola consulta que permita obtener:

- El identificador del producto.
- La cantidad total de unidades vendidas.
- Únicamente los productos con más de 10 unidades vendidas.
- Los resultados ordenados de mayor a menor cantidad de unidades vendidas.

##### Reflexiona 💡

Antes de escribir cada consulta, piensa:

1. ¿Qué información necesito obtener?
2. ¿De qué tabla proviene esa información?
3. ¿Necesito realizar algún cálculo sobre los datos?
4. ¿Qué función de agregación necesito utilizar?
5. ¿Por qué necesito utilizar `GROUP BY`?
6. ¿Estoy filtrando registros individuales o grupos?
7. ¿Qué cláusula debo utilizar para filtrar grupos?
8. ¿Por qué utilizar `ORDER BY`?
9. ¿Qué columna necesito utilizar para ordenar los resultados?

##### Pista 🔎

Para resolver la **Consulta 4**, considera la siguiente estructura:

```sql
SELECT ...
FROM ...
GROUP BY ...
HAVING ...
ORDER BY ...;

[`Anterior`](../ejemplo02/README.md) | [`Siguiente`](../../tema03/README.md)
