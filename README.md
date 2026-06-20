Breast Cancer Classification using Logistic Regression

PROJECT OVERVIEW
Early and accurate detection of breast cancer plays a vital role in patient survival rates. This project utilizes the Breast Cancer Wisconsin (Diagnostic) Dataset to train a machine learning model capable of distinguishing between malignant and benign tumors. The model uses clinical features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass, describing characteristics of the cell nuclei present. The primary objective is to build a reliable classification pipeline, evaluate its baseline performance, and build an interactive predictive system for assessing single patient diagnostic inputs.
DATASET FEATURES
The dataset includes 30 distinct features computed from the cell nuclei, including:
Radius: Mean of distances from center to points on the perimeter.
Texture: Standard deviation of gray-scale values.
Perimeter and Area of the tumor core.
Smoothness: Local variation in radius lengths.
Target Labels: 0 for Malignant, 1 for Benign.
TECH STACK AND DEPENDENCIES
Language: Python
Libraries:
NumPy: Used for efficient numerical operations and array manipulations.
Pandas: Used for data loading, manipulation, and exploratory analysis.
Scikit-Learn: Used for dataset extraction, model training, and evaluation metrics.
PIPELINE WORKFLOW
Exploratory Data Analysis (EDA)
Inspected the dataset topology and feature types using .head(), .tail(), and .info().
Verified data integrity and checked for missing or null entries via .isnull().sum().
Analyzed sample data distributions and target class balance with .describe() and .value_counts().
Data Splitting
Separated the independent features (X) from the dependent target classes (Y).
Partitioned the dataset using an 80/20 train-test split to ensure unbiased testing on unseen data.
Model Training
Initialized a LogisticRegression classifier.
Configured optimization parameters to guarantee structural convergence over the 30 descriptive features.
Evaluation
Tracked and compared classification accuracy across both the training subset and the test subset to verify the model's generalized capability.
Single-Instance Predictive System
Developed a pipeline component that accepts raw, single-patient matrix inputs, reshapes them, maps the appropriate schema feature alignment, and delivers an instant diagnosis string (Malignant or Benign).
KEY FINDINGS AND RESULTS
Accuracy on Training Data: 96.92% (0.9692307692307692)
Accuracy on Testing Data: 92.98% (0.9298245614035088)
Performance Analysis:
The model demonstrates excellent performance, achieving approximately 97% accuracy on the data it learned from and 93% accuracy on completely unseen test data. The close proximity between the training and testing scores indicates that the model has generalized well and is not overfitting to the training subset.
