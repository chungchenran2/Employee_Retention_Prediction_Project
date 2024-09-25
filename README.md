# Employee Retention Prediction Project

## Overview

The goal of this project was to create a logistic regression, decision tree, random forest, and XGBoost model to predict whether an employee of a multinational vehicle manufacturing corporation will leave the company or not. This project utilized a dataset of HR survey responses provided by a sample of employees. Each row is for a different employee's self-reported information among ten columns. The logistic regression model performed with 84.4% accuracy, 57.5% precision, and 23.1% recall in determining which employees will leave the company. The decision tree model performed with 95.7% accuracy, 82.9% precision, and 93.5% recall in determining which employees will leave the company. The random forest model performed with 98.3% accuracy, 96.6% precision, and 93.2% recall in determining which employees will leave the company. The XGBoost model performed with 98.1% accuracy, 96.8% precision, and 91.7% recall in determining which employees will leave the company. The random forest model was chosen as the champion model with the following performance on the test dataset: 98.4% accuracy, 97.4% precision, and 92.7% recall. Based on the random forest model, the employee's self-reported satisfaction level, the number of projects the employee contributed to, the score of the employee's last performance review, the number of years the employee has been with the company, and the average number of hours the employee worked per month were most influential in determining which employees will leave the company.

## Business Understanding

Currently, there is a high rate of turnover among Salifort employees. (Note: In this context, turnover data includes both employees who choose to quit their job and employees who are let go). Salifort’s senior leadership team is concerned about how many employees are leaving the company. Salifort strives to create a corporate culture that supports employee success and professional development. Further, the high turnover rate is costly in the financial sense. Salifort makes a big investment in recruiting, training, and upskilling its employees.

If Salifort could predict whether an employee will leave the company, and discover the reasons behind their departure, they could better understand the problem and develop a solution.

## Data Understanding

The data came from a survey conducted by HR on a sample of employees. The data consisted of approximately 15k unique employee responses and 10 features. The features included information on employee's self-reported satisfaction level, score of employee's last performance review, number of projects employee contributes to, and so on. The bar chart below shows the breakdown of how many employees who left the company versus employees who stayed with the company that exist in the data set.

![Proportion of left column](https://github.com/chungchenran2/Employee_Retention_Prediction_Project/blob/main/Images/Salifort_left_proportion.png)

During model building, there were four features that were not important for the random forest model, they are department, salary, work_accident, and promotion_last_5years. Taking these four features out would not affect the performance of the random forest model.

## Modeling and Evaluation

A random forest model comprising 200 decision trees was used to determine feature importance in who would leave the company or not. The below plot shows that an employee's satisfaction level, number of projects an employee contributed to, and the employee's last performance score were the Top 3 most important factors in determining an employee who leaves the company from an employee who stays. The overall model performed with 98.4% accuracy, 97.4% precision, and 92.7% recall.

![RF feature importances](https://github.com/chungchenran2/Employee_Retention_Prediction_Project/blob/main/Images/Salifort_RF_tr_drop_feature_importances.png)

## Conclusion

This model can benefit Salifort’s senior leadership team in knowing whether an employee will leave the company and discovering the reasons behind the employee's departure. In light of the champion model’s performance and the dataset the model is based on, the company should regularly conduct similar HR surveys and apply the model on the results to predict the possibility of employee turnover.
