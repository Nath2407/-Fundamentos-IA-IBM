```markdown

```
# Documentación

## Sprint 1

---
### 1. Tema, problema y solución

## Tema
**Optimización de ventas y gestión de inventario mediante análisis de datos de clientes y transacciones**

---

## Problema
La tienda cuenta con información distribuida en distintos archivos: clientes, ventas, detalles de venta y productos. Sin embargo, estos datos no se analizan de manera integrada, lo que genera diversas problemáticas operativas y estratégicas, entre ellas:

---

### Solución
Se propone integrar y analizar los archivos disponibles para transformar los datos en información útil para la toma de decisiones estratégicas y operativas.

### Integración de datos
- Relacionar las ventas con los detalles de venta para obtener el valor real de cada transacción.
- Vincular los productos con sus precios, categorías y niveles de venta.
- Asociar los clientes con su historial de compras.

### Análisis propuesto
- Segmentación de clientes según frecuencia de compra y monto gastado.
- Identificación de productos de alta y baja rotación.
- Análisis de tendencias y estacionalidad de ventas.
- Evaluación del desempeño de inventarios.

### Resultados esperados
- Mejora en la planeación y control de inventarios.
- Reducción de pérdidas por productos de baja rotación.
- Incremento en las ventas mediante decisiones basadas en datos.
- Mayor conocimiento del comportamiento del cliente.

### Entregable final
- Dashboard con indicadores clave de ventas, clientes y productos.
- Reporte ejecutivo con conclusiones y recomendaciones estratégicas.

### 2. Dataset de referencia

**Fuente:** Datos generados con fines educativos y de simulación analítica.

**Definición:**  
El conjunto de datos corresponde a un sistema transaccional de una tienda minorista, el cual integra información estructurada asociada al catálogo de productos, al registro de clientes y a las operaciones de venta. Estas bases de datos representan de manera consistente el flujo comercial de la tienda, desde la identificación de productos y clientes hasta el detalle de cada transacción realizada.
---
### 3. Estructura de archivos

El conjunto de datos se encuentra organizado en cuatro archivos principales en formato CSV, los cuales representan las entidades fundamentales del sistema transaccional de una tienda minorista. Cada archivo contiene variables claramente definidas, con tipos de datos y escalas de medición apropiadas para su análisis estadístico y analítico.

---

####Clientes (`clientes.csv`) — ~100 registros

Este archivo almacena la información de identificación y localización de los clientes registrados, así como la fecha de alta en el sistema, lo cual permite análisis de cohortes y antigüedad de clientes.

| Campo           | Tipo de dato | Escala de medición |
|-----------------|--------------|--------------------|
| id_cliente      | Entero       | Nominal            |
| nombre_cliente  | string       | Nominal            |
| email           | string       | Nominal            |
| ciudad          | string       | Nominal            |
| fecha_alta      | Fecha        | Intervalo          |

---

####Ventas (`ventas.csv`) — ~120 registros

Este archivo representa las transacciones de venta realizadas en la tienda. Incluye información temporal, datos del cliente y el medio de pago utilizado, permitiendo análisis de comportamiento de compra y métodos de pago.

| Campo          | Tipo de dato | Escala de medición |
|----------------|--------------|--------------------|
| id_venta       | Entero       | Nominal            |
| fecha          | Fecha        | Intervalo          |
| id_cliente     | Entero       | Nominal            |
| nombre_cliente | string       | Nominal            |
| email          | string       | Nominal            |
| medio_pago     | string       | Nominal            |

---


####Productos (`productos.csv`) — ~100 registros

Este archivo corresponde al catálogo de productos disponibles en la tienda.
Contiene información descriptiva y económica que permite el análisis de precios, categorías y desempeño por producto.

| Campo            | Tipo de dato | Escala de medición |
|------------------|--------------|--------------------|
| id_producto      | Entero       | Nominal            |
| nombre_producto  | string       | Nominal            |
| categoria        | string       | Nominal            |
| precio_unitario  | Numérico     | Razón              |

---

####Detalle de Ventas (`detalle_ventas.csv`) — ~343 registros

Este archivo contiene el desglose de cada transacción de venta a nivel de producto, permitiendo el análisis de cantidades vendidas, precios unitarios e importes totales por línea de venta.

| Campo           | Tipo de dato | Escala de medición |
|-----------------|--------------|--------------------|
| id_venta        | Entero       | Nominal            |
| id_producto     | Entero       | Nominal            |
| nombre_producto | Cadena       | Nominal            |
| cantidad        | Entero       | Razón              |
| precio_unitario | Numérico     | Razón              |
| importe         | Numérico     | Razón              |

---

**Nota técnica:**  
La estructura relacional de los archivos permite su integración mediante claves primarias y foráneas, facilitando la construcción de modelos analíticos, reportes ejecutivos y visualizaciones orientadas a la toma de decisiones.

### 4. Escalas de medición
- **Nominal:** Categorías sin orden ni jerarquía (ej: nombre_cliente, ciudad, medio_pago).  
- **Ordinal:** Categorías con orden, pero sin distancia numérica definida (ej: talla de producto S < M < L).  
- **Intervalo:** Variables con diferencia significativa, pero sin cero absoluto (ej: fecha_alta).  
- **Razón:** Variables con cero absoluto y operaciones matemáticas completas (ej: cantidad, precio_unitario, importe).


## Información del Conjunto de Datos

Seleccione una sección del menú para visualizar la información correspondiente al dataset de la tienda.

---

<details>
<summary><strong>Descripción general</strong></summary>

El conjunto de datos representa un sistema transaccional de una tienda minorista. Incluye información estructurada sobre productos, clientes y operaciones de venta, diseñada con fines educativos y de análisis de datos.

Permite realizar análisis de ventas, comportamiento del cliente, desempeño de productos y gestión de inventarios.
</details>

---

<details>
<summary><strong>Archivos incluidos</strong></summary>

- `productos.csv` — Catálogo de productos  
- `clientes.csv` — Registro de clientes  
- `ventas.csv` — Transacciones de venta  
- `detalle_ventas.csv` — Detalle de productos por venta  

Cada archivo se encuentra relacionado mediante identificadores únicos que permiten su integración.
</details>

---

<details>
<summary><strong>Productos</strong></summary>

Archivo: `productos.csv`
Registros aproximados: 100

Variables principales:
- Identificador del producto
- Nombre del producto
- Categoría
- Precio unitario

Este archivo permite analizar precios, categorías y desempeño por producto.
</details>

---

<details>
<summary><strong>Clientes</strong></summary>

Archivo: `clientes.csv`  
Registros aproximados: 100  

Variables principales:
- Identificador del cliente
- Nombre
- Correo electrónico
- Ciudad
- Fecha de alta

Permite análisis de clientes, segmentación y estudios de antigüedad.
</details>

---

<details>
<summary><strong> Ventas</strong></summary>

Archivo: `ventas.csv`
Registros aproximados: 120

Variables principales:
- Identificador de la venta
- Fecha de la transacción
- Identificador del cliente
- Medio de pago

Facilita el análisis temporal de ventas y métodos de pago.
</details>

---

<details>
<summary><strong>Detalle de ventas</strong></summary>

Archivo: `detalle_ventas.csv`  
Registros aproximados: 343  

Variables principales:
- Identificador de la venta
- Identificador del producto
- Cantidad vendida
- Precio unitario
- Importe por línea

Permite análisis a nivel granular de productos y cálculo de ingresos.
</details>

---

<details>
<summary><strong>Relación entre archivos</strong></summary>

- `clientes.id_cliente` → `ventas.id_cliente`
- `ventas.id_venta` → `detalle_ventas.id_venta`
- `productos.id_producto` → `detalle_ventas.id_producto`

Esta estructura relacional facilita la integración de datos
</details>

## Pasos del programa

### 1. Inicio del programa
Se iniciala la ejecución del sistema de análisis de datos.

---

### 2. Carga de datos
Se importan los archivos que conforman el conjunto de datos:
- `clientes.csv`
- `productos.csv`
- `ventas.csv`
- `detalle_ventas.csv`

---

### 3. Validación y limpieza de datos
Se realizan procesos de aseguramiento de la calidad de los datos:
- Verificación de valores nulos o faltantes.
- Validación de tipos de datos conforme a su definición.
- Comprobación de la integridad referencial mediante identificadores (IDs).

---

### 4. Integración de datos
Se lleva a cabo la consolidación de la información:
- Unión del archivo de ventas con el de clientes.
- Unión del detalle de ventas con el catálogo de productos.
- Integración de todas las entidades en una tabla analítica central.

---

### 5. Cálculo de métricas
Se calculan indicadores clave para el análisis del negocio:
- Ventas totales.
- Ventas por producto y por categoría.
- Ventas por cliente.
- Ticket promedio.
- Identificación de productos de alta y baja rotación.

---

### 6. Análisis
Se aplican técnicas analíticas para la obtención de conocimiento:
- Identificación de patrones de compra.
- Análisis temporal y de tendencias en las ventas.
- Segmentación básica de clientes según su comportamiento.

---

### 7. Visualización y resultados
Se presentan los resultados de manera estructurada:
- Generación de tablas resumen.
- Creación de gráficos y dashboards analíticos.

---

### 8. Generación de reporte
Se documentan los hallazgos del análisis:
- Exportación de resultados.
- Presentación de conclusiones y recomendaciones.

---

### 9. Fin del programa
Se finaliza la ejecución del sistema de análisis de datos.

- **Pseudocódigo:**

INICIO

CARGAR archivo_clientes
CARGAR archivo_productos
CARGAR archivo_ventas
CARGAR archivo_detalle_ventas

SI existen valores nulos O tipos incorrectos EN archivos
    LIMPIAR datos
FIN SI

UNIR ventas CON clientes USANDO id_cliente
UNIR detalle_ventas CON productos USANDO id_producto
UNIR ventas_clientes CON detalle_ventas_productos USANDO id_venta

CALCULAR ventas_totales
CALCULAR ventas_por_producto
CALCULAR ventas_por_categoria
CALCULAR ventas_por_cliente
CALCULAR ticket_promedio
IDENTIFICAR productos_alta_rotacion
IDENTIFICAR productos_baja_rotacion

ANALIZAR tendencias_temporales
SEGMENTAR clientes POR frecuencia_y_monto

MOSTRAR tablas_resumen
GENERAR visualizaciones

EXPORTAR reporte_final

FIN

- **Diagrama de flujo:**
presentado en entreglabes