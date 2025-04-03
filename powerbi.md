#  Guía de Power BI con PostgreSQL

##  ¿Qué es Power BI?

**Power BI** es una herramienta de análisis y visualización de datos desarrollada por Microsoft. Permite:

- Conectarse a diversas fuentes de datos.
- Transformar, limpiar y combinar datos.
- Crear dashboards interactivos y reportes.
- Compartir resultados con otros usuarios o en la web.

---

##  ¿Qué es PostgreSQL?

**PostgreSQL** es un sistema de gestión de bases de datos relacional (RDBMS) de código abierto, potente y extensible. Usa SQL estándar y es ampliamente usado para aplicaciones empresariales.

---

##  Requisitos para la conexión Power BI - PostgreSQL

1. Tener instalado **Power BI Desktop**:  
   [PowerBI](https://apps.microsoft.com/detail/9NTXR16HNW1T?hl=en-us&gl=CR&ocid=pdpshare)




##  Cómo conectar Power BI a PostgreSQL

1. Abre Power BI Desktop.
2. Haz clic en **Inicio > Obtener datos > PostgreSQL database**.
3. Ingresa los datos:
   - **Servidor:** `localhost`, IP o nombre del servidor.
   - **Base de datos:** `nombre_de_tu_bd`
4. Clic en **Aceptar**.
5. Ingresa tu **usuario** y **contraseña** de PostgreSQL.
6. Selecciona las **tablas o vistas** que desees cargar.

---

##  Modelado de datos en Power BI

Una vez cargados los datos:

- Puedes ver las **relaciones** entre tablas en la vista de modelo.
- Usar **Power Query** para transformar datos (filtrar, eliminar columnas, etc.).
- Crear **medidas DAX** o **columnas calculadas**.

---

##  Crear visualizaciones

Power BI permite usar diferentes tipos de gráficos:

- Columnas, líneas, pastel
- Mapas geográficos
- Tarjetas de KPI
- Tablas y matrices
- Segmentaciones (filtros)

Ejemplo: Total de ventas por categoría.

---

##  Ejemplo práctico con Northwind

Supón que tienes estas tablas:

- `orders`
- `order_details`
- `products`
- `categories`
- `customers`

### Objetivo:

1. Relaciona `orders` con `order_details`, y estas con `products`.
2. Relaciona `products` con `categories`.
3. Relaciona `orders` con `customers`.

### Medida DAX para total vendido:
```DAX
Total Ventas = SUMX(order_details, order_details[quantity] * order_details[unit_price])
