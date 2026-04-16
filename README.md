# STAT 486 Final Project: Lung Cancer Survival Prediction and Patient Subtype Clustering

This is the final project for STAT 486 (Machine Learning) at Brigham Young University. The project focuses on analyzing lung cancer data from the National Cancer Database (NCDB) to build predictive models for patient survival and identify patient subtypes through clustering.

## Research Question

Can unsupervised clustering of lung cancer patients reveal subgroups that meaningfully explain variation in supervised survival predictions, and does incorporating clustering improve model performance?

## Project Components

### Supervised Component: Survival Prediction
Build a survival regression model predicting overall survival or 5-year survival probability using:
- Patient demographics
- Tumor stage and histology
- Treatment variables (surgery, chemotherapy, radiation)
- Comorbidity scores

Potential models:
- Cox proportional hazards model
- Random survival forests
- DeepSurv

### Unsupervised Component: Patient Subtype Clustering
Use clustering to discover lung cancer subtypes that share clinical characteristics and survival outcomes.

Potential clustering features:
- Tumor size
- Stage group
- Nodal involvement
- Treatment modality combinations
- Age, insurance status, facility type

Potential methods:
- k-means (after feature scaling)
- Gaussian Mixture Models
- Hierarchical clustering

## Data

The primary dataset is the National Cancer Database (NCDB) lung cancer dataset. A backup dataset is the publicly accessible SEER lung cancer dataset for external validation if needed.

## Setup and Installation

1. Clone this repository.
2. Install the required packages:
   ```
   uv init
   uv sync
   ```
3. Follow the instructions in `data/README.md` to access the data

## Project Structure

- `demo.ipynb`: Demonstration notebook for the project containing code to read in the data and plot Kaplan-Meier curves stratied by a choice of categorical variables
- `src/`: Code to explore, clean, visualize, and analyze the data
- `data/`: Data files
- `progress/`: Progress reports
- `pyproject.toml`: Python dependencies

## Run Order

In the `src` folder, there are three .ipynb notebooks:

* `01_eda.ipynb`
* `02_clean.ipynb`
* `03_analysis.ipynb`

For start-to-finish reproducibility, follow along and run the code in each of the files in order (`eda` first, then `clean`, and lastly `analysis`). However, if the clean, ready-to-analyze data is desired, one may begin with the code in `03_analysis.ipynb`.

## Ethical Considerations

This work complies with NCDB's data use restrictions, emphasizing de-identification and refraining from making clinical recommendations.


