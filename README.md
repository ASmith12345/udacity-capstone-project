# udacity-capstone-project
In 2023, the drop out rate of undergraduate students is 40%, with 24.% of those dropping out in their first year. People who have dropped out of college are 20% less likely to find a job than those with an undergraduate degree. As well as the negative impact to the student’s of dropping out of College, institutions will face other negative consequences of having a low retention rate. Low student success indicates low institution effectiveness. Consequently, this can have a negative financial impact due to loss of revenue from tuition and other expenses. The brand of the institution will also be negatively affected if they are seen to have low numbers of students graduating.

Institutions may benefit from identifying which students are at risk of dropping out. There are learning resources available to students who may be struggling at university. Glean found that 76% of students using their app reported increased grades as well as increasing confidence and reducing stress, which are all associated with retention rates.

Libraries

The libraries used in visualisations.ipynb are pandas, matplotlib, numpy, plotly and seaborn. The libraries used in optimised-columns-ml-analysis are pandas, plotly, matplotlib, seaborn, numpy and sklearn.

Files

Dataset.csv - raw data from kaggle
Formatted_dataset.csv - output from Format-data.ipynb ready for ml models
Format-data.ipynb - process data ready for machine learning model
Optimised-columns-ml-analysis.ipynb - machine learning models exploring optimised regression model
Visualisations.ipynb - exploratory analysis of the data, primarily using visualisations


In order to decide which metrics to use, I performed a correlation analysis of continuous data. Curricular units were all highly correlated with each other so only “Curricular units 2nd sem (approved)” was kept in the model. I hypothesised that there would be high associations between “Mother’s qualification”, “Father’s qualification”, “Mother’s occupation” and “Father’s qualification” so only included “Mother’s qualification” in the model. There would also be a high association between “International” and Nationality so these were excluded. The values kept in tye model were . “GDP”, “Inflation rate” and “Unemployment rate” all seemed to be evenly distributed between the three retention categories so these were also excluded from the model. The remaining columns to include in the model are “Marital status”, “Course”, “Daytime/evening attendance”, "Mother's occupation", “Educational special needs”, “Debtor”, “Gender”, “Scholarship holder”, “Age at enrollment”, “International”, “Curricular units 2nd sem (approved)” and “Target”.

Before modelling the data, I mapped the numerical values to the true categorical values. These were found in the paper “Predicting Student Dropout and Academic Success”. The dataset included one column incorrectly named which was altered. Where columns with categorical values which were only 1 and 0, they were interpreted to be boolean e.g. Debtor is is_debtor, Gender is is_male. I removed enrolled students as we are investigating what the outcome of the student’s university experience is. An enrolled student could become a graduate or dropout so it was important to remove these as it could reduce the accuracy of the model. The dataset included no nulls and required no cleaning.

In optimised-columns-ml-analysis, i created dummy variables in order to manage the categorical columns. This ensures that only numbers are being fed into the models.

Categorical values - https://www.mdpi.com/2306-5729/7/11/146 
Dataset - https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention/data