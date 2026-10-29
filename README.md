# RetailPro-ejercicio-IA
Un ejercicio de crear un README para RetailPro con IA
RetailPro: Análisis Comercial y Dashboard Ejecutivo

1. Descripción General del Proyecto

RetailPro es una solución integral de inteligencia de negocios (Business Intelligence) desarrollada para optimizar la toma de decisiones estratégicas en una tienda minorista especializada en tecnología. El proyecto abarca desde el diseño conceptual de la arquitectura de datos hasta la construcción de consultas SQL avanzadas y la puesta en producción de un dashboard interactivo en Power BI.

El objetivo principal es transformar datos transaccionales dispersos en un modelo de información estructurado que permita evaluar el rendimiento comercial, analizar el comportamiento de los clientes, monitorear la rotación e ingresos por categoría de productos y detectar patrones de consumo clave.

2. Tecnologías y Herramientas Utilizadas

Motor de Base de Datos: SQL Server / T-SQL (Scripts DDL/DML, consultas multitabla con INNER JOIN y LEFT JOIN, agregaciones, expresiones comunes de tabla CTEs y lógica condicional).

Esquema Relacional:

dbo.ventas (Tabla de Hechos: Id_venta, Fecha_venta, Id_cliente, Id_producto, Cantidad, Precio_unitario)

dbo.clientes (Dimensión: Id_cliente, Nombre, Email, Ciudad, Fecha_registro)

dbo.productos (Dimensión: Id_producto, Nombre_producto, Id_categoria, Precio)

dbo.categorias (Dimensión: Id_categoria, Nombre_categoria)

Visualización y Business Intelligence: Power BI Desktop (Modelado de datos en estrella, lenguaje DAX para métricas calculadas y diseño UX/UI interactivo).

Documentación y Diseño Conceptual: Microsoft Word y Wireframes/Mockups para la definición de KPIs y la maquetación inicial.

Control de Versiones: Git & GitHub.

3. Estructura del Repositorio y Flujo de Trabajo

El proyecto sigue una metodología estructurada en tres fases clave para garantizar la trazabilidad, calidad y escalabilidad del análisis:

RetailPro/
│
├── 📁 docs/                        # Documentación conceptual y arquitectura
│   ├── RetailPro_Especificaciones.docx
│   └── Dashboard_Wireframe_Mockup.pdf
│
├── 📁 sql/                         # Scripts de base de datos
│   ├── 01_schema_definition.sql    # Creación de tablas y relaciones (DDL)
│   ├── 02_data_insertion.sql       # Carga de datos transaccionales (DML)
│   └── 03_business_queries.sql     # Consultas analíticas y vistas base
│
├── 📁 reports/                     # Reporte interactivo de Power BI
│   └── RetailPro_Executive_Dashboard.pbix
│
└── README.md                       # Documentación técnica del repositorio



Flujo de Trabajo

Fase 1: Documentación Previa y Mockups Iniciales

Definición de KPIs comerciales (Total Facturado, Ticket Promedio, Tasa de Recurrencia, Top Productos).

Elaboración de mockups y arquitectura funcional en Word/PDF para establecer la distribución visual del tablero antes del desarrollo.

Fase 2: Modelado, Limpieza y Consultas SQL

Diseño del esquema relacional identificando tablas de hechos (dbo.ventas) y tablas dimensionales (dbo.clientes, dbo.productos, dbo.categorias).

Creación de scripts SQL para limpieza de datos, normalización, tratamiento de valores nulos y cálculo de consolidaciones por canal y tiempo.

Fase 3: Carga de Datos y Dashboard Ejecutivo en Power BI

Conexión a la base de datos o ingesta de datasets transformados.

Establecimiento del modelo relacional en estrella (Star Schema).

Creación de medidas DAX avanzadas (métricas acumuladas, porcentajes de participación y análisis año a año).

Implementación de filtros dinámicos, tarjetas de KPI y gráficos navegables.

4. Vista Previa del Dashboard

A continuación se muestran capturas de pantalla del reporte interactivo diseñado en Power BI:

Resumen Ejecutivo y Métricas Principales

Análisis de Productos y Segmentación de Clientes

5. Instrucciones para Replicar o Ejecutar el Proyecto

Sigue estos pasos en orden cronológico para reproducir la base de datos y visualizar el dashboard en tu entorno local:

Paso 1: Clonar el Repositorio

git clone https://github.com/eduardofrancop86-gif/RetailPro.git
cd RetailPro


Paso 2: Configurar la Base de Datos SQL

Abre tu gestor de base de datos (ej. SQL Server Management Studio o DBeaver).

Ejecuta los scripts ubicados en la carpeta sql/ en el siguiente orden:

01_schema_definition.sql: Crea la estructura de tablas y llaves primarias/foráneas.

02_data_insertion.sql: Poblará las tablas con los registros de prueba de ventas, clientes y productos.

03_business_queries.sql: Ejecuta las consultas analíticas principales para verificar la integridad de los resultados.

Paso 3: Abrir y Explorar el Dashboard

Asegúrate de tener instalado Power BI Desktop.

Dirígete a la carpeta reports/ y abre el archivo RetailPro_Executive_Dashboard.pbix.

(Opcional) Si configuraste una conexión directa SQL, actualiza el origen de datos en Transformar Datos > Configuración de origen de datos indicando las credenciales de tu servidor local.

6. Conclusiones e Insights Clave

El tablero ejecutivo de RetailPro proporciona un valor estratégico directo al equipo directivo y comercial mediante:

Visibilidad Financiera: Seguimiento en tiempo real de la facturación global, volumen de transacciones y evolución del ticket promedio por periodo.

Optimización de Portafolio: Identificación de productos "estrella" (alto margen e ingresos) frente a productos de alta rotación pero menor rentabilidad, permitiendo reajustar la estrategia de pricing y empaquetado (bundling).

Segmentación de Clientes: Detección de patrones de compra recurrentes para focalizar campañas de retención y reactivación en los segmentos de mayor valor (LTV).

Análisis Omnicanal: Evaluación del rendimiento comparativo entre ventas en canal Online vs. Presencial para la asignación eficiente de presupuestos de marketing.

👨‍💻 Autor y Contacto

Desarrollador / Analista: Eduardo Franco

GitHub: eduardofrancop86-gif

Proyecto: RetailPro - Data Analytics
