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
   pip install -r requirements.txt
   ```
3. Ensure you have access to the NCDB data (not included in this repository due to data use restrictions).

## Project Structure

- `demo.ipynb`: Demonstration notebook for the project.
- `src/analysis_example.ipynb`: Example analysis notebook.
- `data/data_example.txt`: Example data file (placeholder).
- `progress/01_proposal.md`: Original project proposal.
- `requirements.txt`: Python dependencies.

## Ethical Considerations

This work complies with NCDB's data use restrictions, emphasizing de-identification and refraining from making clinical recommendations.

## License

[Add license information if applicable]


