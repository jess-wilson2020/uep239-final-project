# UEP 239 Final Project
## Spring 2021
## Jess Wilson
---
### **Summary of Project:**

- For my final project, I conducted a suitability analysis to determine which ZCTAs in Metro Boston were the most suitable for young professionals moving to Boston. The following ZCTA - level factors were considered in my analysis: population density, farmer's markets per capita, transit stop density, grocery stores per capita, and median rent. The analysis determined that the top 5 most suitable ZCTAs were : 02121 (Boston), 02113 (Boston), 02119 (Boston), 01718 (Acton), and 02116 (Boston). The top 3 towns with the most suitable ZCTAs were Boston, Acton, and Danvers.

---

### **Instructions on How to Run Notebook:**

1. Download repository or clone repository into working directory. 
2. In windows terminal, powershell, or anaconda prompt, navigate to working directory, and change directory to final project respository: 
    - cd: .\uep239-final-project\
3. Create new environment using final project respository's env:
    - conda env create -f environment.yml or mamba env create -f environment.yml
4. Once finalproject_env loads, activate environment:
    - conda activate finalproject_env 
5. Open jupyter lab:
    - jupyter lab uep239-final-project.ipynb
6. Set working directory in jupyter notebook when prompted to location in which final project data directory is stored (folder from repository titled 'uep239-final-project-data')

---

### **Data Directory Overview: uep239-final-project-data**

- tabular:
    - Population:
        - population.csv: Population Counts per MA ZCTA, Source: 2019 ACS 5-Year Estimates, US Census Bureau
        - metadata.csv
    - Rent:
        - rent.csv: Median Monthly Rent (USD) per MA ZCTA, Source: 2019 ACS 5-Year Estimates, US Census Bureau
        - metadata.csv
    - Supermarkets:
        - supermarkets.csv: Major Grocery Stores in MA (>100 employees), Source: 2021 Reference US
        - metadata.csv

- vector:
    - Farmers_Markets:
        - farmers_markets.shp: Massachusetts Farmers Markets, Source: MassGIS
    - MPO_Boundaries:
        - mpo_boundaries.shp: Boundaries of MA Metropolitan Planning Organizations, Source: MassDOT
    - Town_Boundaries:
        - town_boundaries.shp: Boundaries of MA Towns, Source: MassGIS
    - Transit_Stops:
        - transit_stops.shp: MBTA Rapid Transit Lines, Source: MassGIS
    -ZCTA_Boundaries: 
        - zcta_boundaries.shp: 2010 MA 5-Digit Zip Code Tabulation Areas (ZCTAs), Source: US Census Bureau

- Preprocessing Steps:
    - All data cleaning outlined in jupyter notebook
    - To acquire population.csv: US Census > Geography > All ZCTA in MA > 2019 ACS 5-Year Estimates Subject Tables > Topics: Populations and People > Download all.
    - To acquire supermarkets.csv: Reference USA > US Businesses Database > Advanced Search > Select Verified > Select Metro Area Boston, MA > Keyword SIC NAICS > 541105 - Grocers Retail > Filter by Number of Employees > 100 and Over > Download all.

---

### **Packages Overview:**

- channels:
    - conda-forge
- dependencies:
    - python=3.*
        - used to run entire program
    - ipython=7.10.*
        - used by python
    - jupyterlab=3.*
        - jupyter notebook
    - numpy
        - scientific computing
    - pandas
        - data frame manipulation
    - shapely
        - used by geopandas
    - geopandas
        - pandas manipulation with geospatial components
    - matplotlib
        - plotting and mapping data
    - contextily 
        - basemaps

---

### **Acknowledgements and References:**

- Thank you to Uku-Kaspar Uustalu, the Professor of Geospatial Programming with Python, and to our guest lecturers.  
- Sources Referenced for Debugging and Documentation: 
    - stackoverflow.com  
    - matplotlib.org
    - geopandas.org
    - stats.stackexchange.com
    - contextily.org
- Weights attributed to suitability index using AHP method: 
    - https://bpmsg.com/ahp/ahp-calc.php

---