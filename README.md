Real Estate Price Prediction using Machine Learning



Overview
This project aims to predict real estate prices in Bangalore using machine learning techniques. The goal is to provide insights into property 
values based on various features like square footage, the number of bedrooms, bathrooms, and location. Accurate price predictions can be valuable 
for homebuyers, sellers, and real estate investors.

Dataset
The dataset for this project is sourced from Kaggle and is available here. It contains information about real estate listings in Bangalore, including 
details such as location, size (number of bedrooms), total square footage, price, and more.

Project Structure
The project is organized as follows:

Data Loading and Cleaning: The dataset is loaded into a Pandas DataFrame, and initial data cleaning is performed. Missing values are handled, and unnecessary 
columns like "area_type," "society," "balcony," and "availability" are dropped.

Feature Engineering: New features are created, including the number of bedrooms (bhk), and the "total_sqft" feature is standardized to handle different formats.

Dimensionality Reduction: To reduce the number of location categories, a dimensionality reduction technique is applied, grouping less frequent locations into an "other" category.

Outlier Removal: Outliers are removed based on business logic, such as properties with unusually high or low prices per square foot or an unusual number of bathrooms.

Model Building: A Linear Regression model is trained to predict property prices based on the cleaned and transformed dataset.

Cross-Validation: K-fold cross-validation is used to assess the model's performance and ensure robustness.

Hyperparameter Tuning: A grid search is performed to find the best model among Linear Regression, Lasso, and Decision Tree Regressor.

Testing the Model: A function is provided to test the model with specific property details, giving users the ability to estimate property prices.

Exporting the Model: The trained model is exported to a pickle file for later use.

Exporting Columns Information: Column information is saved in a JSON file, which can be useful for feature selection when building a prediction application.
