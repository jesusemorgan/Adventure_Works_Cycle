# 🚴‍♂️ Power BI Project – Adventure Works Cycle  

💼 **Author:** Jesús E. Morgan  
📊 **Data Analyst | SQL · Python · Power BI**  
📅 **Delivery Date:** 16/07/2025  
📂 **Client:** Henry Bootcamp  

---

## 📖 Introduction  
Adventure Works Cycles (AWC) is a multinational manufacturing company that produces and distributes bicycles, parts, and accessories across North America, Europe, and Asia.  

The goal of this project was to systematically analyze **sales data**, identify areas for improvement, and design a **Power BI dashboard** to provide actionable business insights.  

### Main Objectives:  
- 🧹 Improve **data quality** through cleaning and preprocessing.  
- 🔗 Build a **relational data model** aligned with business needs.  
- 🧮 Implement **DAX measures** for key metrics.  
- 🎨 Design **intuitive and visually appealing dashboards** for decision-making.  

---

## 🛠️ Technologies & Tools  

**Business Intelligence**  
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)   ![Power Query](https://img.shields.io/badge/Power_Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)  

**Databases**  
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)   ![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)  

**DAX Language**  
![DAX](https://img.shields.io/badge/DAX-4479A1?style=for-the-badge&logo=data&logoColor=white)  

---

## 🔧 Project Development  

### 1️⃣ Data Connection and Cleaning  
- Restored **AdventureWorksDW2019** in SQL Server.  
- Connected Power BI to tables such as `DimProduct`, `DimDate`, `DimPromotion`, `FactInternetSales`, among others.  
- Data cleaning with **Power Query**:  
  - Adjusted data types.  
  - Removed unnecessary columns and those with >90% null values.  
- Integrated **DimCustomer** table from Excel.  
- Combined tables:  
  - `Customer + Geography` → to include city, province, and postal code.  
  - `Product + Category + Subcategory` → to classify products.  

### 2️⃣ Relational Model and Mockup  
- Built a **star schema model**.  
- Designed an **initial mockup** to guide the dashboard.  

### 3️⃣ Key DAX Measures  
- **Revenue, Costs, Gross Profit, Net Profit.**  
- **Year-over-Year (YoY) KPIs.**  
- **Ratios:** COGS, Gross Margin, Net Margin.  
- **Cumulative and comparative calculations.**  

Example measures:  
```DAX
TotalRevenue = SUM(FactInternetSales[SalesAmount])

NetProfit = 
VAR MaxYear = YEAR(MAX(FactInternetSales[OrderDate]))
RETURN
CALCULATE(
    SUM(FactInternetSales[SalesAmount]) 
  - SUM(FactInternetSales[TotalProductCost]) 
  - SUM(FactInternetSales[TaxAmt]) 
  - SUM(FactInternetSales[Freight]),
  DimDate[CalendarYear] = MaxYear
)
```
---

### 4️⃣ Dashboard Creation  
- Added **parameters**: Revenue, Net Profit, Gross Profit, COGS, % Margin.  
- Implemented a **Calculation Group** called *Time Intelligence*.  
- **Navigation buttons** between pages.  
- Tooltip functionality.  

---

## 📊 Main Results  
Dynamic dashboard including:  
- Revenue, Costs, Gross Profit, and Net Profit.  
- Slicers by Year, Country, and Category.  
- Year-over-Year (**YoY**) comparisons.  
- Organized documentation of measures and folders.  

👉 The final dashboard facilitates **profitability exploration** and **sales trend analysis**.  

---

## 📸 Dashboard View  

### 🔹 Main Dashboard  
![Main Dashboard](assets/dashboard_principal.png)   

---

📂 You can also explore the complete project by downloading the file:  
[Download AdventureWorks.pbix](assets/Adventure_Works_Cycle.pbix)  

---

## 🔮 Future Enhancements  
- Expand DAX measures for new KPIs.  
- Deepen analysis by **territory and promotions**.  
- Explore integration with **real-time data**.  

---

## 💡 Personal Reflection  
This project allowed me to strengthen:  
- Accuracy and attention to detail in data cleaning.  
- Building a robust relational model.  
- Designing professional dashboards in Power BI.  

---

---

# 🚴‍♂️ Proyecto Power BI – Adventure Works Cycle  

💼 **Autor:** Jesús E. Morgan  
📊 **Data Analyst | SQL · Python · Power BI**  
📅 **Entrega:** 16/07/2025  
📂 **Cliente:** Henry Bootcamp  

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
![Dashboard Principal](assets/dashboard_principal.png)   

---

📂 También puedes explorar el proyecto completo descargando el archivo:  
[Descargar AdventureWorks.pbix](assets/Adventure_Works_Cycle.pbix)  


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



