# DataVisualization_task2

This project analyzes terrorism incidents from the provided dataset to uncover spatial, categorical, and temporal patterns. 
The study integrates geospatial visualization, attack type frequency analysis, and time-series decomposition to interpret trends 
in global terrorism events. The main objectives include identifying geographic hotspots, examining dominant attack types, 
understanding temporal trends, and providing data-driven insights useful for counter-terrorism policy and research.


**Data Preparation**

Data was loaded using pandas and cleaned to remove missing or invalid coordinates. 
534 rows with missing latitude or longitude values were dropped. Numeric columns (nkill, nwound, iyear, imonth, iday) 
were coerced to numeric, and zeros in imonth/iday replaced with 1 to ensure valid datetimes. A GeoDataFrame was created 
using GeoPandas with WGS84 (EPSG:4326) coordinates.

Descriptive statistics were generated for all numerical columns:
• Missing latitude values: 534
• Missing longitude values: 534
• Numeric summary saved as: 99_numeric_summary.csv


**Key Findings**

1. Geographic concentration: Majority of incidents occur in a few hotspot countries (Iraq, Pakistan, India, Afghanistan, Nigeria).
2. Attack type dominance: Bombings and armed assaults are the most frequent tactics.
3. Severity distribution: A small subset of incidents cause the majority of casualties.
4. Temporal trend: Long-term rise until 2015, followed by decline.
5. Mild seasonality: Slight periodic variations in monthly data.


**Limitations and Assumptions**

• Some incidents lacked coordinates and were excluded from maps.
• Reporting bias: Low-visibility events may be underrepresented.
• Date approximation: Month/day zeros replaced with 1 for valid datetime.
• Spatial scale: Country-level polygons obscure subnational variations.
• Analytical scope: Descriptive study only; no causal modeling.

**Conclusion**

This study successfully integrated geospatial, categorical, and temporal analyses to derive actionable insights from terrorism-incident data.
The results highlight regional concentration, dominant attack types, and historical trends, providing a data-driven foundation for further research and strategic policy planning.
Interactive visualizations (Folium maps) complement static analytical plots (Matplotlib, GeoPandas), and the decomposition exposes underlying seasonality beyond simple counts.
Overall: The dataset reveals that terrorism intensity is unevenly distributed, temporally dynamic, and tactically concentrated—insights valuable for both security analysis and academic discussion.


