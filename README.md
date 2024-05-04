# heart-disease-prediction

Heart disease prediction using python,streamlit

Choose a dataset for either a regression or classification problem.

Create Normalized Database (30pts)

Create a normalized database from the raw data file(s).

Do not use Pandas for data loading.

You can utilize the CSV module.

Leave empty values as None/NULL.

The data can be loaded into SQLite3 or any other online relational database service.

Data Preprocessing (20pts)

Write an SQL statement to fetch data from the database into a Pandas DataFrame. MUST USE JOINS. (3pts)

Perform train/test split before inspecting the data. Stratification may be necessary. Make note if data is imbalanced.

Limit EDA to the train data only.

Utilize https://docs.profiling.ydata.ai/latest/ for analysis.

Point breakdown:

Categorize data into categorical and numerical value (3pts).

Identify null and missing values in the data and make note of them (3pts). Also ensure that data columns have the correction data type.

Plots (4pts):
Utilize Seaborn to plot the feature correlation heatmap with correlation values displayed.

Display violin plots to demonstrate the correlation between the target value and categorical features.

Extract meaningful insights from the analysis of categorical and numerical correlation heatmaps.

Examine the distribution of each attribute/feature and derive insightful conclusions from them (3pts).

Develop a class-based preprocessor (4pts):

Address null and missing values and explain the strategy for handling them.

Manage non-normal distributions and detail the strategy for addressing them if necessary.

Implement one-hot encoding for categorical values if required.

Scale the data.

Model Training and Optimization (25 pts)

Register all experiments and models in MLFlow on Dagshub.

Create pipeline with preprocessor and other data manipulation and models.

Select the simplest model and register its metric on the test data, denoting this as the baseline model. (5pts)

For Regression:

mean_absolute_error

mean_squared_error

root_mean_squared_error

For Classification:

accuracy_score

balanced_accuracy_score

f1_score

precision_score

recall_score

roc_auc_score

confusion_matrix

Choose a handful of models or use https://github.com/nityansuman/lazypredict-nightly to figure which which one to select.

Select the top 3 models and register their baseline scores in MLFlow. (5pts)

Perform hyperparameter tuning on the top 3 models and record the scores in MLFlow. (5pts)

Consider feature selection (dropping features) and feature engineering (creating features) at this stage: (5pts)

Drop features based on feature_importance provided by most models. Run experiments with a limited number of features and register them in MLFlow.

Generate new features by combining existing ones or utilizing PCA. Run experiments and record them in MLFlow.

Aim for 10+ experiments. Failure to meet this threshold will result in point deduction. (5pts)

Ensure that your presentation clearly illustrates the improvements made from the baseline model. Use MLFlow to create charts to demonstrate the improvement.

Model Deployment (15pts)

Choose the best model and create a Docker image for deployment on Digital Ocean or alternative services.

For image creation, you can utilize MLFlow or create a Flask API. Note: Due to a bug in MLFlow, you must register the best model locally to create the ML Docker image by downgrading the Python version to 3.12.2.

Streamlit app (10pts)

Develop a Streamlit app that interfaces with your deployed model.

Deploy the Streamlit app on the cloud.

Share the app URL in the Google spreadsheet for verification during the presentation.

Ensure your grader can verify your Streamlit app during the presentation.

Miscellaneous

You will be graded on the process and not on the model performance.

You can use Google Colab

For presentation, use Jupyter Notebook or Google Colab

Some Data sources:

https://thecleverprogrammer.com/2020/11/15/machine-learning-projects/

https://github.com/fivethirtyeight/data

https://github.com/awesomedata/awesome-public-datasets

python --version
Python 3.11.5