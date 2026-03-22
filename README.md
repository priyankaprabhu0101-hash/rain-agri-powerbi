# rain-agri-powerbi
## Name: Priyanka (priyankaprabhu0101@gmail.com)
This repository contains a complete analytics project that explores how rainfall affects crop productivity across Indian states and districts (1966–2017). The core deliverable is an interactive Power BI dashboard that visualizes rainfall trends, crop yield metrics, and correlations to support data‑driven agricultural decisions.
File: rain-agriculture.csv
Contents: state and district identifiers, year, monthly rainfall (June–September), crop area and yield metrics, and other agricultural indicators. Use this dataset as the single source of truth for all visuals and calculations.
Transforming Data:  Data Profiling, Cleaning data types, removing duplicates & adding totals
Created a Year Table ranging from 1966 - 2017
Created relationships between Rain Year & Agricultural Year
## Core DAX measures – Rainfall
-- Total monsoon rainfall (sum across all records) Total Rainfall (mm) = SUMX( 'rain-agriculture', 'rain-agriculture'[JUN] + 'rain-agriculture'[JUL] + 'rain-agriculture'[AUG] + 'rain-agriculture'[SEP] ) 
-- Average monsoon rainfall per record Avg Rainfall (mm) = AVERAGEX( 'rain-agriculture', 'rain-agriculture'[JUN] + 'rain-agriculture'[JUL] + 'rain-agriculture'[AUG] + 'rain-agriculture'[SEP] )
 -- Year-over-year rainfall change % Rainfall YoY % = VAR CurrYear = CALCULATE([Avg Rainfall (mm)]) VAR PrevYear = CALCULATE([Avg Rainfall (mm)], PREVIOUSYEAR(DimYear[Year])) RETURN DIVIDE(CurrYear - PrevYear, PrevYear, BLANK())
## Core DAX measures – Crop Yield
-- Average Rice Yield Avg Rice Yield = AVERAGE('rain-agriculture'[RICE YIELD (Kg per ha)])
 -- Max Rice Yield Max Rice Yield = MAX('rain-agriculture'[RICE YIELD (Kg per ha)]) -- Min Rice Yield (excluding zeros) Min Rice Yield = MINX( FILTER('rain-agriculture', 'rain-agriculture'[RICE YIELD (Kg per ha)] > 0), 'rain-agriculture'[RICE YIELD (Kg per ha)] ) 
 -- Repeating the same pattern for other crops
 Created Dashboards with this expressions
