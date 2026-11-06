Mammographic Mass Classification: Preliminary Model Comparison



A preliminary comparison of supervised ML algorithms for predicting whether a mammographic mass is benign or malignant. The aim was breadth: apply the same data preparation and the same validation to several model families and see how they compare with default settings. It is not an in-depth study of any single model.



For a deeper treatment of a related problem (decision tree pruning, resampling, hyperparameters tuning, recall-focused evaluation), see Classification Predictive Model for Breast Cancer.



Data



UCI Mammographic Mass dataset (https://archive.ics.uci.edu/dataset/161/mammographic+mass): 961 masses, five features (BI-RADS assessment, Age, Shape, Margin, Density) and a binary target, Severity (benign = 0, malignant = 1). Class balance is mild (about 54% benign, 46% malignant), so no resampling was used.



Approach:

* Missing values. 131 of 961 rows (\~14%) have at least one missing value. Rows with missing values have a different malignancy rate (32% vs 49%, chi-square p = 0.0006), so dropping them would bias the sample. Values were imputed instead.
* Imputation without leakage. The data was split (80/20, stratified) before any fitting. A KNNImputer (on standardised features) was fitted on the training set only and applied to the test set, then values were returned to original units and categorical codes rounded.
* Models: Decision tree, random forest, SVM (linear, RBF, sigmoid, polynomial kernels), KNN, Naive Bayes, logistic regression, and a small neural network. Scaling was placed inside pipelines for the models that need it.
* Evaluation. 10-fold cross-validation on the training set, then a single score on the held-out test set.





**---**

The linear SVM, logistic regression, KNN and neural network all exceed 80% test accuracy. On a test set of 193 rows these differences are within the noise expected, so no model is clearly better.

