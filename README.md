# Loan Prediction model

## Table of contents

- [Aim](#aim)
- [Data source](#data-source)
- [Data preparation](#data-preparation)
- [Model Training](#model-training)
- [Save the  model](#save-the-model)
- [Test the  model](#test-the-model)
- [Performance Metrics](#performance-metrics)
- [Recommandations](#recommandations)

  ---
### Project Overview
This project is a machine learning model that predicts whether a loan application will be approved or not, based on different features. It is built using DecisionTreeRegressor algorithm.

---
### Data Source

Loan Data: [Loan Approval Prediction Model](https://www.kaggle.com/code/experience08/loan-prediction)
---

### Tools
- Python 3
- Pandas, NumPy
- Scikit-learn
- imbalanced-learn (for SMOTE)
- Matplotlib / Seaborn (for visualizations)

### Data preparation
1. Data Cleaning.
2. Exploratory Data Analysis.
3. Model Training.
4. Evaluation.
5. Model Saving.

### Model training
The model was trained using Logistic Regression which is suitable for binary and multi-class classification problems.

```
Loan_Prediction_Model = RandomForestClassifier(n_estimators=100, random_state=42)
```

### Save the model
save and load the model for future use

```
import joblib
joblib.dump(Loan_Prediction_Model, "loan_approval_model.pkl")
```

###  Test the Model

use the loded model and new data to make a prediction

```
#Testing using new data
new_data=(24,2,20,0,7500,0,2,0,2,0,0,0,1,1,1,90,0,0,0,0,2)

# changing the input_data to numpy array
new_data_as_numpy_array = np.asarray(new_data)

# reshape the array as we are predicting for one instance
new_data_reshaped = new_data_as_numpy_array.reshape(1,-1)

prediction = loaded_model.predict(new_data_reshaped)
print(prediction)

if (prediction[0] == 0):
  print('The employee will stay in the company')
else:
  print('The employee will leave the company')
```

### Performance Metrics
1. Accuracy: ~0.84
2. ROC-AUC Score: ~0.88 (may vary depending on data split)
3. Classification report includes precision, recall, and F1-score


### Recommandations

To improve the model 
- Tune hyperparameters
- Perform feature engeneering




