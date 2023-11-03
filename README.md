# Machine Learning and Health Data
## **Machine Learning-Based Mortality Prediction in ICU Patients with Acute Kidney Injury: A Retrospective Analysis Using the MIMIC-IV Database**

This is an on-going project for COMP90089. This repo will include the working codes and research proposal illustrating our overall approach and research goal. 
## Team Details

- **Jiahe Liu**
  - ID: 1214235
  - Email: [jiahe3@student.unimelb.edu.au](mailto:jiahe3@student.unimelb.edu.au)

- **Quan Yi**
  - ID: 1054540
  - Email: [quyi@student.unimelb.edu.au](mailto:quyi@student.unimelb.edu.au)

- **Wedad Amer**
  - ID: 1081635
  - Email: [wamer@student.unimelb.edu.au](mailto:wamer@student.unimelb.edu.au)

- **Vaibhav Singh Makhloga**
  - ID: 1424591
  - Email: [vmakhloga@student.unimelb.edu.au](mailto:vmakhloga@student.unimelb.edu.au)

- **Jay Acharya**
  - ID: 1401435
  - Email: [acharyaj@student.unimelb.edu.au](mailto:acharyaj@student.unimelb.edu.au)

## Project Description

**Background:** Acute Kidney Injury (AKI) frequently occurs within Intensive Care Units (ICU). The potential for machine learning to utilize patient demographics, existing health conditions, and laboratory test results to forecast the progression of AKI has not been thoroughly explored.

**Methods:** We selected patient data from the MIMIC-IV database who met the criteria for AKI digital phenotype and categorized them according to survival outcomes. The main aim was to construct a composite machine learning framework capable of predicting mortality due to AKI. The development of this model involved the use of logistic regression for feature selection and heatmap correlation for analytical insights.

**Results:** The research encompassed data from 9,809 patients in the ICU, with 1,659 reported fatalities. The feature selection methodology enabled the identification of pivotal risk factors. The composite model demonstrated an 82.77% precision rate in forecasting fatal outcomes.

**Conclusions:** The application of machine learning techniques to MIMIC-IV dataset appears to be a highly promising strategy for prognosticating mortality among ICU patients suffering from AKI. This method holds the potential to significantly enhance patient management by enabling earlier interventions.

**Keywords:** Acute Kidney Injury, Machine Learning, MIMIC-IV Database, ICU Mortality.

## Research Proposal
The initial focus of our research was on patients with stage II hypertension, but following recommendations from our academic advisors, we shifted our emphasis to acute kidney injury, which is more relevant to the ICU setting. Despite this change in focus, our underlying research methodology remains consistent.

## Scripts
`/notebook/` directory include the scripts used for data collection, data preprocessing and modeling:
- `/notebook/1.data_collection`: This notebook describes the process of selecting intended AKI cohort through filtering by digital phenotype and predefined inclusion and exclusion criteria. This notebook needs to be run through google collab with credential for accessing MIMIC-IV database.
- `/notebook/2.data_preprocessing`: This notebook includes the preprocessing steps: 
    - Basic EDA
    - Identifying and removing outliers
    - Missing value imputation
    - Between-feature correlation analysis
    - Feature selection (risk factor analysis)
- `/notebook/3.baseline_model`: This notebook includes the baseline modeling & imbalance data handling steps. We explored the following models and resampling techniques and compared the accuracy:
    - Binary classification models: linear regression, logistic regression, dummy classifier, decision tree, random forest, SVM
    - Resampling techniques: random oversampling, SMOTE, ADASYN
- `/notebook/Regression Optimisation`: They fine-tuned a regression model.
- `/notebook/Decision Tree Optimisation`: They improved a decision tree's accuracy.
- `/notebook/Ensemble Model`: They built or refined a combined predictive model.

## Data

The dataset located at `/data/df_final_AKI.csv` is utilised for crafting our machine learning model. In this dataset, the `dod` column signifies the mortality rate, which is our primary target for prediction. Meanwhile, `subject_id` denotes the unique identifier for each patient. All other columns represent crucial clinical, lab, and demographic attributes that can serve as predictor variables. 

As we filtered for different features, `/data/clinic_df.csv`,  `/data/lab_df.csv`,  `/data/comorbidity.csv` refers to clinical features, lab-based features and comorbidity respectively.


## Setup & Environment
Python version: >= 3.9

### Libraries Used:
- pandas
- numpy
- matplotlib
- seaborn
- sklearn

### Instructions to Set Up the Environment:
1. Clone the repository: `git clone [repository-link]`
2. Navigate to the project directory: `cd [directory-name]`
3. Create a virtual environment: `python -m venv venv`
4. Activate the virtual environment:
   - On Windows: `venv\Scripts\activate`
   - On macOS and Linux: `source venv/bin/activate`
5. Install the required packages: `pip install -r requirements.txt`
6. Launch Jupyter Notebook: `jupyter notebook`
7. Open the provided notebook and run the cells.
