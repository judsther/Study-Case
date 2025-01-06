# Base de Datos para Tienda de Ropa

## Estructura de la Base de Datos

La base de datos se compone de cuatro tablas principales:

1. **Productos**:
   - Almacena información sobre los productos, como nombre, descripción, precio, talla, color y cantidad en stock.

2. **Clientes**:
   - Contiene datos sobre los clientes, incluyendo nombre, dirección, teléfono y correo electrónico.

3. **Empleados**:
   - Guarda información sobre los empleados, como nombre, dirección, teléfono, correo electrónico y cargo.

4. **Ventas**:
   - Registra las ventas realizadas, incluyendo la fecha, el cliente, el producto, la cantidad vendida y el precio total.

## Justificación del Diseño

- **Relaciones**:
  - Cada venta está vinculada a un cliente y un producto, permitiendo un historial claro y detallado.
- **Integridad Referencial**:
  - Uso de claves foráneas con restricciones `ON DELETE CASCADE` para garantizar la consistencia de los datos.
