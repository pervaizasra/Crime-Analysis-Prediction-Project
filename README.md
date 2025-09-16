# Crime-Analysis-Prediction-Project
**📌 Project Overview**

This project analyzes NYPD crime data to uncover patterns, understand victim demographics, explore weapon–crime relationships, and build predictive models. It also includes an interactive Power BI dashboard for storytelling and decision support.

The project demonstrates data science + business intelligence skills with a strong social impact angle.

## 📑 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#Methodology)
- [Project Workflow](#project-workflow)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Machine Learning Models](#machine-learning-models)
- [Dashboard](#dashboard)
- [Results](#results)
- [How to Run](#how-to-run)
- [Repository Structure](#repository-structure)
- [Future Work](#future-work)
- [License](#license)

---

**🎯 Objectives**

- Explore crime trends and distributions across time, cities, and crime domains.

- Investigate victim demographics (age, gender) and their relation to crime.

- Analyze weapon usage across different crime domains.

- Build machine learning models to predict crime categories and weapon types.

- Create a Power BI dashboard to summarize findings for stakeholders.

  ## 📂 Dataset
- **Source:** Public crime dataset (NYPD Shooting Incidents & others).  
- **Size:** ~### rows, ### columns.  
- **Key Features:**
  - `OCCUR_DATE` – Date of crime occurrence  
  - `BORO` – Borough (NYC crime location)  
  - `PERP_RACE` – Perpetrator race  
  - `VIC_RACE` – Victim race  
  - `WEAPON` – Weapon involved  
  - `CRIME_DOMAIN` – Violent/Non-Violent  

---

  **🛠 Methodology**

 **1. Data Cleaning & Preprocessing**

        - Handled missing values (case closure dates, weapon info).

        - Feature engineering (age groups, case duration, case open/closed flag).

  **2. Exploratory Data Analysis (EDA)**

        - Crime frequency trends (monthly & daily).

         - Victim demographics vs. crime type.
     
         - Weapon usage distribution.

   **3. Machine Learning Models**

      - Random Forest classifier for crime domain prediction.

      - SMOTE applied to handle class imbalance.

      - Accuracy ~30–50% → showing the complexity of real-world crime prediction.

   **4. Dashboard Development (Power BI)**

      - Executive Summary: KPIs & crime distribution.

      - Trends: Crimes per month/day & domain breakdown.

      - Victim Demographics: Gender & age vs. crime.

      - Weapon Analysis: Weapon vs. crime domain relationships.
 ## 🔄 Project Workflow
1. **Data Cleaning & Preprocessing** – Handling nulls, duplicates, formatting.  
2. **EDA** – Identifying hotspots, crime trends, demographics.  
3. **Modeling** – Classification models for crime prediction.  
4. **Visualization** – Power BI dashboard with actionable insights.  

---
## 🔍 Exploratory Data Analysis (EDA)

### Crime Domain Distribution
![Crime Domain Distribution]<img width="1132" height="605" alt="image" src="https://github.com/user-attachments/assets/47f23586-9abd-413f-ad49-0127976fc38e" />
🔎 Majority of crimes fall under "Other Crime" (57%), followed by "Violent Crime" (28%).  
This highlights the importance of non-violent categories in urban crime analysis.

### Victim Demographics
![Victim Demographics]<img width="1276" height="720" alt="image" src="https://github.com/user-attachments/assets/8f8628c2-4830-4ae1-bbfb-0a2df073a1f7" />
🔎 This analyzes 11,472 reported crimes across five major Indian cities from 2020 to 2024, revealing that Young Adults (18–35) are the most affected age group, with males comprising the majority of victims in violent and property crimes

### Weapon vs Crime Domain
![Weapon vs Crime Domain]<img width="1288" height="720" alt="image" src="https://github.com/user-attachments/assets/f5438444-1804-428f-9954-19f3954aa53d" />
🔎 This reveals that knives and blunt objects are the most frequently used weapons in violent crimes across cities like Bangalore and Ahmedabad, with fire-related incidents dominating traffic fatalities and fire accidents.

---
## 🤖 Machine Learning Models
- **Random Forest Classifier**  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1
- **SMOTE for Imbalancing**
 ***Before SMOTE*** 
Accuracy: 0.5174302788844621
Classification report:
                   precision    recall  f1-score   support

   Fire Accident       0.07      0.02      0.03       765
     Other Crime       0.57      0.85      0.68      4590
Traffic Fatality       0.03      0.01      0.01       383
   Violent Crime       0.26      0.10      0.15      2294

        accuracy                           0.52      8032
       macro avg       0.23      0.24      0.22      8032
    weighted avg       0.41      0.52      0.43      8032
   ***After SMOTE***
            precision    recall  f1-score   support

   Fire Accident       0.09      0.17      0.12       765
     Other Crime       0.57      0.37      0.45      4590
Traffic Fatality       0.05      0.22      0.08       383
   Violent Crime       0.27      0.22      0.25      2294

        accuracy                           0.30      8032
       macro avg       0.25      0.25      0.22      8032
    weighted avg       0.41      0.30      0.34      8032
  ## 📊 Dashboard

### Executive Summary
![Executive Summary]<img width="1286" height="722" alt="image" src="https://github.com/user-attachments/assets/ed6ad7a3-c7ee-410f-9974-287ef595a8a4" />
Violent crime dominates the landscape across major Indian cities, with Delhi showing the highest concentration. Knife and blunt object incidents are especially prevalent, underscoring the need for targeted safety interventions and urban crime prevention strategies.

### Crime Trends
![Crime Trends]<img width="1264" height="727" alt="image" src="https://github.com/user-attachments/assets/b5620ca0-cea9-4c37-ac94-6db62f911483" />
Violent crime shows a sharp decline post-2022, while city-level trends reveal fluctuating patterns across domains—suggesting shifts in urban safety dynamics and the evolving impact of local interventions.
---
# ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/crime-data-analysis.git
cd crime-data-analysis
### 2. Install dependencies
pip install -r requirements.txt
### 3. Run Jupyter Notebook
jupyter notebook notebooks/EDA.ipynb
4. Open Power BI Dashboard

Load https://github.com/pervaizasra/Crime-Analysis-Prediction-Project/blob/main/Dashboard/Indian%20Crime%20Analysis.pbix in Power BI Desktop.

📁 Repository Structure

crime-data-analysis/
│
├── data/                # Raw & cleaned datasets
├── notebooks/           # Jupyter notebooks (EDA, Modeling)
├── dashboard/           # Power BI dashboard files
├── images/              # Screenshots for README
├── requirements.txt     # Python dependencies
└── README.md

🚀 Future Work

Add deep learning models for crime trend prediction.

Integrate real-time data pipelines (Kafka + Spark).

Expand dashboard with forecasting capabilities.

📜 License

This project is licensed under the MIT License.
