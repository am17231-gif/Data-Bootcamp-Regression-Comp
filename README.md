# Data-Bootcamp-Regression-Comp

Ames Housing Regression: Small Group Competition

This project predicts house sale prices in Ames, Iowa for the Kaggle regression competition (evaluated by RMSE). The notebook Ames_Housing_Regression.ipynb walks through our whole process, such as exploring the data, cleaning missing values using the data dictionary, engineering features (total square footage, total bathrooms, house age, and converting quality ratings to numbers), and removing one unrepresentative outlier from the training data.

We compared several models using a train/validation split and cross-validation, with simple and multiple linear regression, Ridge, Lasso, and gradient boosting. Our final model is a Ridge regression fit on log(SalePrice), with scaled numeric features and one hot encoded categorical features, and with its strength tuned using GridSearchCV. Polynomial features did not improve cross-validation results, so they were left out. Test predictions are clipped to the range of the training data to avoid extrapolating on one unusually large house.
