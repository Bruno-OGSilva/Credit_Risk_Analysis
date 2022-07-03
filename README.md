# Credit_Risk_Analysis


## CHALLENGE OVERVIEW
---
The purpose of this project is to apply supervised machine learning algorithms to determine credit card risk. Will be deployed various ML models to reduce bias and resample datasets to determine the best methodology or algorithm to accurately predict credit-card risk. The models’ performance will be evaluated and recommendations will be made on each of them.

## FEATURES AND DATA SOURCES
- Data Source: `LoanStats_2019Q1.csv`
- Programming Files: [credit_risk_resampling.ipynb](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/credit_risk_resampling.ipynb), [credit_risk_ensemble.ipynb](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/credit_risk_ensemble.ipynb)
-  Software: `imbalanced-learn`, `Python`, `skikit-learn`, `Jupyter Notebook`

## Challenge Deliverables
- Deliverable 1: Use Resampling Models to Predict Credit Risk
- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
- Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)


## Results
---

1. Naive Random Oversampling

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/1%20-%20Naive%20Random%20Oversampling.png)

- The balanced accuracy score is 65%.
- The high_risk precision is about 1% only with 63% sensitivity, making a F1 of 2% only.
- Driven by high number of the low_risk population, the precision is almost 100% with a sensitivity of 66%.

2. SMOTE Oversampling

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/2%20-%20SMOTE%20Oversampling.png)

- The balanced accuracy score is 62%.
- The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
- Because of the high number of the low_risk population, its precision is almost 100% with a sensitivity of 63%.

3. ClusterCentroids Undersampling

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/3%20-%20ClusterCentroids%20Undersampling.png)
- The balanced accuracy score is down to about 51%.
- The high_risk precision is still 1% only with 59% sensitivity and a F1 of 1%.
- Because of the high number of false positives, the low_risk sensitivity is only 43%.

4. SMOTEENN Combination Sampling

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/4%20-%20SMOTEENN%20Combination%20Sampling.png)

- The balanced accuracy score is about 62%.
- The high_risk precision is still 1%, with 70% sensitivity making a F1 of 2%.
- Because of the high number of false positives, the low_risk sensitivity is 54%.

5. BalancedRandomForestClassifer

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/5%20-%20BalancedRandomForestClassifer.png)

- The balanced accuracy score improved to about 79%.
- The high_risk precision is at 4%, with 67% sensitivity presenting a F1 of only 7%.
- Driven by a lower number of false positives, the low_risk sensitivity is 91% with 100% presicion.

6. EasyEnsembleClassifer

![](https://github.com/Bruno-OGSilva/Credit_Risk_Analysis/blob/1831d2ddaef8daa3381a84843cb390d4f6dba726/Assets/6%20-%20EasyEnsembleClassifer.png)
- The balanced accuracy is 93%.
- The high_risk precision is at 7% with 91% sensitivity an a F1 of 14%.
- Due to a lower number of false positives, the low_risk sensitivity is 94% with 100% presicion.

## Summary
---

We can identify from the data frames that all models presented a weak precision rate in identifying if credit risk is high. But in this case, it is better to have a high sensitivity model than a high precision one, because this way it will minimize false negatives. With that said, the EasyEnsembleClassifier model shows a recall of 91% so it detects almost all high-risk credit. At the same time, with a low precision rate of 7%, the bank will have many false-positive which will negatively impact the company’s commercial performance, and consequently its capability of generating revenue. In this scenario, I would recommend the company not use any of the models tested.
