# Machine Learning and Health Data
**Machine Learning-Based Mortality Prediction in ICU Patients with Acute Kidney Injury: A Retrospective Analysis Using the MIMIC-IV Database**
This is an on-going project for COMP90089. This repo will include the working codes and research proposal illustrating our overall approach and research goal. 

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
