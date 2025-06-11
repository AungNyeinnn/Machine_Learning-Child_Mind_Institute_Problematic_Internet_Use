
The goal of this competition is to develop a predictive model that analyzes children's physical activity and fitness data to identify early signs of problematic internet use. Identifying these patterns can help trigger interventions to encourage healthier digital habits.

The data included two parts: tabular data containing participant demographic info and measurements from a variety of instruments, and parquet files containing the accelerometer (actigraphy) series. The solutions I used to the challenges in this competition are as followed 

Too many missing values-> Drop features with more than 50% missing values, and used KNN imputation to model and fill in the missing values

Too many features given-> Drop any feature that has very low correlation (less than ±0.1) with target variable, and applied PCA for dimensionality reduction

Parquet files from Actigraphy-> Performed Autoencoders to extract features from the Parquet Files and merged with tabular data

Finally, stacking four tree based models into a logistic regression model yielded accuracy score of 0.71 on training set and 0.61 on test set which is very good performance considering the amount of missing values and labels. 
 
This competition was organized by Child Mind Institute in partnetship with Kaggle, and is sponsored by Dell Technologies and NVIDIA. 
