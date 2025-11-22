# Visualizing the Food Landscape: Linking Nutrition and Socioeconomic Indices

This project explores the relationship between global nutrition and socioeconomic indicators through interactive data visualization.  
We use data from **Open Food Facts** and economic statistics (such as GDP per capita) to create a choropleth map showing nutrition equity across countries.

## Overview

The project visualizes:
- National nutrition data aggregated from Open Food Facts
- Economic indicators (e.g., GDP per capita)
- A proposed **Nutrition Equity Index** that standardizes nutrition by economic status

The goal is to reveal how different regions’ nutrition levels relate to their economic standing and identify countries that perform better or worse than expected.

## Current Progress

- Base world choropleth map built with D3.js  
- `data/` folder contains `world_countries.json` (country boundaries) as well as Open Food Facts data
- `lib/` folder contains D3.js dependencies  

**Next steps:**
- Add color scale and legend for the map  
- Integrate tooltip data for each country  
- Compute and visualize the Nutrition Equity Index  

## Setup

1. Download the original food supply intake dataset from the [main FAOStat site](https://bulks-faostat.fao.org/production/SUA_Crops_Livestock_E_All_Data.zip) and place the datatset within the `data` folder.
2. Clone the repository:
   ```bash
   git clone https://github.com/ashaik20/food-socio-viz.git
   cd food-socio-viz
   ```
3. Setup a Conda environment from the project root and then activate it:
   ```
   conda env create -f environment.yml
   conda activate food_socio_viz
   ```
4. Click Run-all for both `FAOSTAT_full.ipynb` and `Country-Clustering.ipynb` to generate the required dataset files using this conda environment. This will generate the required dataset files for the map visualization.
5. Start a python server:
   ```bash
   python -m http.server 8000
   ```
6. Navigate to [http://[::1]:8000/](http://[::1]:8000/) and click `base_map.html` from which the map will be visible

## Data Sources

- [Open Food Facts](https://world.openfoodfacts.org/data)
- [World Bank](https://data.worldbank.org)

## Team
Team 21 — Suhas, Arush, Mithun, Adil, Nandha, Sanjay
Georgia Tech | CS Visualization Project (Fall 2025)
