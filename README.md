# 🎓 Fair and Explainable AI: Bias Detection and Transparency in Student Performance Prediction

>  *Independent Research Project by Goitom Abirha, exploring fairness and explainability in educational machine learning systems.*

![Python](https://img.shields.io/badge/Python-3.12-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Fairness](https://img.shields.io/badge/Fair--AI-Responsible%20ML-green)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

##  Overview
This self-directed research project investigates **fairness and interpretability** in machine-learning models predicting student academic performance.  
It applies **bias detection**, **fairness auditing**, and **Explainable AI (XAI)** techniques to promote ethical and transparent AI in education systems.

The research explores how data-driven models can be made more **fair, transparent, and socially responsible**, supporting equitable student success.

---

##  Dataset
- **Source:** [UCI Machine Learning Repository – Student Performance Dataset](https://archive.ics.uci.edu/ml/datasets/student+performance)
- **Features:** Demographic, social, and academic variables (e.g., age, gender, study time, absences, parental education, G1–G3 grades)
- **Target Variable:** Final grade (G3)
- **Sensitive Attributes:** Gender, parental education, family income (used to assess fairness)

---

##  Methodology
1. **Exploratory Data Analysis (EDA):** Identify hidden bias and visualize group disparities  
2. **Data Preparation:** Handle missing data, encode categorical variables, normalize features, and balance data using SMOTE  
3. **Model Training:** Compare multiple algorithms (Logistic Regression, Random Forest, SVM)  
4. **Fairness Auditing:** Evaluate bias using fairness metrics (Demographic Parity, Equal Opportunity, Disparate Impact) with IBM AIF360  
5. **Explainability:** Apply SHAP and LIME to interpret predictions  
6. **Deployment:** Develop a Streamlit dashboard to visualize fairness and interpretability results  

---

##  Tools & Libraries
| Category | Tools |
|-----------|--------|
| **Programming** | Python 3.12 |
| **Data Processing** | pandas, numpy |
| **Modeling** | scikit-learn, imblearn |
| **Fairness & Ethics** | IBM AIF360, fairness-metrics |
| **Explainability (XAI)** | SHAP, LIME, PDPbox |
| **Visualization** | matplotlib, seaborn, plotly |
| **Deployment** | Streamlit, Flask |
| **Version Control** | GitHub |

---

---

##  Repository Structure

fair-explainable-ai-student-performance/
│
├── notebooks/
│ ├── 01_eda_bias_analysis.ipynb
│ ├── 02_data_preprocessing.ipynb
│ ├── 03_model_training.ipynb
│ ├── 04_fairness_evaluation.ipynb
│ └── 05_explainability_shap_lime.ipynb
│
├── src/
│ ├── preprocessing.py
│ ├── fairness_metrics.py
│ ├── explainability_tools.py
│ └── app.py
│
├── data/
│ ├── raw/ (link to UCI dataset)
│ └── processed/
│
├── results/
│ ├── eda_visuals/
│ ├── fairness_metrics.csv
│ ├── shap_visuals/
│ └── model_performance.csv
│
├── docs/
│ ├── Research_Proposal_Fair_and_Explainable_AI_Final.pdf
│ ├── Presentation_Slides.pdf
│ └── Screenshots/
│
├── requirements.txt
├── LICENSE
└── README.md



---

## 🗓️ 7-Week Project Roadmap
| **Week** | **Focus Area** | **Deliverables / Files** |
|-----------|----------------|--------------------------|
| Week 1 | Project setup & documentation | Repository structure, proposal, README.md |
| Week 2 | EDA & bias detection | `01_eda_bias_analysis.ipynb` |
| Week 3 | Data preprocessing & feature engineering | `02_data_preprocessing.ipynb` |
| Week 4 | Model training | `03_model_training.ipynb` |
| Week 5 | Fairness evaluation | `04_fairness_evaluation.ipynb` |
| Week 6 | Explainability (SHAP, LIME) | `05_explainability_shap_lime.ipynb` |
| Week 7 | Dashboard & final deployment | `src/app.py`, Streamlit link, documentation |

---

## 📈 Results (Expected Outcomes)
- Quantified bias across gender, parental education, and socioeconomic features  
- Fairness-audited models balancing accuracy and equity  
- Transparent SHAP and LIME explanations for model predictions  
- Interactive Streamlit dashboard demonstrating fairness metrics and interpretability

---

##  Demo
🔗 **[Live Streamlit App – Coming Soon](https://yourappname.streamlit.app)** 

---

##  Example Visuals
| SHAP Summary Plot | Fairness Dashboard |
|--------------------|-------------------|
| ![SHAP Plot](docs/Screenshots/shap_summary.png) | ![Dashboard](docs/Screenshots/dashboard.png) |

---

##  Research Ownership
This project was **conceptualized, developed, and documented independently** by **Goitom Abirha** as part of ongoing professional research in **Responsible and Explainable AI**.  
No external supervision or institutional funding was involved.

---
##  Research Proposal
[![View PDF](https://img.shields.io/badge/View--PDF-Fair%20%26%20Explainable%20AI-blue)](docs/Research_Proposal_Fair_and_Explainable_AI_Final.pdf)
---

##  References
- Barocas, S., Hardt, M., & Narayanan, A. (2019). *Fairness and Machine Learning.*  
- Cortez, P., & Silva, A. (2008). *Using Data Mining to Predict Secondary School Student Performance.*  
- Lundberg, S. M., & Lee, S.-I. (2017). *A Unified Approach to Interpreting Model Predictions.* *NeurIPS.*  
- Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). *“Why Should I Trust You?”* *KDD Conference.*

---

##  Author
**Goitom Abirha**  
 M.Sc. in Data Science — Eastern University  
 Silver Spring, Maryland, USA  

📧 [goitomabirha41@gmail.com](mailto:goitomabirha41@gmail.com)  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/goitom-abirha-089428397)



---

##  License
This project is licensed under the **MIT License** — free to use and modify with proper credit.


## Week 2 — Exploratory Data Analysis & Bias Detection (Final Summary)
 Objective

The goal of Week 2 was to perform a detailed exploratory analysis (EDA) of the Student Performance dataset and identify early signs of bias across demographic and socio-economic groups. This step establishes the foundation for building fair and explainable machine-learning models in later weeks.

 Data Overview

•	Combined dataset size: 1044 students, 33 features
•	Two original datasets merged: Math and Portuguese
•	No missing values
•	16 numeric variables and 17 categorical variables

Key Analyses Performed
1. Univariate Exploration
•	Histograms for numeric features (age, absences, studytime, grades)
•	Bar plots for categorical features (sex, school, parental education, internet)
•	Visuals saved to figures/eda/
•	These plots help understand the distribution and balance of the dataset.

2. Correlation Analysis

•	Generated a correlation heatmap for all numeric features
•	Found strongest predictors of final grade (G3):

o	G2 (previous grade)
o	G1
o	Studytime
o	Failures (negative correlation)
This helps guide feature selection for future modeling.

3. Bias-Oriented Group Analysis

Examined mean G3 across key groups:

Attribute	                              Gap Between Groups	              Key Observation
Mother's Education (Medu)	      2.33 points                             	 largest difference
Father's Education (Fedu)	      1.97 points	                                    Strong socio-economic factor
School (GP vs MS)	                  1.12 points     	                        GP students perform higher
Internet Access	                  1.02 points	                                    Digital divide effect
Gender                                          0.24 points     	                        smallest gap

These findings suggest that socio-economic factors show stronger disparities than gender or family structure.

 Fairness Insights

•	Early indicators of potential unfairness include:
•	Higher grades for students with more educated parents
•	Performance difference between schools (GP vs MS)
•	Performance advantage for students with internet access
•	Lower performance among students in romantic relationships (possible stress/time constraint?)
These disparities will guide Feature Engineering (Week 3) and Fairness Auditing (Week 5).
Outputs Generated

•	figures/eda/*.png — all histograms, bar plots, boxplots, heatmaps
•	reports/group_target_stats.csv — descriptive stats by group
•	reports/initial_bias_gaps.csv — gap analysis
•	reports/eda_bias_notes.md — auto-generated narrative report
•	Updated notebook: 01_eda_bias_analysis.ipynb

