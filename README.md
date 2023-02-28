## Machine Learning tool to predict the quality of freshwater
The project is based on one of the themes Intel® oneAPI Hackathon for Open Innovation

### Machine Learning Challenge Track: Predict the quality of freshwater

#### Problem:
Freshwater is one of our most vital and scarce natural resources, making up just 3% of the earth’s total water volume. It touches nearly every aspect of our daily lives, from drinking, swimming, and bathing to generating food, electricity, and the products we use every day. Access to a safe and sanitary water supply is essential not only to human life, but also to the survival of surrounding ecosystems that are experiencing the effects of droughts, pollution, and rising temperatures.

#### Expected Solution:
In this track of the hackathon, we apply Machine learning concepts and leverage oneAPI capabilities to help global water security and environmental sustainability efforts by predicting whether freshwater is safe to drink and use for the ecosystems that rely on it


#### Objective
The objective of this project is;

- To Create a prediction model which can determine whether the target source is a freshwater or not.


### Data Pre-Processing:

Usage of OneAPI library  helped accelerate the time of data load and optimisation.

The input data had 'Target' as the dependent and the below listed independent variables.

a. Continuous Attributes: pH, Iron, Nitrate,Chloride, Lead, Zinc, Color, Turbidity, Fluoride, Copper, Odor, Sulfate, Conductivity, Chlorine, Manganese, Total Dissolved Solids, Source,Water Temperature, Air Temperature

b. Categorical Attribute: Day,Time of Day, Month, Source, Color

The attributes 'Day', 'Month' and 'Time of Day' were not considered in order to avoid over-fitting.

All The categorical attributes are converted to continuous attributes by using the 'Factorization' Method.
The Attributes not contributing to the result like 'Day' , 'Month' , 'Time Of Day' are dropped.

## Selecting Machine Learning Models
Five ML Models were run on the dataset - Logistic Regression , Gradient Boost , XG Boost , Light GBM , Cat Boost.
Boosting algorithm fared better, and within them LightGBM fared the best. The run time was accelerated by using sklearn library of OneAPI tool.

### Optimisation and final model selection
We were able to gain a faster execution time of LightGBM and derive the model to predict the target source (whether it is a freshwater or not)
Final Accuracy : 95.003 % 

### Implementation on Local System
- Copy the data into the folder from this link (https://s3-ap-southeast-1.amazonaws.com/he-public-data/datasetab75fb3.zip). Unzip it
- Run the Freshwater Prediction.ipynb file on your local system using Jupyter or any other Python Interpreter.
- Change the path in the ipynb file from C:\Users\User\Downloads\dataset.csv to the path of file in your system

Execute The Cells One by One to get the results.
