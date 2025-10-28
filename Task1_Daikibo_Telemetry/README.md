#  Task 1 – Daikibo Telemetry Data Analysis

## Objective
The objective of this task was to analyze machine telemetry data collected from Daikibo’s four factories located in Japan, China, and Germany.  
Each machine sent performance logs every 10 minutes, and the goal was to determine:
1. Which factory had the most machine downtime.
2. Which machine types broke down most frequently at that factory.

---

## Tools Used
- **Tableau** – for data visualization and dashboard creation  
- **JSON** – as the raw telemetry data format  
- **Calculated Fields** – for downtime computation

---

## Process Overview
1. Imported the provided `daikibo-telemetry-data.json` file into Tableau.
2. Created a calculated field called **`Unhealthy`** using the formula:
   ```text
   IF [Status] = "Unhealthy" THEN 10 ELSE 0 END
