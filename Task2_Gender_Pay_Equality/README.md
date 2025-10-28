# Task 2 – Gender Pay Equality Analysis

## Objective
Daikibo Industrials received multiple internal complaints regarding gender pay inequality.  
The goal of this task was to analyze salary data and classify the **level of pay equality** for different job roles across global factory locations.

---

## Tools Used
- **Microsoft Excel** – for data manipulation and formula creation  
- **Conditional Logic (IF, AND, OR)** – for automated classification  

---

## Process Overview
1. Opened the provided dataset `Equality Table.xlsx` containing three columns:
   - Factory  
   - Job Role  
   - Equality Score (ranging from -100 to +100; where 0 represents perfect equality)
2. Added a new column named **`Equality Class`** to categorize each role’s score using the formula:
   ```excel
   =IF(AND(C2>=-10,C2<=10),"Fair",
     IF(OR(AND(C2>-20,C2<-10),AND(C2>10,C2<20)),"Unfair",
     IF(OR(C2<=-20,C2>=20),"Highly Discriminative","")))
