## Credit-Card-Application-Fraud-Analytics

Notice: For security purpose, all files are stored under master branch.


### Project Goal:

This project explores a synthetic dataset of 1,000,000 credit card and phone number applications, and builds a real-time supervised model based on the Personal Identity Information (PII) in those applications to help companies identify possible application frauds in real time.


### Project Overview:

This project broke up model building into six steps, strictly following the steps of data engineering and machine learning. The details are shown as follows:

- Data exploration: I examined the dataset through identifying each variable, calculating minimum, maximum, percentage of null values for the numeric variables & calculating the number of unique values and the most common field value for the categorical variables. After the data examination, I wrote a Data Quality Report (DQR) for the dataset. 

- Data cleaning: To better prepare the data for model building, I cleaned and organized the data. The first focus was on fixing the data type for the date and zip5 fields. I also fixed frivolous values (values that are actually null but filled with impossible values in dataset) for the ssn, address, dob (date of birth), and homephone fields. Lastly, we did target encoding for the date field. 

- Variable creation: Before the model building and selection, I created as many variables as possible to better capture all possible variables that can be used to build a good predictive model to detect the fraud applications in the future. To achieve this, I linked, grouped and did basic calculation of original fields to create 1883 new features.

- Feature selection: From the various variables created in the previous step, I selected the 30 best performing variables to further build models and make model selections.  For the selection process, we used the KS method to reduce the dimension to 100 variables and then used wrapper–forward selection to select the top 30 best variables for the next step.

- Model building: I tried 6 models: Logistic Regression, Decision Tree, Random Forest, Extreme Gradient Boosting (XGboost), Light Gradient Boosting (LightGBM) and Neural Network to find the best predicting model. For each model, I changed hyperparameters to better fit the dataset and compared their performances to select the best model.

- Results: After testing all models and making comparisons, I chose the best performing model with the highest fraud detection rate (FDR) at 3%. I found that the XGboost model had the best performance.  This algorithm is still used by 90% of the banks across the United States.


### Folder Explaination:

This project is divided into 4 folders and 1 summary report. All implementation codes can be found under folders. Summary report gives detailed brackgrounds of this project, retionales behind the method used and explainations of each step.

(1) Data Exploration Part: (Folder)

- Practice of “Data Exploration” part listed above.
- Csv file is the original dataset.
- Ipynb file is the code used in this step.
- Word file is the results of this step.

(2) Data Cleaning and Create New Variables: (Folder)

- Practice of “Data Cleaning” and "Variable Creation" parts listed above.
- Csv file is the original dataset.
- Ipynb file is the code used in this step.
- Pdf file is the results of this step.

(3) Feature Selection: (Folder)

- Practice of “Freature Selection” part listed above.
- Csv file used in this step can be acquired from previous step. (not provide here because of the size limitation, you can get this file by executing the previous step)
- Ipynb file is the code used in this step.
- Xlsx file is the result of this step. (30 variables used for building models)

(4) Fit Model & Performance Table & Graph: (Folder)

- Practice of “Model Building” and "Results" (model building and verifying) parts listed above.
- Csv file is the dataset used in this step. (Results of last step)
- Ipython “build models” fits several models and make best choice.
- Ipython "draw a graph" verify best model through train, test and OOT datasets.

(5) Credit Card Application Fraud Report: (Report)

- Summary Report of all steps listed above.
