# Smart Travel Advisor

Smart Travel Advisor is a notebook-based data science project that explores travel planning with machine learning. It combines trip data, destination cost-of-living data, weather data, and health data to estimate travel cost, assess trip suitability, predict disease risk, and group destinations into clusters.

## What It Does

- Predicts total trip cost from trip duration and traveler age
- Predicts disease cases from weather and environmental inputs
- Classifies whether a trip is suitable based on travel conditions
- Clusters destinations using weather and cost-of-living features
- Visualizes key distributions and model outputs with charts

## Project Files

- [Smart_Travel_Advisor.ipynb](Smart_Travel_Advisor.ipynb) - main notebook with data loading, cleaning, modeling, and visualizations
- [travel_trip_data.csv](travel_trip_data.csv) - trip records with traveler and cost details
- [cost_data.csv](cost_data.csv) - cost-of-living data by country
- [weather_data.csv](weather_data.csv) - weather observations by city and country
- [health_data.csv](health_data.csv) - health/environment data used for disease case prediction

## Dataset Overview

The notebook uses the following fields from the CSV files:

- Trip data: `Destination`, `Start date`, `End date`, `Duration (days)`, `Traveler age`, `Accommodation cost`, `Transportation cost`
- Cost data: `Country`, `Cost of Living Index`, `Rent Index`, `Groceries Index`, `Restaurant Price Index`, `Local Purchasing Power Index`
- Weather data: `City`, `Country`, `temperature`, `humidity`, `pressure`, `wind_speed`, `weather_description`
- Health data: `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`

## Requirements

Use Python 3.9+ with these packages:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

## How To Run

1. Open the repository folder in VS Code or Jupyter Notebook.
2. Install the required Python packages if needed.
3. Open [Smart_Travel_Advisor.ipynb](Smart_Travel_Advisor.ipynb).
4. Run the cells from top to bottom.

Example install command:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

## Workflow Summary

1. Load the CSV files into pandas DataFrames.
2. Clean and normalize trip data.
3. Merge trip, weather, and cost data by country.
4. Train a linear regression model for trip cost prediction.
5. Train a linear regression model for health risk prediction.
6. Train and compare classifiers for travel suitability.
7. Apply K-Means clustering to destination features.
8. Plot distributions, scatter plots, and comparison charts.

## Notes

- The notebook is exploratory and assumes the CSV files remain in the project root.
- Some cells rely on previously created variables, so running cells in order matters.
- If you change the CSV structure, update the notebook column names accordingly.
