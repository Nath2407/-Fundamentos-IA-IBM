# Instrucciones para Copilot  
## Proyecto: Análisis de Datos de una Tienda Minorista

---

## 1. Contexto del proyecto
Este proyecto tiene como objetivo analizar un conjunto de datos que representa una tienda minorista, incluyendo información de clientes, productos y operaciones de venta.  
Los datos se utilizan con fines educativos y analíticos, y se procesan mediante Python, utilizando Programación Orientada a Objetos (POO).

El sistema permite:
- Explorar la estructura del conjunto de datos.
- Integrar múltiples archivos CSV.
- Calcular métricas básicas de ventas.
- Mostrar resultados mediante un menú interactivo en consola.
- Ejecutarse en Google Colab.

---

## 2. Archivos de datos utilizados
El proyecto trabaja con los siguientes archivos en formato CSV:

- `clientes.csv`
- `productos.csv`
- `ventas.csv`
- `detalle_ventas.csv`

Cada archivo representa una entidad del sistema transaccional y se integra mediante identificadores únicos (IDs).

---

## 3. Lenguaje y herramientas
Copilot debe generar sugerencias considerando:

- Lenguaje: **Python 3**
- Librerías principales:
  - `pandas`
- Paradigma: **Programación Orientada a Objetos (POO)**
- Entorno de ejecución: **Google Colab**

---

## 4. Estructura esperada del código
El código debe:

- Definir una clase principal para el análisis de datos.
- Separar responsabilidades en métodos claros:
  - Carga y validación de datos.
  - Integración de datasets.
  - Análisis y cálculo de métricas.
  - Visualización de resultados en consola.
- Implementar un menú interactivo usando `input()`.

---

## 5. Funcionalidades del menú
Copilot debe considerar que el menú interactivo incluya las siguientes opciones:

1. Mostrar información del conjunto de datos:
   - Número de archivos utilizados.
   - Número de registros y columnas.
   - Tipos de datos de cada variable.
2. Mostrar un resumen general de ventas.
3. Mostrar ventas agrupadas por categoría.
4. Salir del programa.

No debe incluir análisis de ventas por cliente.

---

## 6. Buenas prácticas esperadas
Copilot debe sugerir código que:

- Sea legible y bien documentado.
- Utilice nombres de variables descriptivos.
- Incluya comentarios técnicos.
- Evite código redundante.
- Sea fácilmente extensible (por ejemplo, para agregar gráficos o exportar resultados).

---

## 7. Salida del programa
El sistema debe mostrar los resultados directamente en consola, incluyendo:

- Métricas calculadas.
- Tablas resumen.
- Mensajes claros para el usuario al navegar por el menú.

---

## 8. Alcance del proyecto
Este proyecto no incluye:
- Bases de datos externas.
- Modelos predictivos avanzados.
- Interfaces gráficas complejas.

Su propósito es demostrar el flujo completo de análisis de datos: carga, validación, integración, análisis y presentación de resultados.

---

## 9. Nota final
Copilot debe priorizar soluciones claras, didácticas y alineadas con un contexto académico o de formación en análisis de datos.
