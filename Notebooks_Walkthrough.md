# Project Walkthrough: Air Quality and Climate Dynamics in California

## Overview

Welcome to our project on air quality and climate dynamics in California. This walkthrough will guide you through each notebook in the repository, explaining the purpose, key steps, and results. By the end of this walkthrough, you will understand how we processed, merged, and analyzed data to explore the relationship between climate factors and air pollution.

## Data Preprocessing

### Purpose
In this section, we focus on preparing the raw air quality and meteorological data for analysis. Our source data consisted of daily CSV files, separated by year, covering all U.S. counties.

### 1. Parameter Selection

**Air Quality Parameters:** We selected the following air quality pollutants for analysis:
- **SO2** (Sulfur Dioxide)
- **O3** (Ozone)
- **PM10** (Particulate Matter ≤ 10 µm)
- **PM2.5** (Particulate Matter ≤ 2.5 µm)
- **CO** (Carbon Monoxide)
- **NO2** (Nitrogen Dioxide)

**Weather Parameters:** To study the relationship between pollutants and weather conditions, we focused on:
- **Pressure**
- **Temperature**
- **Wind Speed**
- **Relative Humidity**

### 2. Data Concatenation

The data was initially separated into multiple files by year. We needed to:
- **Concatenate** all the yearly data files to create a comprehensive dataset.
- **Focus on the last 20 years** of data to analyze long-term trends and patterns.

### 3. Parameter Filtering

To streamline the analysis:
- **Retained only the relevant parameters** for our study from the concatenated data.
- **Removed unnecessary columns** to focus solely on the pollutants and weather parameters selected.

### 4. Aggregation

Air quality data from multiple measurements per station required aggregation:
- **Aggregated measurements** for each station to obtain daily averages or totals, ensuring consistency in the data.

### 5. Data Cleaning

Both air quality and meteorological data required cleaning:
- **Removed outliers** in the weather data, which were identified through preliminary analysis.
- **Applied linear interpolation** to handle missing values and smooth out irregularities in the data.

By executing these preprocessing steps, we ensured that our dataset was clean, consistent, and ready for detailed analysis, setting a solid foundation for understanding the relationship between air quality and climate dynamics.

### [Go to Data Preprocessing folder](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/tree/main/Data_preprocessing)

---

## Merging Datasets

### Purpose

In this section, we merge the cleaned air quality and meteorological data to create two unified datasets. This allows us to analyze the interactions between climate and pollution levels. Below is an overview of the notebooks used in this process:

### 1. [Air Quality Data](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/1_Air_Quality_Data_merged.ipynb)

**Purpose:** 
- Imported and merged all air pollution data.
- Ensured no records were lost despite some stations not having values for all dates.
- Removed the AQI data included in each pollutant file to retain later on the process only the critical parameter’s AQI (the highest AQI derived from the pollutant, indicating the highest concentration).

### 2. [AQI File](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/2_AQI_FILE.ipynb)

**Purpose:**
- Imported air pollution data once again.
- Focused on retaining the AQI of the critical parameter and the critical parameter itself for further analysis.

### 3. [Air Data & AQI](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/3_air_data_%26_AQI.ipynb)

**Purpose:**
- Merged the AQI data created in the previous notebook with key columns from the air pollution data.
- This step reintroduces the necessary columns for a comprehensive analysis, integrating AQI information with relevant air quality variables eg. Location, Date etc.

  *Initially, we removed extraneous variables to simplify data processing due to the large number of entries. 

### 4. [Weather Data](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/4_Weather_Data_merged.ipynb)

**Purpose:**
- Merged all weather data.
- Ensured no records were lost despite some stations not having values for all dates.

These notebooks collectively ensure that we have a comprehensive and unified dataset, combining air quality and weather data to explore their interactions effectively.

### [Go to Data Merging folder](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/tree/main/Data_merging)

---

## Data Analysis

### Purpose
These notebooks are dedicated to analyzing the final datasets to find the focus areas in usa (counties to study first) and uncover relationships between climate variables like temperature and air pollution levels.

### 1. [Yearly Aggregations](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Analysis/1_Weather_yearly_aggregation.ipynb)

**Purpose:** 
- Imported and aggregated daily air pollution data to yearly data also imported and aggregated daily weather data . We then merged weather and air pollution data.
- Ensured no records were lost despite some stations not having values for all dates and parameters.
- By studing yearly data we found the most polluted diachronically counties to focus on our alanysis.

  *Power bi was used in this step to visualize those statements.

### 2. [California & Utah](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/2_AQI_FILE.ipynb)

**Purpose:**
- Imported air pollution data and choce Utah and California to keep as the top polluted counties throuout the years.
- Added aqi data in the dataset.
- Imported weather data and choce Utah and California to keep as the top polluted counties throuout the years.
- merged weather and aqi data.
  
  *we included this as a part of our analysis cause it was derived from our power bi analysis oservations.

### 3. [Seasonal & Urban/Rural Analysis](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/3_air_data_%26_AQI.ipynb)

**Purpose:**
- In this step we imported Utah and Californias data and decided to focus on california cause as it is explained in the presentation it was a state that has High levels of pollution 
- Extensive network of monitoring stations
- Diverse geographic regions
- Strict environmental regulations. so we conducted temporal analysis first, distribution of aqis per season, and the aqi heatmap per year and month,and then temporal analysis, which included, aqi throuh the years in urban and rural areas, aqi comparison in urban and rural areas, average aqi in urban and rural areasduring different temperature ranges in california, and all 7 aqi pollutants levels in urban and rural areas over time. 


### 4. [Heatwaves](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Data_merging/4_Weather_Data_merged.ipynb)

**Purpose:**
- Identifid via literature los angeles as a county with heatwaves and found the heatwaves there and then plotted 2020 months to identify the months with heatwaves and in those plots see how aqi reacts during heatwaves.
- Ensured no records were lost despite some stations not having values for all dates.



### [Go to Data Merging folder](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/tree/main/Data_merging)

