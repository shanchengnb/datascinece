# Title:
Predicting and Explaining Road Traffic Accident Severity in Inner London Using Interpretable Machine Learning

## 📍 Objective
This project investigates how road design, temporal patterns, and environmental conditions impact the severity of road traffic accidents in Inner London. The goal is to both predict and explain accident outcomes using interpretable machine learning methods.

## 🧠 Methodology Summary
We employed a three-pronged approach:

Descriptive & Statistical Analysis (Method 1):
Explored accident severity patterns across time, road type, junction control, lighting, weather, and surface conditions. Chi-squared tests confirmed key variables significantly associated with severity (p < 0.001).

KMeans Clustering (Method 2):
Identified four distinct clusters of accident conditions, revealing high-risk combinations such as late-night crashes at uncontrolled junctions, and daytime traffic at complex intersections.

Supervised Classification Models (Method 3):
Compared Logistic Regression, Random Forest, and XGBoost to predict accident severity (Slight vs Serious/Fatal).

Applied SMOTE, threshold tuning, and class weighting to address class imbalance.

Used SHAP for model interpretability.

Final soft voting ensemble (LogReg:1, RF:1, XGB:2, threshold = 0.24) prioritized recall of serious/fatal incidents.

## 📊 Key Findings
1️⃣ Temporal Risk Patterns
Serious and fatal accidents are significantly more likely to occur between 12:00 AM and 4:00 AM, especially on weekends (notably Sundays).

Driver fatigue, reduced visibility, and alcohol-related behaviors are likely contributing factors.

Temporal variables such as hour, weekday/weekend, and time period classification ranked among the most important predictors in SHAP analysis.

2️⃣ Road Design and Infrastructure
Single carriageways, high-speed roads, and complex/uncontrolled junctions (e.g., slip roads, roundabouts, T-junctions) are strongly associated with higher accident severity.

Areas with limited or no signal control are particularly high-risk.

SHAP values and feature importance from tree-based models highlighted junction control type and carriageway class as top contributors to serious/fatal outcomes.

3️⃣ Environmental Conditions
Darkness without street lighting, wet or icy surfaces, and adverse weather conditions (e.g., snow, heavy rain with wind) significantly increase accident severity.

These environmental variables were statistically significant (p < 0.001) in chi-squared tests and were among the top-ranked SHAP features.

4️⃣ Clustering Insights
KMeans clustering identified four distinct accident profiles:

Cluster 0: Typical daytime traffic at roundabouts or crossroads.

Cluster 1: Early morning, low-speed crashes at give-way junctions.

Cluster 2: Evening and nighttime accidents, likely linked to fatigue and low visibility.

Cluster 3: High-density, signal-controlled areas with complex intersections—risky despite lower speed limits.

These clusters help localize and contextualize severity risk across boroughs and time windows.

5️⃣ Modeling Insights & Severity Prediction
Logistic Regression provided high recall for serious/fatal cases with SMOTE and class weighting but suffered from low precision, making it suitable for high-alert screening tools.

Random Forest offered better balance between precision and recall, capturing complex interactions.

XGBoost, when paired with SMOTE and threshold tuning, achieved the best recall on high-risk cases.

The final ensemble model (LogReg:1, RF:1, XGB:2, threshold = 0.24) optimized for recall, making it ideal for safety-critical applications.

SHAP interpretability confirmed that time, road type, junction control, and environmental conditions are key to predicting severity.

## 🟢 Implications 
The findings of this study offer actionable insights for urban planners, transport authorities, and policymakers aiming to reduce the severity of road traffic accidents in Inner London and similar urban environments. Key recommendations include:

1️⃣ Temporal Risk Management
Late-night enforcement:
Accidents between 12 AM and 4 AM are significantly more likely to be serious or fatal. This suggests a need for increased police presence, sobriety checkpoints, and speed monitoring during these hours—especially on weekends.

Time-aware traffic control:
Implement dynamic speed limits and traffic calming measures during high-risk periods, such as weekend nights and early mornings.

2️⃣ Infrastructure Redesign at High-Risk Locations
Junction reengineering:
High-severity crashes frequently occur at complex or uncontrolled intersections (e.g., roundabouts, T-junctions, slip roads). These areas should be prioritized for:

Improved traffic signal installation,

Redesigned lane configurations,

Raised markings or rumble strips to enhance driver awareness.

Carriageway upgrades:
Narrow, single carriageways in high-speed zones should be redesigned with speed reduction elements, clear signage, or separation barriers.

3️⃣ Environment-Responsive Safety Measures
Visibility improvements:
Poor lighting is a critical factor in serious crashes. Solutions include:

LED street lighting in high-risk corridors,

Reflective road paint and cat’s eyes at bends or intersections.

Weather-adaptive systems:
Install real-time warning signs and variable speed limit systems that respond to adverse weather (e.g., fog, rain, snow).
Use high-friction surface materials in locations prone to skidding or hydroplaning.

4️⃣ Data-Informed Policy and Planning
The machine learning models, particularly the ensemble, offer a practical and interpretable tool to support:

Hotspot detection and risk mapping,

Resource allocation for enforcement and maintenance,

Pre-emptive infrastructure upgrades in emerging risk zones.

SHAP-based explainability ensures decision-makers can trace the model’s reasoning, fostering transparency and trust in AI-assisted planning tools.

## 📁 Data Sources
UK STATS19: Road Collisions and Casualties

Inner London Boundaries (GLA / GeoJSON)

Data processed to accident-level with demographic aggregation (e.g., number of casualties, average age, gender ratio)

## ⚙️ Environment
Platform: Anaconda (Python 3.9)

Runtime: ~15 min

Machine: Intel i7, 17 GB RAM

Key Libraries:

xgboost, shap, imbalanced-learn, psutil (additional)

scikit-learn, pandas, geopandas, matplotlib, folium (standard)



