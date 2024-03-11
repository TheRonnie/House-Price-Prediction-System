# House-Price-Prediction-System
This project utilizes linear regression to predict house prices based on various features such as area, bedrooms, and amenities, achieving an R-squared score of 0.70.

Here's a breakdown of what you've done:

1.	Data Preprocessing:

•	You loaded the dataset and performed some initial exploratory data analysis.
•	Checked for missing values and outliers, and handled outliers using the IQR method.
•	Converted categorical variables into binary (0/1) using one-hot encoding.
•	Split the data into features (X) and target variable (Y), and then further split them into training and testing sets.

2.	Model Building and Evaluation:

•	You used the Linear Regression model from scikit-learn to train on the training data.
•	Predicted house prices using the trained model on the test data.
•	Evaluated the model's performance using the R-squared score, which measures how well the independent variables explain the variance in the dependent variable (house prices).

3.	User Input Prediction:

•	You collected user input for various features of a house (area, bedrooms, bathrooms, etc.) to predict the price of a new house.
•	You then used the trained model to predict the price based on the user input.


However, there are a few issues and improvements that could be made:

1.	Handling Categorical Variables:

•	When converting categorical variables into binary, ensure that you drop one of the columns to avoid the dummy variable trap. It seems you have handled this correctly by dropping the 'furnishingstatus' column after creating dummy variables.

2.	User Input Handling:

•	There seems to be a mistake in your input handling code. The variable a is assigned as a string, but you're trying to compare it to integers later on. You should convert it to an integer before comparing.
•	You should also handle the case where the user inputs a value other than 1, 2, or 3 for the furnishing status.

3.	Model Performance:

•	While the R-squared score of 0.70 indicates that the model explains 70% of the variance in the target variable, it's always good to explore other evaluation metrics and possibly try different models to see if you can improve performance.

4.	Further Data Exploration:

•	Consider exploring the relationships between different features and the target variable in more detail. This could involve visualizations such as correlation matrices or scatter plots to understand the relationships better.


