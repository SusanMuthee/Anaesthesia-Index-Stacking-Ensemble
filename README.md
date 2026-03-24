# Anaesthesia-Index-Stacking-Ensemble
Depth of Anaesthesia Index using Stacking Ensemble Learning
Built a new depth of anaesthesia (DoA) index from EEG data using a stacking ensemble — combining Random Forest and Linear Regression base models with a Linear Regression meta-model. Validated against the clinical BIS index on real patient data.

Results
Pearson correlation
0.8922
R² score
0.7829
MSE
89.38
Patients
17 (12 train · 5 test)
Approach
1. EEG feature extraction (7 features x1–x7)
2. Correlation analysis + Random Forest feature importance → selected x4, x7, x5, x1
3. Stacking: RF + LR base models → LR meta-model
4. Evaluated with Pearson, R², MSE, scatter plot, Bland-Altman

Key finding
x4 was the dominant EEG feature (importance score 0.58). Model performs well for BIS 20–80 but shows wider spread above 80 — an area for future improvement.

Tech stack
Python · pandas · scikit-learn · matplotlib · seaborn · scipy
