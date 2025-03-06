# data-challenge-CdF
**Selected Challenge** : Overall Survival Prediction for patients diagnosed with Myeloid Leukemia by QRT

1. Feature Engineering
   - Ratios (interactions) of the different cell counts in the blood stream
   - Cytogenetic data : [1st approach] construct a one-hot encoding of the risk level of the data --> categorical data
        - next up : implement it as a numerical data, thresholds with percentage of risk
   - Next : work on the molecular data
        - preprocess the molecular data
        - train a model (en //?) on this data
        - Test the COX model on those "upgraded" data
2. Test a Deep Learning Survival model
   
