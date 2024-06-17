# Flu-vaccine-predictor

**Description:**

This project aims to predict the likelihood of individuals receiving the xyz and seasonal flu vaccines. Utilizing a comprehensive dataset with various demographic, behavioral, and opinion-based features, this model estimates the probabilities for each type of vaccine uptake. The primary objectives are to accurately forecast two probabilities: one for the xyz vaccine and one for the seasonal flu vaccine.

**Project Features:**

- **Multilabel Classification**: The problem is formulated as a multilabel classification, where each individual may receive either, both, or neither of the vaccines.
  
- **Data Preprocessing**: 
  - Handling missing values by filling them with the mode.
  - Encoding categorical variables using one-hot encoding to convert them into numerical format.
  - Ensuring consistent feature alignment between training and test datasets.

- **Model Training**:
  - Employing a `RandomForestClassifier` wrapped in a `MultiOutputClassifier` to handle the multilabel nature of the task.
  - Splitting the data into training and validation sets to evaluate model performance.

- **Evaluation Metrics**:
  - Using the ROC AUC score to measure the performance of the model for each target variable.
  - Calculating the average ROC AUC score to provide an overall assessment of model performance.

- **Prediction**:
  - Generating probability predictions for the test dataset.
  - Outputting the predictions in a format suitable for submission, including respondent IDs and their associated vaccine uptake probabilities.

**Dataset Description**:

The dataset comprises 36 columns:
- **respondent_id**: A unique identifier for each individual.
- **Features**: 35 features including demographic details (age, sex, race, etc.), behavioral patterns (mask usage, handwashing, etc.), and opinions on vaccine effectiveness and risks.

**Usage**:

To use this project:
1. Clone the repository.
2. Ensure you have the required datasets in the specified directory.
3. Run the provided Python script to preprocess the data, train the model, and generate predictions.

**Dependencies**:
- `pandas`
- `scikit-learn`
- `notebook` (Jupyter)

**How to Run**:

```sh
# Clone the repository
git clone https://github.com/your-username/Flu-vaccine-predictor.git

# Navigate to the project directory
cd Flu_vaccine_predictor

# Ensure the datasets are placed in the specified directory
# Run the script
jupyter notebook Flu_vaccine_predictor.ipynb
```

This project provides a robust framework for predicting vaccine uptake probabilities using machine learning techniques, ensuring a comprehensive approach to data preprocessing, model training, and evaluation.
