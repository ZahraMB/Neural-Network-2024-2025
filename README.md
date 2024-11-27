Medical Cost Prediction with Custom Multi-Layer Perceptron (MLP) <br>
Overview
This project focuses on building a custom Multi-Layer Perceptron (MLP) model to predict individual medical costs based on personal factors. The dataset includes features such as age, gender, BMI, smoking status, number of dependents, and residential region in the US. The goal is to design, train, and optimize a neural network for this regression task, leveraging data preprocessing, model architecture tuning, and performance evaluation.

Dataset Description
The dataset consists of:

age: Age of the primary beneficiary.
sex: Gender of the policyholder (male/female).
bmi: Body Mass Index, correlating weight with height.
children: Number of dependents covered by the insurance.
smoker: Smoking status (yes/no).
region: Geographical region in the US.
charges: Medical costs billed by health insurance (target variable).

Project Features
1.Data Preprocessing:
-Encoding categorical features (e.g., one-hot encoding).
-Scaling and normalizing continuous features.

2.Model Design:
-Custom MLP architecture with optimized layers, neurons, and activation functions.
-Regularization techniques like dropout to prevent overfitting.

3.Evaluation:
-Performance measured using Mean Squared Error (MSE).
-Exploratory Data Analysis (EDA) for insights into feature relationships and distributions.

4.Report Highlights:
-EDA findings, model architecture, and hyperparameter tuning process.
-Detailed performance evaluation and error analysis.

Technologies Used
Python
TensorFlow/Keras for building the MLP model
Matplotlib/Seaborn for EDA visualizations

Usage
1.Clone the repository:
git clone https://github.com/your-username/Neural-Network-2024-2025.git
2.Open and run the Google Colab notebooks provided in the repository for step-by-step implementation.

Results
The final model predicts medical costs with optimized accuracy, leveraging a custom neural network design tailored for the dataset. Further improvements are outlined in the conclusion section.

Acknowledgments
This project was developed as part of an academic assignment focused on neural network design and implementation for real-world regression tasks.
