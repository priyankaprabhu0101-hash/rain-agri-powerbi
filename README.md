# 🌾 Rainfall Impact on Agricultural Productivity — Power BI Dashboard

A comprehensive data analytics project analysing the relationship between
monsoon rainfall patterns and agricultural productivity across Indian states
from 1966 to 2017.

---

## 📊 Project Overview

This project explores how variability in monsoon rainfall affects crop yields
across 18+ Indian states over five decades. Built as an interactive Power BI
dashboard, it enables stakeholders to identify rainfall trends, crop
performance patterns, and regional productivity variations through dynamic
visualisations.

---

## 📁 Repository Structure
```
├── rain-agriculture.csv        # Raw dataset (936 rows, 83 columns)
├── Priyanka_Prabhu_CPDA_Batch_9.pbix  # Power BI Dashboard file
├── Problem_statement_Agri.pdf  # Project brief and requirements
└── README.md                   # Project documentation
```

---

## 📂 Dataset Description

**Source:** rain-agriculture.csv  
**Period:** 1966 – 2017  
**Coverage:** 18+ Indian States  
**Records:** 936 rows · 83 columns  

| Column | Description |
|--------|-------------|
| State Name | Indian state |
| Agri_Year | Year of observation |
| RICE YIELD (Kg per ha) | Rice productivity metric |
| WHEAT YIELD (Kg per ha) | Wheat productivity metric |
| JUN, JUL, AUG, SEP | Monthly monsoon rainfall (mm) |
| Total_Monsoon_mm | Total monsoon rainfall (calculated) |
| Decade | Decade grouping (calculated) |

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — Dashboard development
- **Power Query** — Data cleaning and transformation
- **DAX** — Calculated measures and columns
- **GitHub** — Version control and project documentation

---

## ✅ Project Tasks

### Task 1 — Data Cleaning & Preparation
- Imported CSV into Power BI
- Fixed State Name casing using `Text.Proper()`
- Handled null values in crop columns
- Added `Total_Monsoon_mm` calculated column
- Set correct data types for all columns

### Task 2 — Data Modeling & DAX
- Created `DimYear` dimension table (1966–2017)
- Built `_Measures` table with 20+ DAX measures
- Added `Decade` grouping column
- Key measures include:
  - `Average Rainfall`, `Total Rainfall`
  - `Avg Rice Yield`, `Max Rice Yield`, `Min Rice Yield`
  - `Rainfall YoY %`

### Task 3 — Data Analysis
- Analysed temporal rainfall trends across states
- Evaluated rainfall–yield correlation
- Identified seasonal and geographic productivity patterns
- Discovered Green Revolution effect in 1970s–80s data

### Task 4 — Dashboard Development
- Built 3 interactive report pages
- Page 1: Executive Overview (KPI cards, map, trend line)
- Page 2: Rainfall Deep Dive (monthly breakdown, decomposition)
- Page 3: Crop Analysis (scatter plot, matrix, decade comparison)
- Interactive slicers for State, Year, Decade
- Cross-filtering and drill-through enabled

### Task 5 — Insights & Recommendations
- Documented 5+ data-backed insights
- Proposed actionable recommendations for agricultural stakeholders

---

## 💡 Key Insights

- **Kerala** recorded the highest average rainfall at 1,916.86 mm —
  483% higher than Tamil Nadu at 328.72 mm
- **1988** was the highest rainfall year nationally at 1,126.24 mm
- **Rice yield nearly doubled** from ~887 Kg/ha in the 1960s to
  ~1,726 Kg/ha in the 1990s — driven by the Green Revolution
- **July dominates** monsoon contribution across most Indian states
- Yield growth has **plateaued post-2000**, signalling the need for
  next-generation agricultural interventions
- **Punjab and Haryana** achieve top yields despite moderate rainfall
  through canal irrigation — decoupling productivity from monsoon dependency

---

## 📋 Recommendations

1. Use July rainfall as an **early warning indicator** for harvest forecasting
2. Invest in **micro-irrigation** in high-rainfall but low-yield northeastern states
3. Promote **drought-tolerant crops** in states below 400 mm average rainfall
4. Use historical data to build **smarter crop insurance** pricing models
5. Focus on **precision farming and climate-resilient varieties** to break
   the post-2000 yield plateau

---

## 📸 Dashboard Preview

| Page 1 — Summary | Page 2 — Map | Page 3 — Grean Revolution |Page 4 Key Insights
|-------------------|-------------------|----------------|----------------|
<img width="569" height="323" alt="image" src="https://github.com/user-attachments/assets/845a57d7-ca5f-438f-9e8f-c06cbc284a1e" />
<img width="572" height="325" alt="image" src="https://github.com/user-attachments/assets/f4cb000a-1021-4646-b202-6ae63b878128" />
<img width="556" height="314" alt="image" src="https://github.com/user-attachments/assets/43d91ae5-507c-4518-9792-e42736aaec06" />
<img width="574" height="323" alt="image" src="https://github.com/user-attachments/assets/65a450f1-d60e-46ca-ae4b-2d5bf9e269c1" />

---

## 🚀 How to Use

1. Clone this repository
```bash
git clone https://github.com/yourusername/rainfall-agriculture-powerbi.git
```
2. Open `Priyanka_Prabhu_CPDA_Batch_9.pbix` in **Power BI Desktop**
3. Ensure `rain-agriculture.csv` is in the same folder if prompted to
   refresh data source
4. Interact with slicers and visuals to explore the data

---

## 👩‍💻 Author

**Priyanka Prabhu**  
CPDA Batch 9  
[GitHub](https://github.com/priyankaprabhu0101-hash) · [LinkedIn](www.linkedin.com/in/priyanka-prabhu-256136a1)

---

## 📄 License

This project is submitted as part of the CPDA programme at HeroVired.  
Dataset and problem statement © 2025 HeroX Private Limited.
