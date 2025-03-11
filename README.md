# London Traffic Accident Analysis Project
## Project Overview
This research aims to analyze the spatiotemporal patterns of traffic accidents in London, identify influencing factors, and develop predictive models to provide scientific evidence for urban traffic management.

## Research Objectives
1. Analyze the spatiotemporal distribution of traffic accidents in London
2. Identify key factors influencing accident occurrence
3. Develop prediction models for high-risk areas

## Data Description

### Transport Data
- Accident data: location, severity, time information
- Traffic flow: average daily flow by area
- Road characteristics: road type, speed limits, pedestrian crossings, junction control

### Socio-Economic Data
- Population density
- Index of Multiple Deprivation (IMD)
- Employment data
- Car ownership rates
- Income levels
- Commuting patterns

## Analysis Framework

### 1. Spatiotemporal Pattern Analysis
- **Spatial Analysis**
  - Accident density heatmap
  - Hotspot analysis
  - Spatial autocorrelation analysis
- **Temporal Analysis**
  - Accident trend analysis
  - Peak vs. night-time accident comparison

### 2. Factor Analysis
- **Feature Importance Analysis**
  - Correlation analysis
  - Random Forest feature importance
  - Principal Component Analysis
- **Regression & Causal Analysis**
  - Linear regression
  - Panel regression
  - Causal inference

### 3. Prediction Models
- **Machine Learning Models**
  - Classification models (accident severity prediction)
  - Cluster analysis (high-risk area identification)
  - Time series forecasting

## File Structure
data/processed/
├── social-enconmic/
│   ├── cleaned_carownerrate.csv    # Car ownership data
│   ├── cleaned_icda.csv           # Socio-economic indicators
│   ├── cleaned_income.csv         # Income data
│   ├── cleaned_incomeemploy.csv   # Employment and income data
│   └── cleaned_poverty1.csv       # Poverty indicators
└── transport/                     # Transport-related data

## Expected Outcomes
1. Identification of high-risk accident areas in London
2. Quantification of factor importance
3. Development of reliable accident prediction models
4. Policy recommendations for traffic management

## Technical Stack
- Python
- Data Analysis: Pandas, NumPy
- Spatial Analysis: GeoPandas, Folium
- Machine Learning: Scikit-learn, XGBoost
- Visualization: Matplotlib, Seaborn
- Statistical Analysis: StatsModels

## Methodology
The research follows a three-stage approach:
1. Exploratory Data Analysis
2. Statistical Modeling
3. Predictive Analytics

## Future Work
- Integration with real-time traffic data
- Development of interactive visualization dashboard
- Extension of the model to other UK cities