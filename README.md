# COVID-19 Vaccination & Socioeconomic Factors Analysis: U.S. County-Level Study

## Project Overview
This project investigates how COVID-19 vaccination rates and socioeconomic factors correlate with COVID-19 case rates across 3,202 U.S. counties.  
The interactive web map visualizes spatial patterns to highlight disparities and support data-driven public health interventions.  

The project integrates multiple national datasets, performs rigorous data cleaning, and uses spatial visualization through web mapping technologies.

---

## Data Collection Pipeline

### 1. Primary Data Sources

#### COVID-19 Case Data
- *Source:* NY Times COVID-19 Data GitHub Repository  
- *File:* us-counties.csv  
- *Variables:* County FIPS codes, case counts, dates  
- *URL:* [https://github.com/nytimes/covid-19-data](https://github.com/nytimes/covid-19-data)

#### Vaccination Data
- *Source:* CDC COVID-19 Vaccination Data  
- *File:* COVID-19_Vaccinations_in_the_United_States_County.csv  
- *Variables:* Vaccination percentages, county FIPS codes  
- *Collection:* CDC official data portal

#### Socioeconomic Data
- *Source:* U.S. Census Bureau American Community Survey (ACS)  
- *Dataset:* ACS 5-Year Estimates 2023 (DP03)  
- *Variables:* Population, median income, poverty rates  
- *Access:* Census API or direct download

#### Geographic Data
- *Source:* U.S. Census TIGER/Line Shapefiles  
- *File:* tl_2023_us_county.shp  
- *Purpose:* County boundaries for mapping  
- *Variables:* FIPS codes, land area (for density calculations)

---

## Data Management and Cleaning Process

### 2.1 COVID-19 Case Data Preparation
- Extracted and aggregated case data by FIPS codes.  
- Filtered relevant time periods for analysis.  
- Managed missing or incomplete county-level data.

### 2.2 Vaccination Data Cleaning
- Merged vaccination data with county-level identifiers.  
- Standardized percentage fields.  
- Removed duplicates and non-county records.

### 2.3 Census Data Processing
- Selected key socioeconomic indicators (population, median income, poverty).  
- Cleaned formatting and variable naming.  
- Matched with FIPS codes for integration.

### 2.4 Geographic Data Preparation
- Clipped TIGER/Line shapefiles to U.S. county boundaries.  
- Reprojected shapefiles for web mapping compatibility.  
- Joined spatial data with attribute datasets.

### 2.5 Master Dataset Integration
- Used FIPS codes as unique identifiers.  
- Conducted inner joins to align all datasets.  
- Generated the final dataset for mapping and analysis.

---

## Statistical Analysis Methodology

### 3.1 Descriptive Statistics
- Summarized COVID-19 case rates and vaccination coverage.
- Calculated central tendencies and distribution patterns.

### 3.2 Correlation Analysis
- Explored linear relationships between vaccination rates and case rates.
- Assessed strength of associations with socioeconomic factors.

### 3.3 Multivariate Regression
- Built regression models to predict case rates based on:
  - Vaccination percentages
  - Poverty rates
  - Median income
  - Population size

### 3.4 Categorical Variable Creation for Mapping
- Binned continuous variables into categorical classes (e.g., low, medium, high vaccination coverage).
- Optimized for meaningful visualization.
---

## Data Preparation in QGIS

## Map Design

- Base Layer: U.S. Counties  
- Symbology: Choropleth map for COVID-19 cases  
- Additional Attributes: Vaccination rate, poverty rate, risk score in popups  
- Controls: Zoom, pan, optional fullscreen  
- Projection: EPSG:4326 (WGS84)  

---

## Exporting the Interactive Map

### 1. Use qgis2web

### 2. Folder Structure After Export


final_webmap/
├── index.html
├── data/
├── resources/
└── Openlayers/



### 3. Test Locally
- Open index.html in your browser.
- Check zoom, popups, and base map.

---

## Publishing with GitHub Pages

### Step 1 — Create a Repository
- Go to [https://github.com](https://github.com)
- Click *New Repository*
- Give a meaningful name (COVID19-USA-2023-Vaccination-Analysis)
- Check *Add README* and select *MIT License*

### Step 2 — Upload Files
- Upload everything from the exported final_webmap folder:
  - index.html
  - data folder
  - resources folder
  - supporting folders

### Step 3 — Enable GitHub Pages
- Go to *Settings → Pages*
- Source: main branch  
- Folder: / (root)  
- Click *Save*

You’ll get a live URL:


https://github.com/KIAChy21/US-COVID19-Cases-Vaccination2023/


### Step 4 — Add Collaborator
- Go to *Settings → Collaborators*
- Add instructor’s username:

jfobrycki

`
- Click *Add collaborator*

---

## Embedding the Map

You can embed the map in another webpage or LMS using an iframe:

html
<iframe src="https://your-username.github.io/us-covid-vaccination-map" 
      width="100%" 
      height="600" 
      frameborder="0">
</iframe>
`
---
## Repository Structure


us-covid-vaccination-map/
├── index.html
├── data/
├── resources/
├── README.md
└── LICENSE

---
## License

This project is licensed under the *MIT License*.
You are free to use, modify, and share with proper credit.

--

## Acknowledgments

* *Instructor:* John Obrycki [jfobrycki]
* *Author:* Kamal Ibne Amin Chowdhury [KIAChy21]
* *Software:* QGIS
* *Data:* NY Times, CDC, U.S. Census Bureau
* *Tools:* qgis2web, GitHub Pages

---

## Contact

For questions or collaboration, contact: mail to: kch365@uky.edu

---

This project demonstrates how open data and free GIS software can be used to visualize and communicate complex public health information effectively.

```
