# Visualizing the Food Landscape: Linking Nutrition and Socioeconomic Indices

This project explores the relationship between global nutrition and socioeconomic indicators through interactive data visualization.  
We use data from **Food and Agriculture Organization of the United Nations (FAOStat)**, economic statistics (such as GDP per capita), as well as macro and micro nutrient details to create a choropleth map showing nutrition equity across countries.

## DESCRIPTION

The project visualizes:
- National nutrition data aggregated from FAOStat
- Economic indicators (e.g., GDP per capita)
- A proposed **Nutrition Score** that standardizes nutrition by economic status
- Carbs, Proteins, and Carbohydrates with respect to GDP across countries

The goal is to reveal how different regions’ nutrition levels relate to their economic standing and identify countries that perform better or worse than expected. We also aim to discover hidden or new relationships as well as connections/trends across various countries.

## File Tree

- `global_food_nutrition.html` - base site contains d3 visualization and representations
- `data/` folder 
   - `world_countries.json` (country boundaries) (GIVEN)
   - `API_NY.GDP.PCAP.PP.CD_DS2_en_csv_v2_254072.csv` is a file containing GDP data (GIVEN)
   - `SUA_Crops_Livestock_E_All_Data_NOFLAG.csv` is a file that contains the bulk food supply intake that needs be downloaded (NEED TO DOWNLOAD)
   - After running through the ipynb files, more files will be generated
      - `area_cluster_colors.csv` represents a mapping of ISO3 country codes to cluster colors (GENERATED)
      - `country_nutrient_totals.csv` represents an analysis of micronutrient spread for each country (GENERATED)
      - `country_nutrition_scores.csv` represents the nutrition scores of each country along with ISO3 codes for mapping (GENERATED)
      - `SUA_Crops_Livestock_E_All_Data_Categorized.csv` represents a succient categeorized version of the original bulk dataset (GENERATED)
   - `nutrient rankings` folder
      - Contains three files corresponding to rankings of each countries carbohydrates, fats, and protein intake (GIVEN)
- `lib/` folder contains D3.js dependencies 
- `dataset_analysis`
   - `category_map.json` represents a consolidation and mapping of categories from the bulk FAOStat dataset
   - `Country-Clustering.ipynb` represents a notebook file that applies clustering and creates the appropriate csv files
   - `FAOSTAT_full.ipynb` represents a notebook file that constructs the base nutrition score analysis along with various other nutrition statistics
- `food-nutrition-data`
   - Contains various model categories and a macro nutrient and micro nutrient breakdown for later analysis
- `environment.yml` - conda environment setup file, to run notebook code



## INSTALLATION

1. Clone the repository:
   ```bash
   git clone https://github.com/ashaik20/food-socio-viz.git
   cd food-socio-viz
   ```
2. Download the original food supply intake dataset from this [FAOStat link](https://bulks-faostat.fao.org/production/SUA_Crops_Livestock_E_All_Data.zip) and place the datatsets, specifically, `SUA_Crops_Livestock_E_All_Data_NOFLAG.csv`, within the `data` folder.
3. Setup a Conda environment from the project root and then activate it:
   ```
   conda env create -f environment.yml
   conda activate food_socio_viz
   ```
4. Click Run-all for first `FAOSTAT_full.ipynb` and second `Country-Clustering.ipynb` to generate the required dataset files using this conda environment. This will generate the required dataset files for the map visualization.

## EXECUTION
1. Start a python server:
   ```bash
   python -m http.server 8000
   ```
2. Navigate to [http://[::1]:8000/](http://[::1]:8000/) and click `global_food_nutrition.html` from which the map will be visible

## Data Sources

- [FaoStat Database](https://www.fao.org/faostat/en/#data/SCL)
- [World Bank Database](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD)

## Team
Team 21 — Suhas, Arush, Mithun, Adil, Nandha, Sanjay
Georgia Tech | CS Visualization Project (Fall 2025)
