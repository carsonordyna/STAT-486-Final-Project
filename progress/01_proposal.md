---
format:
  html:
    anchor-sections: false
---

# Initial Proposal

## Project Idea 1: Survival Prediction + Patient Subtype Clustering {#Project_1}

### Supervised Component:
Build a survival regression model predicting overall survival or 5‑year survival probability using:

- Patient demographics
- Tumor stage + histology
- Treatment variables (surgery, chemo, radiation)
- Comorbidity scores


Potential models to use:

- Cox proportional hazards model
- Random survival forests
- DeepSurv

### Unsupervised Component:
Use clustering to discover lung cancer subtypes that share clinical characteristics and survival outcomes.

Potential clustering features:

- Tumor size
- Stage group
- Nodal involvement
- Treatment modality combinations
- Age + insurance status + facility type


Potential methods:

- k‑means (after feature scaling)
- Gaussian Mixture Models
- Hierarchical clustering

### Research Question:
- Do unsupervised clusters of lung cancer patients correspond to significantly different survival predictions? Can clusters help clinicians understand patient subtypes the model predicts worst for? This is a classic “precision oncology” style problem.



## Project Idea 2: Treatment Recommendation Engine + Treatment Effect Classification

### Supervised Component:
Train a classification model predicting which primary treatment a patient will receive:

- Surgery
- Chemotherapy
- Radiation
- Immunotherapy combinations
- Palliative vs. curative


Potential predictors:

- Tumor stage
- Comorbidities
- Facility type
- Age
- Histology
- Insurance

### Unupervised Component:
Build a treatment recommender that suggests treatments that worked best for “similar patients”

Potential approaches:

- k‑NN similarity model
- Matrix factorization using patient–treatment–outcome matrix
- Content‑based recommendations using tumor + demographic features

### Research Question:
- Can a recommender model identify effective treatments for new patients by learning from outcomes of similar historical patients? This blends precision medicine + ML interpretability.



## How did AI influence the plan and direction for my project?

AI influenced my idea selection by presenting several project concepts that clearly connected National Cancer Database (NCDB) lung cancer data with multiple different machine learning approaches/models that I could use. Based on my understanding of and comfortability with these methods, I was able compare their feasibility and scope. The AI tool also highlighted the strengths of each option. When I told the AI tool the idea that I liked the most, it helped me refine my research question and the candidate target variable(s) for supervised analysis. AI proposed how I could combine supervised/unsupervised methods (survival modeling and clustering, respectively) to answer my research questions and the practical implementation path I should pursue.



## Excerpt of AI Exchange
**Me**: I am working on a senior-level machine learning project. I am interested in a lung cancer database from the National Cancer Database (NCDB). I need a project idea that combines both supervised learning (classification or regression) and another ML approach, such as clustering, anomaly detection, or recommender systems. Can you suggest feasible project ideas?

**AI**: Here are feasible, senior‑level ML project ideas using NCDB lung cancer data that combine supervised learning and another ML approach (clustering, anomaly detection, or recommendation). Each idea is designed to be realistic, clinically meaningful, and implementable with typical NCDB fields (demographics, tumor characteristics, staging, treatments, survival, facility type, etc.). . . . Do want a recommendation on which one fits your skill level and timeframe? Tell me: 

- your preferred ML area (deep learning? classical ML?)
- time available
- whether you have survival data access
- whether you prefer clinical or methodological contributions

I can help you select one, build an outline, and even draft your project proposal.

**Me**: I would like to pursue [Idea 1](#Project_1). Can you draft a paragraph or two that addresses the following?

- Final research question
- Candidate target variable for supervised analysis
- Dataset choice and backup dataset
- Feasibility (time, compute, scope)
- Ethical/legal considerations
- Planned additional ML methods

**AI**: Here is a polished, proposal-ready write‑up for [Idea 1](#Project_1), structured around all your required elements: . . .



## Refined Proposal
The final research question for this project is: Can unsupervised clustering of lung cancer patients reveal subgroups that meaningfully explain variation in supervised survival predictions, and does incorporating clustering improve model performance? The supervised component will target overall survival or a derived binary outcome such as 5‑year survival, both of which should be well‑supported by the National Cancer Database (NCDB) lung cancer dataset. The NCDB dataset will serve as the primary dataset due to (hopefully) its large sample size and clinical detail, while the publicly accessible SEER lung cancer dataset will function as a backup or external validation source if needed. This project is feasible because both clustering (e.g. k‑means, GMMs) and survival modeling (e.g. Cox models, random survival forests) are computationally efficient and manageable on standard hardware. Ethically, the work will comply with NCDB’s data use restrictions, emphasizing de‑identification and refraining from making clinical recommendations. Additional planned machine learning methods include unsupervised clustering to identify patient subtypes, followed by integration of cluster labels into survival models to test whether these groups improve predictive accuracy or uncover clinically relevant heterogeneity.