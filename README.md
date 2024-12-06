# Azubi_Assignment
Azubi Assessment Exams
Achieving Predictive Modeling for Client Subscription

In this article, we will walk through the essential processes that were followed to build a predictive model aimed at forecasting whether a client would subscribe to a bank's term deposit product. These steps include data analysis, feature engineering, model building, and evaluation. 
1. Understanding the Problem
The goal of the task was to predict if a client would subscribe to a bank's term deposit product based on various features collected during direct marketing campaigns. The dataset provided contains information about previous clients, such as their job type, marital status, education, and previous contact information with the bank. The target variable (what we want to predict) is whether a client subscribed to the term deposit, labeled as yes or no.

2. Exploratory Data Analysis (EDA)
Before jumping into building a model, we needed to understand the data thoroughly. This process is called Exploratory Data Analysis (EDA). Here's how we approached it:
A. Looking at the Data
First, we loaded the dataset and examined its structure:
•	We checked the number of rows and columns to understand the size of the dataset.
•	We looked at the first few rows to get an idea of what data we were working with.
B. Summary Statistics
Next, we reviewed some key statistics:
•	We calculated summary statistics for numerical columns like age, balance, and duration of contact.
•	We also looked at the categorical features (like job type and education) to understand their unique values and distribution.
C. Checking for Missing Values
Data often has missing values, and it’s important to identify them early on. We used simple techniques to check for any columns with missing data, which might need to be handled later (either by removing or filling in the missing values).


D. Target Variable Distribution
The next step was to check the balance of our target variable (y), which indicates whether a client subscribed to the term deposit:
•	We used a count plot to visually assess how many clients subscribed (yes) versus those who did not (no). This showed whether the data was balanced or imbalanced.
E. Feature Correlations
We then looked at the relationships between different numerical features:
•	We used a correlation heatmap to see how features like age, balance, and previous contact duration are related to one another.
•	This helped us understand which features might be more influential in predicting client subscriptions.
F. Feature Distributions and Outliers
To see how individual features were spread out, we created histograms for each numerical feature and checked for outliers using box plots. Outliers are extreme values that could skew the model’s performance, so we needed to identify and decide whether to keep or remove them.
G. Categorical Feature Analysis
For categorical features like job, education, and marital status, we used count plots to examine how these features are distributed across the target classes (yes or no). This helped us identify patterns that could influence a client's likelihood of subscribing.

3. Feature Engineering
Feature engineering is the process of preparing and improving the features (data columns) for the machine learning model. Here’s what we did:
•	Encoding Categorical Data: Many machine learning algorithms work best with numerical data. Therefore, we used techniques like Label Encoding to convert categorical variables (such as job or education) into numeric representations.
•	Handling Imbalanced Classes: If the dataset has many more no subscriptions than yes ones (class imbalance), it can lead to poor predictions. We addressed this by using SMOTE (Synthetic Minority Over-sampling Technique), which generates synthetic data points for the minority class (those who subscribed) to balance the data.

4. Building the Predictive Model
After preparing the data, the next step was to build a predictive model. Here’s how we did it:
•	We split the data into training and testing sets. The training data is used to teach the model, and the testing data is used to evaluate its performance.
•	We selected a machine learning algorithm to build the model. In this case, we used a Random Forest classifier, which is great for handling both numerical and categorical data and can give us insight into which features are most important.

5. Evaluating the Model
Once the model was trained, we needed to evaluate its performance:
•	We used different metrics like accuracy, precision, recall, and F1-score to check how well the model performed.
o	Accuracy tells us how many predictions the model got right.
o	Precision measures how many of the predicted yes subscriptions were actually correct.
o	Recall shows how many actual yes subscriptions the model managed to identify.
o	F1-score is the balance between precision and recall, giving us a single metric to evaluate performance.
•	We also checked if the dataset was imbalanced (more no than yes subscriptions). If it was, we could use techniques like oversampling or adjusting class weights to improve the model’s ability to predict the minority class (yes).

6. Conclusion: Insights and Findings
After performing the EDA and building the model, we gained several important insights:
•	Key Features: Some features like the client's job, marital status, and previous contact with the bank had a strong impact on predicting whether they would subscribe to the term deposit.
•	Class Imbalance: There was an imbalance in the target variable, with more clients not subscribing. We addressed this with SMOTE to improve the model’s performance.
•	Model Performance: The Logistic Regression model performed well, with high accuracy and F1 scores, especially after balancing the classes.
These insights can be used by the marketing team to target specific groups of clients who are more likely to subscribe, improving the effectiveness of future campaigns.

Final Thoughts
In this article, we discussed the key steps involved in building a predictive model for client subscription to a term deposit product. By performing a thorough Exploratory Data Analysis (EDA), handling missing values, balancing classes, and applying machine learning techniques, we were able to predict subscription outcomes effectively. The results of this analysis can help the bank refine its marketing strategies, ensuring that resources are better targeted toward the most promising clients.

