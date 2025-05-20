# Loan Prediction model

## Table of contents

- [Aim](#aim)
- [Data source](#data-source)
- [Data preparation](#data-preparation)
- [Model Training](#model-training)
- [Save the  model](#save-the-model)
- [Test the  model](#test-the-model)
- [Results](#results)
- [Recommandations](#recommandations)

  ---
### Project Overview
This project is a machine learning model that predicts whether a loan application will be approved or not, based on different features. It is built using DecisionTreeRegressor algorithm.

---
### Data Source

Loan Data: [Loan Approval Prediction Model](https://www.kaggle.com/code/experience08/loan-prediction)
---

### Tools
- Kaggle
- Python
- scikit-learn

### Data preparation
1. Data Cleaning.
2.  Exploratory Data Analysis.
3. Feature Engineering.
4. Model Training.
5. Evaluation.
6. Model Saving and Inference.

### Model training
The model was trained the Logistic Regression which is suitable for binary and multi-class classification problems.

```
 Loan_Prediction_Model = LogisticRegression()
```

### Save the model
save and load the model for future use

```

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

### Results

An accuracy of 69.68% was achived using the trained model

### Recommandations

To improve the model 
- Tune hyperparameters




