# StreetEasy Manhattan Rent Prediction

This project utilizes a dataset from StreetEasy to predict apartment rental prices in Manhattan based on various features such as size, number of bedrooms and bathrooms, proximity to the subway, and building amenities. The script uses **linear regression** from the `scikit-learn` library to train a machine learning model.

## Dataset
The dataset contains information about rental listings in Manhattan and includes the following columns:
- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `size_sqft`: Square footage of the apartment
- `min_to_subway`: Minutes walking distance to the nearest subway
- `floor`: Floor number of the apartment
- `building_age_yrs`: Age of the building in years
- `no_fee`: Indicates if the listing is no-fee (1 for yes, 0 for no)
- `has_roofdeck`: Indicates if the building has a roof deck (1 for yes, 0 for no)
- `has_washer_dryer`: Indicates if the apartment has an in-unit washer/dryer (1 for yes, 0 for no)
- `has_doorman`: Indicates if the building has a doorman (1 for yes, 0 for no)
- `has_elevator`: Indicates if the building has an elevator (1 for yes, 0 for no)
- `has_dishwasher`: Indicates if the apartment has a dishwasher (1 for yes, 0 for no)
- `has_patio`: Indicates if the apartment has a patio (1 for yes, 0 for no)
- `has_gym`: Indicates if the building has a gym (1 for yes, 0 for no)
- `rent`: The target variable representing the apartment's rental price.

## Code Overview

### Libraries Used
- `pandas`: For data manipulation and analysis.
- `matplotlib.pyplot`: For plotting and visualization (imported but not used in this script).
- `scikit-learn`: For implementing machine learning models and splitting data into training and testing sets.

### Steps
1. **Load the Dataset**  
   The dataset is loaded from a CSV file hosted on GitHub into a pandas DataFrame.

2. **Feature Selection**  
   The script selects key features (`x`) and the target variable (`y`).

3. **Data Splitting**  
   The data is split into training (80%) and testing (20%) sets using `train_test_split`.

4. **Model Training**  
   A multiple linear regression model (`LinearRegression`) is trained using the training data.

5. **Prediction**  
   Predictions are made for the test set and for a sample apartment described by `sonny_apartment`.

### Sonny's Apartment
An example apartment with the following features is used to predict rent:
- 1 bedroom
- 1 bathroom
- 620 sqft
- 16 minutes to the subway
- Located on the 1st floor
- Building age: 98 years
- No fee
- No roof deck
- In-unit washer/dryer
- No doorman
- No elevator
- Has a dishwasher
- Has a patio
- No gym

The predicted rental value is printed to the console.

## Running the Code
To run the script:
1. Ensure Python and the required libraries (`pandas`, `scikit-learn`, `matplotlib`) are installed.
2. Copy and paste the code into a Python script or Jupyter Notebook.
3. Run the script. The predicted rental value for Sonny's apartment will be printed.

## Example Output
The value is: [[3240.678]]


This indicates that the predicted rent for Sonny's apartment is approximately $3,240.68.

## Further Improvements
- **Visualization**: Add plots to better understand the relationships between features and rent.
- **Feature Engineering**: Explore interactions or transformations of features for improved model performance.
- **Model Evaluation**: Use metrics like R² and RMSE to evaluate the model's accuracy.
- **Hyperparameter Tuning**: Experiment with different regression algorithms or configurations.
