[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas WHERE`](../README.md)
# 🔴 RETO 3 — El reto jefe final 👑

**“¿Quiénes son nuestros clientes frecuentes?”**

La tienda quiere encontrar los usuarios que han realizado más pedidos que el promedio de pedidos por usuario.

## Tu misión

Mostrar:
* `nombre`
* `apellido`
* `total_pedidos`

Pero **solamente** de los usuarios cuyo número de pedidos sea mayor al promedio.

## Aquí hay trampa 😈

Primero necesitas obtener algo como:

| Usuario | Pedidos |
| :--- | :--- |
| Ana | 5 |
| Luis | 2 |
| Pedro | 8 |
| Sofía | 4 |

Después calcular:
* `promedio de pedidos`

Y finalmente:
* ¿Quién está por encima del promedio?

## Reglas

* 🚫 No calcules el promedio manualmente.
* 🚫 No copies ningún número obtenido previamente.
* ✅ Debes utilizar subconsultas.

## Bonus nivel EXPERTA 🔥

Intenta resolverlo de dos maneras diferentes:
1. Utilizando una subconsulta en `FROM`
2. Utilizando una subconsulta correlacionada

Y después pregunta: **¿Cuál de las dos consultas me resulta más fácil de leer?**
*(Esto abre una conversación excelente sobre que SQL no consiste solamente en “que funcione”, sino también en escribir consultas mantenibles).*


[`Anterior`](../ejemplo03/README.md) | [`Siguiente`](../../../sesion04/README.md)
