---
layout: page
title: "Tableau & Power BI: NYC Flight Weather Dashboard"
subtitle: "Comparative visualization and analysis of wind speed patterns across three major New York airports using Tableau and Power BI."
permalink: /projects/tableau-powerbi-dashboard/
description: "Developed dual dashboards in Tableau and Power BI for analyzing the 2013 NYC flight weather dataset, focusing on wind speed and precipitation patterns at LGA, JFK, and EWR airports."
---

<section class="lead" style="text-align: justify;">
This project was completed as part of the postgraduate coursework for <strong>SIT731: Data Wrangling</strong> at Deakin University.  
The task involved creating interactive dashboards using <strong>Tableau Public</strong> and <strong>Power BI</strong> to visualize meteorological data from three New York airports (LGA, JFK, and EWR) during 2013.  
The objective was to compute and visualize the daily and monthly mean wind speeds, identify the windiest days, and compare analytical results across both visualization platforms.
</section>

---

### 📊 Project Objective

The dataset <code>nycflights13_weather.csv</code> provides hourly weather observations for New York airports.  
All data wrangling and conversions were performed directly within Tableau and Power BI—external preprocessing in pandas or Python was not permitted.  

**Goals:**
1. Convert all measurements into metric (SI) units.  
2. Compute daily mean wind speed for LGA Airport.  
3. Identify the 10 windiest days at LGA with corresponding precipitation levels.  
4. (Postgraduate extension) Visualize monthly mean wind speeds for LGA, JFK, and EWR on a single plot.  

---

### 🧩 Implementation Details

#### Tableau
Data preprocessing began by filtering out comment lines and renaming unreadable columns.  
Each weather variable was converted into SI units using calculated fields:

- **Temperature (°F → °C):** `(x - 32) * 5/9`  
- **Dew Point (°F → °C):** `(x - 32) * 5/9`  
- **Precipitation (in → mm):** `x * 25.4`  
- **Visibility (mi → m):** `x * 1609.34`  
- **Wind Speed / Gust (mph → m/s):** `x * 0.44704`

A new field `date_time` was created using:  
`DATEPARSE('yyyy-MM-dd', STR([year]) + '-' + STR([month]) + '-' + STR([day]))`

**Visualizations created in Tableau:**
- Daily mean wind speed (LGA)  
- Monthly mean wind speed (all airports)  
- Top 10 windiest days at LGA  
- Combined dashboard with interactive filters  

**Tableau Dashboard:**  
[View Tableau Dashboard](https://public.tableau.com/views/s224117575/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)

---

#### Power BI
Due to the lack of in-app filtering, comment rows were manually removed from the CSV before import.  
Conversions followed Excel-based formulas, implemented within Power BI’s data view.

**Example formula:**  
`temp_celsius = (weather[temp] - 32) * 5/9`  
`date_time = DATE(weather[year], weather[month], weather[day])`

**Visualizations created in Power BI:**
- Daily mean wind speed (LGA)  
- Monthly mean wind speed (LGA, JFK, EWR)  
- Top 10 windiest days at LGA (using Top N filter)  
- Additional card elements showing day count and mean wind speed  

**Power BI Dashboard:**  
[View Power BI Dashboard](https://app.powerbi.com/reportEmbed?reportId=ddb7d055-e62b-48b6-9d67-8033030991ef&autoAuth=true&ctid=d02378ec-1688-46d5-8540-1c28b5f470f6)

---

### 🧠 Reflection

The project was a technical and conceptual exercise in working within the constraints of two different business intelligence tools.  
Unlike scripted environments, Tableau and Power BI required all transformations to occur within their internal formula engines.  

Several challenges arose:
- Cleaning and structuring the unformatted dataset entirely within GUI tools.  
- Rebuilding time columns manually to maintain temporal accuracy.  
- Adapting formulas between two software systems with different syntaxes and aggregation behaviors.  

Despite the limitations, both dashboards successfully replicated the same analytical objectives.  
The process clarified the conceptual difference between procedural (Python-based) and declarative (BI-based) data manipulation, strengthening practical understanding of data pipelines and visualization logic.

---

### 🧾 Summary

| Component | Tool | Output |
|------------|------|---------|
| Metric Conversion | Tableau / Power BI | Implemented using calculated fields |
| Daily Wind Speed (LGA) | Tableau / Power BI | Line graph |
| Monthly Wind Speed (3 Airports) | Tableau / Power BI | Multi-line comparison |
| Top 10 Windiest Days | Tableau / Power BI | Table with precipitation data |
| Dashboard Integration | Tableau / Power BI | Published to web dashboards |

---
