# 🚴‍♂️ Proyecto Power BI – Adventure Works Cycle  

💼 **Autor:** Jesús E. Morgan  
📊 **Data Analyst | SQL · Python · Power BI**  
📅 **Entrega:** 16/07/2025  
📂 **Cohorte:** DA-FT16  

---

## 📖 Introducción  
Adventure Works Cycles (AWC) es una empresa multinacional de fabricación y distribución de bicicletas, piezas y accesorios en América del Norte, Europa y Asia.  

El objetivo del proyecto fue analizar de manera sistematizada las **ventas**, identificar puntos de mejora y diseñar un tablero en **Power BI** que permita a los usuarios obtener insights clave.  

### Objetivos principales:  
- 🧹 Mejorar la **calidad de los datos** mediante limpieza y depuración.  
- 🔗 Construir un **modelo de datos relacional** alineado al negocio.  
- 🧮 Implementar **medidas DAX** para métricas críticas.  
- 🎨 Diseñar **dashboards visuales e intuitivos** para la toma de decisiones.  

---

## 🛠️ Tecnologías y Herramientas  

**Business Intelligence**  
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)   ![Power Query](https://img.shields.io/badge/Power_Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)  

**Bases de Datos**  
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)   ![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)  

**Lenguaje DAX**  
![DAX](https://img.shields.io/badge/DAX-4479A1?style=for-the-badge&logo=data&logoColor=white)  

---

## 🔧 Desarrollo del Proyecto  

### 1️⃣ Conexión y Limpieza de Datos  
- Restauración de **AdventureWorksDW2019** en SQL Server.  
- Conexión desde Power BI a tablas como `DimProduct`, `DimDate`, `DimPromotion`, `FactInternetSales`, entre otras.  
- Limpieza con **Power Query**:  
  - Ajuste de tipos de datos.  
  - Eliminación de columnas innecesarias y con >90% de nulos.  
- Integración de tabla **DimCustomer** desde Excel.  
- Combinación de tablas:  
  - `Customer + Geography` → para ciudad, provincia y código.  
  - `Product + Category + Subcategory` → para clasificación en producto.  

### 2️⃣ Modelo Relacional y Mockup  
- Creación de un **modelo estrella**.  
- Diseño de un **mockup inicial** para guiar el dashboard.  

### 3️⃣ Medidas DAX principales  
- **Ingresos, Costos, Utilidad Bruta, Utilidad Neta.**  
- **KPIs de variación año contra año (YoY).**  
- **Ratios:** COGS, Margen Bruto, Margen Neto.  
- **Cálculos de acumulados y comparativos.**  

Ejemplo de medidas:  
```DAX
TotalIngresos = SUM(FactInternetSales[SalesAmount])

UtilidadNeta = 
VAR AnioMax = YEAR(MAX(FactInternetSales[OrderDate]))
RETURN
CALCULATE(
    SUM(FactInternetSales[SalesAmount]) 
  - SUM(FactInternetSales[TotalProductCost]) 
  - SUM(FactInternetSales[TaxAmt]) 
  - SUM(FactInternetSales[Freight]),
  DimDate[CalendarYear] = AnioMax
)
```
---

### 4️⃣ Creación del Tablero  
- Incorporación de **parámetros**: Ingresos, Utilidad Neta, Utilidad Bruta, COGS, % Margen.  
- Implementación de un **Grupo de Cálculo** llamado *Inteligencia de Tiempo*.  
- Botones de **navegación entre páginas**.  
- Tooltip

---

## 📊 Resultados Principales  
Tablero dinámico con:  
- Ingresos, Costos, Utilidad Bruta y Neta.  
- Segmentadores por Año, País y Categoría.  
- Comparaciones interanuales (**YoY**).  
- Documentación organizada de medidas y carpetas.  

👉 El dashboard final facilita la **exploración de la rentabilidad** y el **análisis de tendencias en ventas**.  

---

---

## 📸 Vista del Dashboard  

### 🔹 Dashboard Principal  
![Dashboard Principal](Projects/Adventure Works Cycle/assets/dashboard_principal.png)   

---

📂 También puedes explorar el proyecto completo descargando el archivo:  
[Descargar AdventureWorks.pbix](Projects/Adventure Works Cycle/assets/Adventure Works Cycle.pbix)  


## 🔮 Líneas Futuras  
- Ampliar las medidas DAX para nuevos KPIs.  
- Profundizar en análisis por **territorio y promociones**.  
- Explorar integración con **datos en tiempo real**.  

---

## 💡 Reflexión Personal  
Este proyecto me permitió afianzar:  
- El orden y precisión en la limpieza de datos.  
- La construcción de un modelo relacional robusto.  
- El diseño de dashboards profesionales en Power BI.  

---


