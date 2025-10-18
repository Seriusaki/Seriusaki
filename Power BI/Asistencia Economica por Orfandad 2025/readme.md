# 🏛️ **INFORME DE ASISTENCIA ECONÓMICA POR ORFANDAD – PERÚ 2025**

---

## 🎯 Objetivo del Proyecto

Este informe en Power BI tiene como propósito analizar la distribución de subvenciones económicas otorgadas a personas en situación de orfandad en Perú durante el año 2025. El proyecto busca identificar patrones de ayuda, detectar brechas territoriales y demográficas, y facilitar la toma de decisiones basadas en evidencia para mejorar la cobertura de programas sociales.

---

## 🛠️ Tecnologías Utilizadas

- **Power BI Desktop**: Para la visualización interactiva de datos  
- **Power Query**: Para la transformación y limpieza avanzada del dataset  
- **DAX (Data Analysis Expressions)**: Para el cálculo de métricas clave  

---

## 📁 Metadatos del Dataset

El conjunto de datos utilizado proviene de fuentes públicas oficiales del Estado peruano, como [datos.gob.pe](https://www.datos.gob.pe), y contiene información anonimizada sobre beneficiarios de asistencia económica.

### Campos principales:
- `ID_Beneficiario`: Identificador único  
- `Departamento`, `Provincia`, `Distrito`: Ubicación geográfica  
- `Edad`, `Género`: Variables demográficas  
- `Tipo_Subvención`: Clasificación del apoyo económico  
- `Subvención Económica`: Valor monetario asignado  
- `Fecha de Nacimiento`, `Fecha de Entrega`: Datos temporales relevantes  

---

## 🔄 Procesamiento y Transformación

La transformación de datos se realizó íntegramente en **Power Query**, aplicando procesos de limpieza, normalización y enriquecimiento de la información.

### Transformaciones clave:
- Eliminación de duplicados y estandarización de nombres geográficos  
- Generación de una columna adicional de **cliente único**, combinando:  
  - `ID_Beneficiario`  
  - `Departamento`  
  - `Provincia`  
  - `Distrito`  
  - `Fecha de Nacimiento`  

Esta columna permite una segmentación precisa y evita duplicaciones en el análisis.

---

## 📊 Funciones DAX Utilizadas

Se implementaron expresiones DAX para calcular indicadores clave dentro del informe. Las funciones utilizadas incluyen:

- `AVERAGE()`  
- `SUM()`  
- `COUNTROWS()`  
- `DISTINCTCOUNT()`  
- `CALCULATE()`  
- `ALL()`  
- `FILTER()`  
- `VAR`  
- `RETURN`  
- `MAXX()`  
- `SUMMARIZE()`  
- `SELECTCOLUMNS()`  

Estas funciones permiten construir métricas como cantidad de personas ayudadas, monto total entregado, promedio de edad, segmentación por discapacidad, y ranking de departamentos más beneficiados.

---

## ✨ Autor

**Angel Gianfranco Valdivia Huayhualla**  
Data & Cloud Specialist | Microsoft Certified Trainer | Data Analyst | Educational Technologist  
📍 Lima, Perú  
📧 agvaldivia86@gmail.com  
🔗 [[LinkedIn](https://www.linkedin.com/in/agvaldivia86)]

---

> Este proyecto forma parte de una iniciativa educativa y analítica para promover la transparencia, la equidad y el uso ético de los datos en políticas sociales. Se agradece la retroalimentación y colaboración.
