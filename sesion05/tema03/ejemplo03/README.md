[`Introducción a Bases de Datos`](../../../README.md) > [`Sesión 05`](../../README.md) > [`Creación de tablas`](../README.md)

#### Ejemplo 3

##### Objetivos 🎯

- Ejemplificar cómo usar `CREATE TABLE` con datos reales.

##### Requisitos 📋

- MySQL Workbench instalado.

##### Desarrollo 🚀

A manera de ejemplo, te mostramos los comandos necesarios para crear todas las tablas de nuestra base de datos `tienda`:

```sql
-- Creación de la tabla Usuarios
CREATE TABLE Usuarios (
    user_id INT PRIMARY KEY,
    nombre VARCHAR(50),
    apellido VARCHAR(50),
    edad INT,
    correo_electronico VARCHAR(100),
    fecha_registro DATE
);

-- Creación de la tabla Pedidos
CREATE TABLE Pedidos (
    pedido_id INT PRIMARY KEY,
    user_id INT,
    fecha_pedido DATE,
    total_pedido DECIMAL(10, 2),
    FOREIGN KEY (user_id) REFERENCES Usuarios(user_id)
);

-- Creación de la tabla Productos
CREATE TABLE Productos (
    producto_id INT PRIMARY KEY,
    nombre_producto VARCHAR(100),
    descripcion TEXT,
    precio DECIMAL(10, 2),
    stock_disponible INT
);

-- Creación de la tabla Detalles_Pedido
CREATE TABLE Detalles_Pedido (
    detalle_id INT PRIMARY KEY,
    pedido_id INT,
    producto_id INT,
    cantidad INT,
    precio_unitario DECIMAL(10, 2),
    subtotal DECIMAL(10, 2),
    FOREIGN KEY (pedido_id) REFERENCES Pedidos(pedido_id),
    FOREIGN KEY (producto_id) REFERENCES Productos(producto_id)
);
```

No dudes en preguntar cualquier duda que tengas a tu experta o experto :wink:

[`Anterior`](../README.md) | [`Siguiente`](../../tema04/README.md)
