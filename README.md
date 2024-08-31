# Air Quality and Climate Dynamics in California

## Table of Contents
- [Project Overview](#project-overview)
- [Project Objectives](#project-objectives)
- [Data Sources](#data-sources)
- [Installation and Requirements](#installation-and-requirements)
  - [Prerequisites](#prerequisites)
  - [Dependencies](#dependencies)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [Results and Findings](#results-and-findings)
- [Challenges and Limitations](#challenges-and-limitations)
- [Future Work](#future-work)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview
This project examines air quality and climate dynamics in California, focusing on the interplay between air quality trends and climate patterns. Our goal is to provide insights that can help insurance companies develop targeted strategies to address risks associated with poor air quality.

## Project Objectives
- **Data Collection:** Gathered 20 years of air quality and weather data from the EPA.
- **Preliminary Analysis:** Cleaned and processed the data to identify states with the highest pollution levels.
- **Identify Areas of Interest:** Focused on states with high pollution and significant climatic variability.
- **Analyze Correlations:** Explored relationships between AQI, key pollutants, and weather data.
- **Heatwaves Analysis:** Examined the correlation between heatwaves, temperature spikes, and AQI.
- **Seasonal and Urban-Rural Analysis:** Studied AQI trends across different seasons and between urban and rural areas.
- **Implications for Insurance:** Provided recommendations for risk assessment and policy adjustments.

## Data Sources
- **EPA:** U.S. Environmental Protection Agency data for air quality and weather parameters. Historical data collected over 20 years, including pollutants like PM2.5, PM10, NO2, CO, SO2, Ozone, and weather parameters such as temperature and pressure.

## Installation and Requirements

### Prerequisites
- **Python 3.9:** Ensure Python 3.9+ is installed on your system.
- **Conda:** Conda package manager for environment management.
- **Git:** Version control system for cloning repositories.
- **Jupyter:** For running Jupyter notebooks, ensure Jupyter is installed.
- **Pandas, NumPy, Matplotlib, Seaborn:** Python libraries for data analysis and visualization.
- **Operating System:** Run on Windows.
- **Power BI:** Required for viewing and interacting with Power BI visualizations.

### Dependencies
To replicate the environment used in this project, follow these steps:

1. **Download the environment file:** [environment.yml](environment.yml)
2. **Create and activate the environment:**
    ```sh
    conda create --name your-env-name --file environment.yml
    conda activate your-env-name
    ```
3. **Install additional packages:**
    ```sh
    pip install pandas seaborn matplotlib
    ```

## Usage
1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/your-repo-name.git
    ```
2. **Navigate to the project directory:**
    ```sh
    cd your-repo-name
    ```
3. **Run Jupyter Notebooks:** Start Jupyter Notebook or JupyterLab and open the notebooks located in the `data_preprocessing`, `data_merging`, and `data_analysis` directories.

## Visualizations
Here are some key visualizations from the project:

- **AQI in Urban vs Rural Areas:** ![AQI in Urban vs Rural Areas](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Visualizations/AQI%20%26%20Urban%20and%20Rural%20Areas.png)
- **AQI and Heatwaves:** ![AQI and Heatwaves](https://github.com/alagogianni/Air-Quality-and-Weather-Analysis/blob/main/Visualizations/AQI%20and%20Heatwaves.png)
- **Urban vs Rural Comparison:** ![Urban vs Rural](path-to-image-file.png)

## Results and Findings
Key insights from the analysis include:
- **States of Focus:** Utah, California, Maryland, Arizona, Mississippi.
- **California Hotspots:** San Bernardino, Riverside, Tulare, Kern, Fresno.
- **Temperature Effects:** High temperatures and heatwaves significantly impact AQI.
- **Key Pollutants:** Ozone (O3), PM2.5, and PM10 are major contributors to poor air quality.
- **Seasonal Variations:** AQI trends show higher pollution in summer months; urban areas experience different patterns compared to rural areas.

## Challenges and Limitations
- **Data Gaps:** Some weather data had missing entries, requiring interpolation.
- **Seasonal Bias:** Sparse AQI data in winter months for rural counties.
- **Heatwave Definitions:** Varying definitions of heatwaves across counties.

## Future Work
- **Expand Analysis:** Extend to other highly polluted states like Texas and Illinois.
- **Machine Learning Models:** Predict future AQI trends based on climate data.
- **Integration with Insurance Data:** Incorporate health and insurance claims data for more accurate risk models.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
- Thanks to the **EPA** for providing the air quality data.
- Special thanks to the **Data Analytics Bootcamp** for guidance and mentorship.
- Used libraries and tools:
  - Pandas
  - Seaborn
  - Matplotlib
