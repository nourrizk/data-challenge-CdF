# data-challenge-CdF
**Selected Challenge** : Overall Survival Prediction for patients diagnosed with Myeloid Leukemia by QRT

1. Feature Engineering
   - Ratios (interactions) of the different cell counts (features collected from the clinical data csv) in the blood stream
   - Cytogenetic data : [1st approach] construct a one-hot encoding of the risk level of the data (High/Low) --> categorical data
        - **next up :** implement it as a numerical data (or categorical with more bins) based on thresholds with percentage of risk
   - Molecular data :
        - [1st approach] : preprocess the molecular data and train COX and RSF model on all features
        - **next up :** work on feature selection to reduce correlation and improve the model ipcw c-index
        - **next up :** train a model (en //?) on this data avant de feed the data to the COX or RSF model?
2. Trained models :
     - COX survival model with regularization [on the platform : 0.72]
     - RSF model [on the platform : 0.745]
          - try adding regularizaiton
     - combination of the Z_norm predictions of the COX and RSF model [on the platform : 0.73 et truc] ---- the COX model is pulling down the prediction? but it might be mitigating the overfitting
     - training a meta-model (on the results of OCX and RSF? (need to review the implementation/ choice of input features))
          - tried a Logistic Regression
          - **in progress :** trying an XGBoost ----- promissing : need to refine before uploading on the platform
     - **next up :** grid search for all models + refine the feature engineering
     - **in progress :** implementing a Deep Learning Survival model
   
