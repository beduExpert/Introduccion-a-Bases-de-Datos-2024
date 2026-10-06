[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 03`](../../README.md) > [`Subconsultas FROM`](../README.md)

# 🟡 RETO 2 — Detectives de pedidos

## Contexto

La tienda quiere detectar si hay pedidos que contienen productos que actualmente están agotados. 

## Tu misión

Obtén:

* `pedido_id`
* `fecha_pedido`

De los pedidos que contengan productos cuyo:
`stock_disponible = 0`

## Restricciones

Debes utilizar:
* ✅ Una subconsulta
* ✅ Y puedes necesitar 1 o más de una subconsulta

## Pistas

**Pista 1**
Primero encuentra: ¿Qué productos están agotados?
```sql
SELECT producto_id
FROM Productos
WHERE stock_disponible = 0;
```

**Pista 2**
Ahora pregunta: ¿Qué pedidos tienen esos productos?

## SUPER BONUS 🔥🔥

Intenta explicar tu consulta de adentro hacia afuera. No solamente ejecutes el código.



[`Anterior`](../ejemplo02/README.md) | [`Siguiente`](../../tema03/README.md)
