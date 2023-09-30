# Bank_Repayment_Prediction_With_Deep_Learning_Model
Deploying a Deep learning model to predict whether a New customer will be able to repay the loan or not

Project Title: Loan Repayment Prediction with Deep Learning

Summary:
The goal of this project is to build a deep learning model that predicts whether a borrower will repay a loan or not, using historical data from Lending Club. The dataset includes various features related to loans and borrowers, and the target variable is whether the loan was fully paid or charged off.

Project Steps:

Data Exploration and Preprocessing:

Import necessary libraries: pandas, numpy, seaborn, and matplotlib.
Load the dataset containing information about the dataset features (lending_club_info.csv) into a DataFrame called data_info.
Define a function columndes to display descriptions of specific columns.
Use columndes to display the description of the "mort_acc" column.
Load the main loan dataset (lending_club_loan_two.csv) into a DataFrame called df.
Explore the dataset, including visualizations like a countplot of loan statuses and a heatmap of feature correlations.
Data Preprocessing:

Prepare the data for modeling by handling missing values and categorical variables.
Drop unnecessary columns like "emp_title" and "title" due to high cardinality.
Handle missing values in the "mort_acc" column by filling them with the mean value based on the "total_acc" column.
Convert the "term" column from a string to an integer.
Encode categorical variables using one-hot encoding.
Modify the "home_ownership" column to group categories "NONE" and "ANY" into "OTHER."
Extract the zip code from the "address" column and use one-hot encoding for zip codes.
Drop the "issue_d" column as it is not needed for prediction.
Transform the "earliest_cr_line" column to extract the year.
Data Splitting and Scaling:

Split the data into features (X) and the target variable (y).
Normalize the features using Min-Max scaling.
Split the data into training and testing sets.
Deep Learning Model:

Create a sequential neural network model using TensorFlow and Keras.
Add multiple hidden layers with dropout regularization to prevent overfitting.
Use a sigmoid activation function in the output layer for binary classification.
Compile the model with binary cross-entropy loss and the Adam optimizer.
Train the model using the training data, specifying the number of epochs and batch size.
Model Evaluation:

Visualize the training and validation loss over epochs.
Make predictions using the test data.
Define a threshold (0.5) to classify predictions.
Evaluate the model using classification reports and confusion matrices.
Conclusion:
The deep learning model was built and trained to predict loan repayment based on Lending Club data. The model's performance can be assessed using metrics such as precision, recall, F1-score, and accuracy. Further refinements and hyperparameter tuning can be performed to optimize the model's performance. This project provides a solid foundation for predicting loan repayment using deep learning techniques.
