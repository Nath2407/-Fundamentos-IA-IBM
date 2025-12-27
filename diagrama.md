```mermaid
flowchart TD
    A([Inicio]) --> B[Cargar archivos CSV<br/>clientes, productos, ventas, detalle_ventas]

    B --> C[Validar y limpiar datos<br/>• Valores nulos<br/>• Tipos de datos]
    C --> D[Integrar datos<br/>Ventas + Clientes<br/>Detalle + Productos<br/>Tabla analítica]

    D --> E[Mostrar menú principal]
    E --> F{Seleccionar opción}

    F -->|Opción 1| G[Información del conjunto de datos<br/>• Número de archivos<br/>• Registros y columnas<br/>• Tipos de datos]
    F -->|Opción 2| H[Resumen general de ventas<br/>• Ventas totales<br/>• Ticket promedio]
    F -->|Opción 3| I[Ventas por categoría<br/>Agrupación y totales]
    F -->|Opción 4| Z([Salir])

    G --> J{¿Regresar al menú?}
    H --> J
    I --> J

    J -->|Sí| E
    J -->|No| Z

    Z --> K([Fin])
