# ANN_WINE_QUALITY
This project uses a Random Forest Classifier to predict the quality of red wine based on chemical attributes. The model is trained on the UCI Wine Quality dataset and provides detailed predictions along with insights into the importance of each feature.

Features
Predict wine quality based on 11 chemical properties.
Detailed insights about the features influencing the wine's quality.
Model evaluation includes accuracy, F1 score, recall, and a classification report.
Custom input allows users to provide their own data for wine quality prediction.
Dataset
The dataset used for training the model is the UCI Wine Quality Dataset. It contains various chemical properties of red wine, including:

Fixed acidity
Volatile acidity
Citric acid
Residual sugar
Chlorides
Free sulfur dioxide
Total sulfur dioxide
Density
pH
Sulphates
Alcohol
The target variable is the wine's quality, which ranges from 0 to 10.

Installation
Clone this repository or download the project files to your local machine.

bash
Copy code
git clone <repository-url>
Install the required Python packages.

bash
Copy code
pip install -r requirements.txt
Required packages:

pandas
numpy
sklearn
matplotlib
ucimlrepo
tensorflow
Run the wine_quality_prediction.py script to train the model and predict wine quality.

bash
Copy code
python wine_quality_prediction.py
Usage
Step 1: Train the Model
The script first trains a Random Forest Classifier using the UCI Wine Quality dataset. It splits the data into training and test sets, scales the features using StandardScaler, and fits the model.

Step 2: Model Evaluation
Once the model is trained, it will output the following evaluation metrics:

Accuracy: The percentage of correct predictions made by the model.
F1 Score: A measure of the model's performance that balances precision and recall.
Recall: The percentage of actual positives correctly identified by the model.
Classification Report: Detailed performance metrics for each class in the dataset.
Step 3: Custom Input Prediction
The script allows you to enter your own data for prediction. It will prompt you to input values for the following features (comma-separated):

Fixed acidity
Volatile acidity
Citric acid
Residual sugar
Chlorides
Free sulfur dioxide
Total sulfur dioxide
Density
pH
Sulphates
Alcohol
Example input:

Copy code
7.4, 0.7, 0.0, 1.9, 0.076, 11, 34, 0.9978, 3.51, 0.56, 9.4
After entering the values, the model will predict the wine's quality and provide the following outputs:

Predicted wine quality score
Model's evaluation metrics (Accuracy, F1 Score, Recall)
Detailed description of the features affecting wine quality
A classification report detailing how well the model performs on the test data.
Example Output
Model Evaluation:

yaml
Copy code
Accuracy: 0.9375
F1 Score: 0.9450
Recall: 0.9421
Classification Report:
              precision    recall  f1-score   support

           3       0.75      0.33      0.46        12
           4       0.87      0.89      0.88       137
           5       0.93      0.96      0.94       385
           6       0.93      0.90      0.91       223
           7       0.95      0.97      0.96       132
           8       0.92      0.92      0.92        67

    accuracy                           0.94       956
   macro avg       0.89      0.84      0.87       956
weighted avg       0.94      0.94      0.94       956
Custom Prediction Output:

vbnet
Copy code
Enter values for the following features (comma-separated):
Fixed Acidity, Volatile Acidity, Citric Acid, Residual Sugar, Chlorides, Free Sulfur Dioxide, Total Sulfur Dioxide, Density, pH, Sulphates, Alcohol
Enter values: 7.4, 0.7, 0.0, 1.9, 0.076, 11, 34, 0.9978, 3.51, 0.56, 9.4

--- Prediction Result ---
Predicted Wine Quality: 6

--- Model Insights ---
Model Accuracy on Test Set: 0.9375
Model F1 Score on Test Set: 0.9450
Model Recall on Test Set: 0.9421

--- Detailed Information ---
Wine quality is rated on a scale of 0-10, where higher values indicate better quality. The features provided represent different chemical compositions and attributes of the wine such as acidity, alcohol content, and residual sugar. The model uses these features to predict the wine's quality.

--- Example of Feature Descriptions ---
Fixed Acidity: Measures the acidity of the wine in g/t. A higher value indicates more acidic wine.
Volatile Acidity: Measures the amount of acetic acid in the wine. Too much can indicate spoilage.
Citric Acid: Adds freshness and flavor. A higher level may indicate a fruity taste.
Residual Sugar: The amount of sugar left after fermentation. Wines with higher residual sugar tend to taste sweeter.
Chlorides: Measures the salt content of the wine. Higher levels may indicate spoilage.
Free Sulfur Dioxide: Preservative used to prevent oxidation. A higher level may indicate preservation, but excessive levels can be harmful.
Total Sulfur Dioxide: The total amount of sulfur dioxide present. Similar to free sulfur dioxide, but includes bound forms.
Density: Measures the mass of the wine per unit volume. Can reflect the alcohol and sugar content.
pH: Indicates the acidity or alkalinity of the wine. Wines with lower pH tend to be more acidic.
Sulphates: A component that affects the wine's flavor and taste. Higher values can contribute to a stronger taste.
Alcohol: The percentage of alcohol in the wine. Higher alcohol content can influence the flavor profile.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Notes:
Ensure that you have installed all the necessary Python packages to run the script correctly.
You can customize the number of estimators and other hyperparameters for the RandomForestClassifier based on your needs to potentially improve the model's performance.
This README provides an overview of how to use the model, the expected output, and how to interpret the results, making it easier for others to understand and use your wine quality prediction model.






