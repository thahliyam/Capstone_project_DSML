# Capstone_project_DSML
Data Story
The dataset used in this project is the Online Shoppers Purchasing Intention Dataset, originally published on the UCI Machine Learning Repository.

The data consists of 12,330 records and 18 features, including both numeric and categorical variables that describe user behavior during each session.

Each row in the dataset represents a user session, with features such as the number of pages visited in different sections (Administrative, Informational, ProductRelated), the duration spent on each, bounce and exit rates, traffic source, month of the visit, visitor type, and whether the session occurred on a weekend. The target variable, Revenue, is a binary indicator of whether the session resulted in a purchase.
This capstone project aims to understand and predict user behavior on an e-commerce platform—specifically, whether a visitor will generate revenue. The dataset contains various features such as the duration spent on different types of pages, bounce rates, exit rates, month of visit, traffic types, and other behavioral indicators.

After loading and exploring the dataset, some important cleaning steps were performed. For example, columns like Revenue and Weekend were originally not in numeric format and were converted to integers for better analysis and model compatibility. The dataset was then analyzed to identify categorical and numerical features so that appropriate preprocessing could be applied to each.

Outliers in the numerical columns were handled using quantile-based capping methods. Two different strategies were tested: one based on the 0.01 to 0.99 range and another on the 0.05 to 0.95 range. Skewness was calculated after each transformation, and it was observed that capping at the 0.05 and 0.95 quantiles resulted in a more balanced distribution across most variables. This version of the dataset was selected for further modeling.

Feature preprocessing included scaling the numerical columns and one-hot encoding the categorical variables. These transformations were incorporated into a pipeline using ColumnTransformer and Pipeline from scikit-learn, ensuring a clean and reproducible workflow.

Several classification models were built and tested, such as Logistic Regression, Decision Tree, Random Forest. To optimize performance, hyperparameter tuning was done using techniques like  RandomizedSearchCV. This helped in selecting the best set of parameters for each model, enhancing accuracy and other evaluation metrics.

In the end, model performance was assessed using metrics like accuracy, precision, recall, F1-score, and ROC-AUC. Based on these results, the best-performing model was selected , offering reliable predictions for whether a user will result in a purchase. The project successfully demonstrates how proper preprocessing, feature engineering, and model tuning can improve predictive performance and support data-driven decision-making in e-commerce analytics.
