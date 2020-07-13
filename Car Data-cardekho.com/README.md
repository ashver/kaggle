# Car dataset: 

Objective of this exercise is to create a machine learning model to predict selling price of a used car and create a production deployment demo using flask.

## The Data

This dataset contains information about used cars listed on www.cardekho.com.
This data can be used for a lot of purposes such as price prediction to exemplify the use of different regression algorithm in Machine Learning.
The columns in the given dataset is as follows:

1. Car_Name
2. Year
3. Selling_Price
4. Present_Price
5. Kms_Driven
6. Fuel_Type
7. Seller_Type
8. Transmission
9. Owner

Kaggle Data source: https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho

# Flask-Deployment

Deployement of machine learning model on production using Flask API(demo)

## Structure
This project has three major parts :

1. rf_model.plk - Random-forest model pickle file.
2. app.py - This contains Flask APIs that receives details through API calls, computes the precited value based on our model and returns it.
3. templates - This folder contains the index.html (HTML template) to allows user to enter variable-details and displays the predicted selling price based on the entered details.
