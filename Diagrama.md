# Tienda de Ropa - Diagrama Entidad-Relación (ERD)

```mermaid
erDiagram
    productos {
        INT id PK
        VARCHAR nombre
        VARCHAR descripcion
        DECIMAL precio
        VARCHAR talla
        VARCHAR color
        INT cantidad_stock
    }
    clientes {
        INT id PK
        VARCHAR nombre
        VARCHAR direccion
        VARCHAR telefono
        VARCHAR correo_electronico
    }
    empleados {
        INT id PK
        VARCHAR nombre
        VARCHAR direccion
        VARCHAR telefono
        VARCHAR correo_electronico
        VARCHAR cargo
    }
    ventas {
        INT id PK
        DATE fecha
        INT cliente_id FK
        INT producto_id FK
        INT cantidad
        DECIMAL precio_total
    }

    productos ||--o{ ventas : "es comprado en"
    clientes ||--o{ ventas : "realiza"
    empleados ||--o{ ventas : "puede gestionar"
