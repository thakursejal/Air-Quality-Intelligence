# 🌫️ Air Quality Intelligence — Data Analytics, Predictive Insights & Decision Support

## 📌 Project Overview

**Air Quality Intelligence** is an end-to-end data analytics and machine learning project that transforms real-world air-quality monitoring data into meaningful insights and decision-support information.

The project follows the workflow:

**Data → Information → Insight → Decision → Action**

It includes data cleaning, exploratory data analysis, pollutant analysis, geographic analysis, machine learning, model evaluation, KPI generation, visualization, and analytical decision support.

---

## 🎯 Objectives

- Clean and preprocess air-quality monitoring data.
- Understand the structure and quality of the dataset.
- Analyze pollutant-level patterns.
- Explore city, state, and station-level observations.
- Perform exploratory data analysis and visualization.
- Analyze geographic monitoring patterns.
- Build machine-learning models for pollutant-value estimation.
- Evaluate models using MAE, RMSE, and R².
- Generate project KPIs.
- Identify locations requiring priority monitoring.
- Create data-driven decision-support outputs.

---

## 📊 Dataset

The project uses the Government of India Open Government Data dataset:

**Real time Air Quality Index from various locations**

The dataset contains air-quality observations from monitoring locations and includes fields such as:

- Country
- State
- City
- Station
- Last Update
- Latitude
- Longitude
- Pollutant ID
- Pollutant Minimum
- Pollutant Maximum
- Pollutant Average

### Dataset Source

Government of India Open Government Data Platform / Central Pollution Control Board (CPCB).

The dataset is used for academic analysis.

---

## 🔄 Project Workflow

Data Collection  
↓  
Dataset Profiling  
↓  
Data Cleaning & Quality Control  
↓  
Exploratory Data Analysis  
↓  
Pollution Pattern Analysis  
↓  
Geographic Analysis  
↓  
Machine Learning  
↓  
Model Evaluation  
↓  
Decision Support  
↓  
KPI Generation  
↓  
Final Visualizations & Outputs

---

## 🧹 Data Cleaning & Preprocessing

The project performs data-quality checks and preprocessing before analysis.

The workflow includes:

- Dataset structure inspection
- Missing-value inspection
- Duplicate checking
- Data-type validation
- Numerical-field preparation
- Categorical feature preparation
- Feature preparation for machine learning
- Cleaned dataset export

The cleaned dataset is saved as:

`cleaned_air_quality_data.csv`

---

## 🔎 Exploratory Data Analysis

The exploratory analysis examines:

- Pollutant observation coverage
- Average pollutant values
- City-level observation coverage
- Geographic patterns
- Available date/time information
- Relative pollutant levels

Visualizations are used to make the analytical findings easier to understand.

---

## 🤖 Machine Learning

The project includes a genuine machine-learning component for **pollutant-value estimation**.

### Models Used

1. **Linear Regression**
2. **Random Forest Regressor**

### Target Variable

`pollutant_avg`

### Features

The model uses available pollutant and location-related information, including:

- Pollutant identity
- State
- City
- Station
- Latitude
- Longitude

Categorical features are encoded before model training.

The dataset is divided into training and testing subsets using an **80:20 split** with a fixed random state.

---

## 📏 Model Evaluation

The models are evaluated using:

- **MAE — Mean Absolute Error**
- **RMSE — Root Mean Squared Error**
- **R² — Coefficient of Determination**

The model comparison is saved as:

`model_comparison.csv`

### Important Note

The available dataset represents a current monitoring snapshot rather than a long historical time series.

Therefore, this project **does not claim long-term future pollution forecasting**.

The machine-learning component is presented as **pollutant-value estimation using the available observations and features**.

---

## 📍 Geographic & Hotspot Analysis

Location-related fields are used to analyze monitoring patterns across:

- States
- Cities
- Stations
- Latitude
- Longitude

The project identifies locations associated with relatively higher observed pollutant levels and generates priority monitoring information.

The output is saved as:

`priority_locations.csv`

---

## 📊 Decision Support

A percentile-based analytical framework is used to classify observations into relative pollutant-level categories.

| Category | Analytical Range |
|---|---|
| Lower Relative Level | Below 50th percentile |
| Moderate | 50th to below 75th percentile |
| High | 75th to below 90th percentile |
| Very High | 90th percentile and above |

### Important Disclaimer

These categories are **project-defined analytical signals**.

They are **not official AQI categories** and should not be interpreted as medical or health-risk classifications.

---

## 📈 Executive KPIs

The project generates summary KPIs covering:

- Total observations
- Number of states
- Number of cities
- Number of monitoring stations
- Number of pollutant types
- Higher-level observations

The KPI output is saved as:

`kpi_summary.csv`

---

## 📁 Generated Project Outputs

The project generates the following analytical files:

- `cleaned_air_quality_data.csv`
- `model_comparison.csv`
- `pollutant_summary.csv`
- `priority_locations.csv`
- `kpi_summary.csv`

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- OpenPyXL
- Python-docx
- Google Colab

---

## 📂 Project Structure

Air-Quality-Intelligence/

    ├── ThakurSejal_AirQualityIntelligence.ipynb
    ├── ThakurSejal_AirQualityIntelligence_ProjectReport.docx
    ├── requirements.txt
    ├── README.md
    │
    └── project_outputs/
        ├── cleaned_air_quality_data.csv
        ├── model_comparison.csv
        ├── pollutant_summary.csv
        ├── priority_locations.csv
        └── kpi_summary.csv

---

## ▶️ How to Run the Project

### 1. Install the required packages

    pip install -r requirements.txt

### 2. Open the notebook

Open:

`ThakurSejal_AirQualityIntelligence.ipynb`

using Google Colab or a compatible Jupyter Notebook environment.

### 3. Upload the dataset

The notebook expects the dataset:

`air_quality_data.csv.xlsx`

### 4. Run the notebook

Execute the notebook cells in order from the beginning through the final project-output section.

The notebook generates the cleaned data, model results, summaries, priority locations, KPIs, and visualizations.

---

## 🌍 Sustainable Development Goals

This project is aligned with the following UN Sustainable Development Goals:

### SDG 3 — Good Health and Well-Being

Air-quality monitoring provides environmental information relevant to public well-being.

### SDG 11 — Sustainable Cities and Communities

Location-based air-quality analysis supports understanding of urban environmental conditions.

### SDG 13 — Climate Action

Data-driven environmental monitoring contributes to environmental awareness and analytical decision support.

---

## ⚠️ Limitations

- The available dataset is a current snapshot rather than a long historical time series.
- The project does not claim long-term time-series forecasting.
- Relative-level categories are project-defined analytical signals and are not official AQI classifications.
- Model performance depends on the available features and observations.
- Random train-test splitting may produce optimistic generalization estimates when similar station or pollutant observations occur in both subsets.

---

## 🔮 Future Scope

Future improvements could include:

- Integrating longer historical air-quality time-series data.
- Developing genuine time-series forecasting models.
- Incorporating meteorological variables such as temperature, humidity, wind, and rainfall.
- Using grouped or time-based validation for stronger model evaluation.
- Developing an interactive Power BI, Tableau, or web-based dashboard.
- Automating data updates from official monitoring sources.
- Adding explainable machine-learning techniques.

---

## 📚 References

- Government of India Open Government Data Platform — Real time Air Quality Index from various locations.
- Central Pollution Control Board (CPCB) — Air-quality monitoring information.
- Python scientific computing and data-analysis ecosystem.
- Scikit-learn documentation for machine-learning algorithms and evaluation metrics.

---

## 👩‍💻 Author

**ThakurSejal**

### Project

**Air Quality Intelligence — Data Analytics, Predictive Insights & Decision Support**

### Program

**AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026**

---

## ⭐ Conclusion

Air Quality Intelligence demonstrates an end-to-end data-to-decision workflow using real-world air-quality observations.

The project combines data preprocessing, exploratory analysis, visualization, geographic analysis, machine learning, model evaluation, KPI generation, and decision-support analysis to transform raw monitoring observations into structured and interpretable analytical outputs.