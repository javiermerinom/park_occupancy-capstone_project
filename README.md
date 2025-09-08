# Park Usage Analytics Dashboard

## 🏗️ Project Context  
This project was developed in collaboration with the **City of Vancouver** as a capstone team project for Langara College’s Data Analytics Program. It addresses the challenge of limited visibility into park usage patterns and supports the Vancouver Park Board in planning, operations, and resource allocation.  

⚠️ Note: This repository does **not** include raw datasets due to size and access restrictions. Instead, it contains code and scripts to showcase ingestion, transformation, forecasting, and dashboard integration steps.  

---

## 📌 Project Overview  
The **Park Usage Analytics Dashboard** integrates multiple data sources into a unified analytics solution to provide insights into how, when, and where parks are used across Vancouver. Built in **Microsoft Fabric**, the project delivers descriptive and predictive analytics through a **Power BI dashboard**, combining live and historical usage data, weather, amenities, and events.  

---

## 🎯 Objective  
- Uncover meaningful patterns in park usage.  
- Support **smarter resource allocation** and **strategic planning**.  
- Improve **visitor flow** and **accessibility**.  
- Enhance **sustainable and enjoyable park experiences**.  

---

## 🛠 Tools & Technologies  
- **Microsoft Fabric** (Lakehouse, Notebooks, Data Pipelines, OneLake)  
- **Power BI** (semantic model, interactive dashboards)  
- **Machine Learning**: XGBoost, LightGBM for forecasting & user estimation  
- **Languages**: Python (ETL, ML)  
- **Data Sources**:  
  - Google Popular Times (Live & Usual)  
  - Observational Study counts  
  - Weather data (historical & forecast)  
  - Park amenities, classifications, and IDs  
  - Park events & BC holidays  

---

## 📊 Key Steps  
1. **Data Ingestion & Transformation**  
   - Pipeline 1: Load raw CSVs → create clean dimension & fact tables (Bronze → Silver → Gold).  
2. **User Estimation**  
   - Pipeline 2: Train XGBoost model using static + weather features to predict daily user counts.  
3. **Forecasting Model**  
   - Pipeline 3: Train LightGBM model to forecast weekly occupancy using weather and event features.  
4. **Occupancy Prediction**  
   - Pipeline 4: Generate 7-day hourly forecasts with confidence intervals per park.  
5. **Visualization**  
   - Publish results via semantic model → Power BI dashboard.  

---

## 🚀 Results  
- **Descriptive Analytics**:  
  - Occupancy patterns by hour, day, week, and month.  
  - Filters by park classification, amenities, location, and maintenance area.  
  - KPIs: peak/off-peak hours, live vs. average busy times, users per hectare, bus stops per hectare.  

- **Predictive Analytics**:  
  - Daily user estimates by park.  
  - 7-day occupancy forecasts for operational planning.  
  - Integration of weather and events improves forecast accuracy.  

- **Impact**:  
  - Provides park managers with actionable insights for staffing, maintenance, and resource allocation.  
  - Enables long-term strategic planning with data-driven evidence.  

---

## 📂 Repository Structure  
```bash
├── Documentation/      # Presentation and Report
├── Output/            # Forecasting, Dashboard Screen-Shot
├── Src/            # JSON pipeline definitions (Data Ingestion, Estimation, Forecasting), measurement for Semantic Model
├── README.md             # This file
```

---

## 🙌 Acknowledgments  
Developed by:  
- Javier Merino  
- Meyliani Sanjaya  
- Angeli De los Reyes  
- Nay Zaw Lin  
