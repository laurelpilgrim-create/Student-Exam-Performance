Why I Conducted This Research

After spending several years as a mathematics teacher, I became interested in understanding which factors most strongly influence student success. Rather than relying solely on classroom observations, I wanted to explore the question using machine learning techniques and real-world educational data. This project was conducted independently as an opportunity to apply data science methods to an area that has long been of personal and professional interest.
Student Exam Performance Prediction Using Machine Learning

Overview

This project is an independent machine learning research study exploring the factors that influence student academic performance. Motivated by a personal interest in understanding how academic, family, and lifestyle factors contribute to student success, I developed predictive models to estimate student exam scores using real-world educational data.

The study follows a complete data science workflow, including data acquisition, preprocessing, exploratory data analysis (EDA), feature engineering, predictive modeling, hyperparameter tuning, cross-validation, and residual analysis. Two regression algorithms—Linear Regression and Random Forest Regression—were evaluated to determine which model best predicts student exam performance while identifying the variables with the greatest impact on student achievement.
Dataset

Source: Kaggle – Student Performance Dataset by Ayesha Siddiqa

https://www.kaggle.com/datasets/ayeshasiddiqa123/student-perfirmance

The dataset contains information on 6,607 students and includes academic, demographic, family, and lifestyle variables that may influence student achievement.

Target Variable
Exam_Score
Predictor Variables

The dataset includes features such as:

Hours Studied
Attendance
Previous Scores
Tutoring Sessions
Sleep Hours
Physical Activity
Internet Access
Teacher Quality
School Type
Family Income
Distance from Home
Motivation Level
Parental Involvement
Parental Education Level
Peer Influence
Learning Disabilities
Access to Educational Resources
Extracurricular Activities
and several additional student characteristics.
Project Objectives

The objectives of this project were to:

Predict student exam scores using supervised machine learning.
Compare Linear Regression and Random Forest Regression models.
Identify the most influential factors affecting student performance.
Evaluate model accuracy using multiple regression metrics.
Demonstrate a complete end-to-end machine learning workflow.
Data Preparation

Before modeling, the data underwent several preprocessing steps:

Downloaded the dataset directly from Kaggle using KaggleHub.
Examined the dataset for missing values.
Replaced missing categorical values using mode imputation.
Converted categorical variables into numerical values using Label Encoding.
Split the dataset into 80% training data and 20% testing data.
Verified the data before model training.
Exploratory Data Analysis

Several visualizations were created to better understand the relationships within the data, including:

Distribution of exam scores
Hours Studied vs. Exam Score
Internet Access vs. Exam Score
Parental Involvement vs. Exam Score
Feature importance rankings
Cross-validation comparison
Residual plots for both models

These visualizations helped identify trends, relationships, and potential predictors before developing machine learning models.

Machine Learning Models
Linear Regression
A Linear Regression model was developed as the baseline predictive model. This model estimates exam scores by assuming a linear relationship between the predictor variables and the target variable.

Random Forest Regression
A Random Forest Regressor was developed to capture more complex, nonlinear relationships within the data.

The model was further optimized using GridSearchCV by tuning:

Number of trees
Maximum tree depth
Minimum samples required to split nodes
Minimum samples required at leaf nodes
Model Performance

Both models were evaluated using four standard regression metrics.

Model	MAE	MSE	RMSE	R²
Linear Regression	1.02	4.40	2.10	0.69
Tuned Random Forest Regressor	1.09	4.54	2.13	0.68
Interpretation

The Linear Regression model produced the strongest overall performance on the testing dataset.

Average prediction error was approximately 1 exam point.
The model explained approximately 69% of the variation in student exam scores.
Although the Random Forest model was optimized through hyperparameter tuning, its performance was nearly identical but slightly lower than Linear Regression.

The results suggest that the relationships within this dataset are largely linear, allowing the simpler Linear Regression model to perform slightly better than the more complex Random Forest model.

Cross-Validation

To evaluate how well each model generalized to unseen data, 5-fold cross-validation was performed.
Cross-validation demonstrated that both models produced consistent performance across multiple data splits, indicating reliable predictive capability and reducing the likelihood of overfitting.

Residual Analysis
Residual plots were used to evaluate whether each model satisfied the assumptions of regression and to identify potential modeling issues.

Ideal Residual Plot
An ideal residual plot displays a random scatter of points around the horizontal line at zero. This indicates that the model is effectively capturing the underlying relationships in the data and that prediction errors are randomly distributed (homoscedasticity).

Patterns Evaluated
During residual analysis, the following patterns were considered:

Funnel Shape (Heteroscedasticity): A widening or narrowing spread of residuals suggests that prediction errors are not constant across all predicted values.
Curvature or Nonlinear Patterns: A curved trend indicates that the model may be missing nonlinear relationships and that additional feature engineering or more complex algorithms may improve predictions.
Clusters: Distinct clusters of residuals may indicate missing explanatory variables or uncaptured categorical effects within the dataset.

Residual analysis provides valuable insight into the strengths and limitations of predictive models beyond traditional performance metrics and helps determine whether important modeling assumptions have been violated.

Key Findings
The analysis identified several important factors associated with student success:
Hours Studied was one of the strongest predictors of exam performance.
Previous academic performance also had a significant influence on final exam scores.
Greater parental involvement generally corresponded with higher student achievement.
Access to educational resources and internet availability showed positive relationships with academic performance.
Multiple academic, family, and lifestyle variables contributed to student success rather than any single factor.
Linear Regression slightly outperformed the tuned Random Forest model across every evaluation metric.

Overall, the findings suggest that student achievement is influenced by a combination of study habits, academic history, family support, and educational resources.

Technologies Used
Python
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn
KaggleHub
Repository Structure

Future Improvements

Potential future enhancements include:
Compare additional machine learning algorithms such as XGBoost, LightGBM, and CatBoost.
Apply One-Hot Encoding instead of Label Encoding for nominal categorical variables.
Perform feature selection to reduce model complexity.
Develop an interactive dashboard using Tableau or Power BI.
Deploy the final model using Streamlit or Flask.

Conclusion

This project demonstrates an end-to-end machine learning workflow for educational data analysis. Beginning with raw student data, the project progresses through preprocessing, visualization, predictive modeling, hyperparameter tuning, cross-validation, and residual analysis to evaluate model performance.
The final results indicate that Linear Regression achieved the highest predictive accuracy, explaining approximately 69% of the variation in student exam scores while maintaining an average prediction error of only about one point. The analysis also highlights the importance of study habits, previous academic performance, parental involvement, and access to educational resources in predicting student achievement.

This project demonstrates practical experience with data preprocessing, exploratory data analysis, regression modeling, model evaluation, hyperparameter optimization, and statistical interpretation using Python and Scikit-learn.
