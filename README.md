# Employee-Attrition-Analysis-and-Prediction

Employee attrition means the gradual reduction in the number of employees due to employees leaving. The three main reasons for us to work on this project is as follows : 

**High Business Impact:** Employee attrition costs U.S. companies over $1 trillion annually, significantly affecting productivity, morale, and overall organizational performance
**Organizational Challenges:** Attrition leads to a loss of institutional knowledge, reduced productivity, and high replacement costs, often up to 150% of the employee’s annual salary
**Proactive Solution:** Implementing ML-based early warning systems can help organizations identify at-risk employees and enable targeted retention strategies, reducing turnover and improving employee retention.


**In this project:**

-Conducted exploratory data analysis (EDA) to uncover patterns and trends related to attrition.
-Preprocessed the dataset to handle missing values, encode categorical features, and scale numerical data.
-Applied and evaluated multiple machine learning models to predict attrition.
-Focused on identifying the most influential factors contributing to employee turnover.

The dataset used for the analysis consists of 1,470 entries with 35 features, and it contains no missing or NaN values. 

The HR Employee Attrition dataset was loaded and prepared by dropping four columns based on EDA. Categorical features were encoded using Label Encoding, while the target variable, Attrition, was transformed into binary labels. Min-Max scaling was applied to normalize the feature values within the range of [0, 1]

Multiple classification algorithms were implemented, including Logistic Regression, Decision Tree Classifier, Random Forest Classifier, Gaussian Naive Bayes, and Support Vector Classifier with both RBF and linear kernels. These were our Base Models. Each model was trained on the normalized training dataset, and performance metrics such as precision, recall, F1-score, and accuracy were calculated to compare their effectiveness in predicting employee attrition.

For the advanced models, we implemented a preprocessing pipeline which consisted of the following additional steps:
Removal of columns which did not contribute useful information like Employee Count, EmployeeNumber, Over 18 and Standard Hours
Features with a unique value were also dropped
Synthetic Minority Oversampling Technique (SMOTE) was applied to generate samples of the minority class to tackle the class imbalance

Model 3 with Hybrid XGBoost and Random Forest with Recursive Feature Elimination and Bayesian Optimization gave the best performace with 95% accuracy in predicting employee attrition and thus was the best out of the advanced mdoels.
