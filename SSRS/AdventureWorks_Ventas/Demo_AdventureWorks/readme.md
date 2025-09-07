# 📊 AdventureWorks - BI Insights con SSRS

Este proyecto utiliza la base de datos AdventureWorks para generar reportes analíticos mediante **SQL Server Reporting Services (SSRS)**. Se diseñaron visualizaciones interactivas y tabulares que permiten analizar el rendimiento comercial por país, canal de venta, producto y tienda.

## 🎯 Objetivo

Construir un conjunto de reportes dinámicos en SSRS que faciliten la toma de decisiones estratégicas, simulando escenarios reales de inteligencia de negocios.

## ⚙️ Configuración Inicial

- Instalación de **Visual Studio** con **SQL Server Data Tools (SSDT)**.
- Habilitación del diseñador de reportes `.rdl`.
- Conexión a la base de datos AdventureWorks2019.
- Validación de permisos para ejecutar consultas y publicar reportes.

## 📈 Reportes Implementados

### 1. Reporte de Ventas
- Filtro por año y mes.
- Tabla con detalle por orden: país, tipo de compra, producto, total vendido.

### 2. TOP 10 - Productos y Tiendas
- Ranking de productos más vendidos por cantidad.
- Ranking de tiendas con mayores ventas por monto.
- Incluye canal "Online" como tienda virtual.

### 3. Dashboard Financiero
- Gráfico de ingresos anuales (2011–2014).
- Comparativa de ingresos por país.
- Distribución de ingresos online vs offline.
- Promedio de orden por país.

## 🔍 Funciones SQL Utilizadas

- `SUM()`, `ROUND()`, `COUNT()` para cálculos financieros
- `GROUP BY`, `ORDER BY`, `TOP` para segmentación y ranking
- `CASE`, `IIF()` para clasificación de origen de compra
- `JOIN` entre múltiples tablas: ventas, territorios, productos, ofertas, tarjetas
- `COALESCE()` para manejo de valores nulos
- **CTE (Common Table Expressions)** para estructurar subconsultas reutilizables y mejorar la legibilidad
- Uso de filtros dinámicos y condiciones temporales para simular escenarios de negocio

## 🛠️ Tecnologías Utilizadas

- Visual Studio + SSDT
- SQL Server Reporting Services (SSRS)
- SQL Server Management Studio (SSMS)
- AdventureWorks2019
- GitHub para documentación y control de versiones

## 🚀 Próximos Pasos

- Refinar visualizaciones con parámetros dinámicos
- Publicar reportes en servidor corporativo o portal web
- Integrar alertas automatizadas según métricas críticas
- Explorar migración a Microsoft Fabric para análisis en tiempo real

## 👤 Autor

**Angel Gianfranco Valdivia Huayhualla**  
Microsoft Certified Trainer | Data Analyst | Educational Technologist  
📍 Lima, Perú  
🎓 Especialista en SQL, SSRS, Power Query y automatización de procesos
