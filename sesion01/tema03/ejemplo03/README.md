#### Ejemplo 3: Filtrado básico

##### Objetivos 🎯

- Realizar algunas consultas sencillas.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

Veamos algunos ejemplos de filtros.

1. Usuarios mayores a 30 años:

   ```sql
   SELECT * 
   FROM Usuarios
   WHERE edad > 30;
   ```
2. Productos cuyo precio es menor a 100:

   ```sql
   SELECT * 
   FROM Productos
   WHERE precio < 100;
   ```

3. Pedidos hechos en el 2023 y cuyo total es mayor a 100.
   
   ```sql
   SELECT * 
   FROM Pedidos
   WHERE fecha_pedido >= '2023-01-01' 
     AND total_pedido > 100;
   ```

4. Usuarios de 19 a 64 años de edad.

   ```sql
   SELECT * 
   FROM Usuarios
   WHERE edad > 18 
      OR edad < 65;
   ```

5. Productos cuyo stock disponible sea igual o menor a 0 (los que estén agotados).

   ```sql
   SELECT * 
   FROM Productos
   WHERE NOT stock_disponible > 0;
   ```

[`Anterior`](../README.md) | [`Siguiente`](../reto03/README.md)
