This project involves predicting which passengers were transported to an alternate dimension during the collision of the Spaceship Titanic with a spacetime anomaly. Here is a detailed step-by-step explanation of the process, from data preprocessing to model training, evaluation, and submission.

Step 1: Load and Preprocess Data
Loading Data:

We load the training and test datasets from CSV files using pandas.
Handling Missing Values:

For numerical columns, missing values are filled with the median.
For categorical columns, missing values are filled with the most frequent value (mode).
Feature Engineering:

Total Spend: Calculate the total amount spent by each passenger across all amenities.
Group Size: Extract group size from the PassengerId.
Is Alone: Create a feature indicating whether a passenger is traveling alone.
Deck, Num, Side: Split the Cabin column into three separate features.
Step 2: Model Training and Tuning
Hyperparameter Tuning for Random Forest:

Use RandomizedSearchCV to find the best hyperparameters for the Random Forest model.
Stacking and Blending Models:

Combine predictions from multiple models (Random Forest and XGBoost) using a stacking classifier to improve performance.
Step 3: Addressing Class Imbalance
SMOTE (Synthetic Minority Over-sampling Technique):
Apply SMOTE to balance the class distribution in the training data.
Step 4: Neural Networks
Neural Network Model:
Build and train a neural network using TensorFlow and Keras for potentially better performance.
Step 5: Make Predictions and Prepare Submission
Predict on Test Set:

Use the trained stacking model to make predictions on the test set.
Prepare Submission File:

Format the predictions as required by Kaggle and save them to a CSV file.
