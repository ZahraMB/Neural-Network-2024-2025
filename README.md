# Medical Cost Prediction with Custom Multi-Layer Perceptron (MLP) <br>
## Overview
This project focuses on building a custom Multi-Layer Perceptron (MLP) model to predict individual medical costs based on personal factors. The dataset includes features such as age, gender, BMI, smoking status, number of dependents, and residential region in the US. The goal is to design, train, and optimize a neural network for this regression task, leveraging data preprocessing, model architecture tuning, and performance evaluation.

## Dataset Description
The dataset consists of:<br>

age: Age of the primary beneficiary.<br>
sex: Gender of the policyholder (male/female).<br>
bmi: Body Mass Index, correlating weight with height.<br>
children: Number of dependents covered by the insurance.<br>
smoker: Smoking status (yes/no).<br>
region: Geographical region in the US.<br>
charges: Medical costs billed by health insurance (target variable).<br>

## Project Features
1.Data Preprocessing:<br>
-Encoding categorical features (e.g., one-hot encoding).<br>
-Scaling and normalizing continuous features.<br>

2.Model Design:<br>
-Custom MLP architecture with optimized layers, neurons, and activation functions.<br>
-Regularization techniques like dropout to prevent overfitting.<br>

3.Evaluation:<br>
-Performance measured using Mean Squared Error (MSE).<br>
-Exploratory Data Analysis (EDA) for insights into feature relationships and distributions.<br>

4.Report Highlights:<br>
-EDA findings, model architecture, and hyperparameter tuning process.<br>
-Detailed performance evaluation and error analysis.<br>

## Technologies Used
Python<br>
TensorFlow/Keras for building the MLP model<br>
Matplotlib/Seaborn for EDA visualizations<br>

## Usage
1.Clone the repository:<br>
git clone https://github.com/your-username/Neural-Network-2024-2025.git<br>
2.Open and run the Google Colab notebooks provided in the repository for step-by-step implementation.<br>

## Results
The final model predicts medical costs with optimized accuracy, leveraging a custom neural network design tailored for the dataset. Further improvements are outlined in the conclusion section.

## Acknowledgments
This project was developed as part of an academic assignment focused on neural network design and implementation for real-world regression tasks.
