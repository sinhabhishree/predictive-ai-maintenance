# Predictive-ai-maintenance

**Introduction**
Predictive maintenance is a proactive approach to equipment management that aims to reduce unplanned downtime and extend the lifespan of assets. This project leverages machine learning techniques to predict maintenance requirements for machinery based on historical and real-time data. The primary objective is to classify equipment conditions and provide actionable insights to mitigate potential failures.

**Objectives**
To develop a robust predictive model for identifying maintenance needs.
To reduce operational downtime by predicting failures before they occur.
To provide interpretability through feature importance analysis.


**Dataset Overview**
The dataset used includes features like:
Temperature (°C)
Vibration (mm/s)
Pressure (Pa)
RPM

Target Variable: Maintenance Required (Binary: 1 - Maintenance Needed, 0 - No Maintenance).
The dataset was preprocessed to handle missing values, scale numerical data, and balance the classes using SMOTE.

**Methodology**
1. Feature Selection
Users select relevant features for prediction dynamically. These features are stored and used throughout the pipeline for consistency.

2. Data Preprocessing
Scaling: StandardScaler was used to normalize the feature set.
Balancing: SMOTE was applied to handle class imbalance.
Dimensionality Reduction: PCA reduced features to two principal components for visualization.
3. Model Optimization
Optuna, a hyperparameter optimization framework, was used to find the best parameters for a Random Forest Classifier.

4. Evaluation
The optimized model was evaluated using metrics like classification report, confusion matrix, and ROC-AUC score.

5. Real-Time Prediction
The system allows users to input real-time values for the selected features and predicts whether maintenance is required.

**Key Features**
Feature Importance Analysis: Highlights the most critical parameters influencing the prediction.
Model Persistence: The trained model and scaler are saved for reuse, enabling future predictions without retraining.
Interactive Input: User-friendly interface to input real-time data for predictions.
Results
Classification Report: The model achieved high accuracy, precision, and recall on the test set.
Confusion Matrix: Demonstrated balanced predictions between positive and negative cases.
Feature Importance: Revealed significant contributors to maintenance needs, like vibration and temperature.
Conclusion
This project successfully implemented a predictive maintenance system capable of identifying potential failures. The solution is adaptable to various industrial settings by leveraging machine learning and interactive inputs. The system's scalability and efficiency make it a valuable tool for operational reliability.

