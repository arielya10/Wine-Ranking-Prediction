# Wine Quality Classifier
This project aims to classify the quality of wine based on its rating, reviews, and other attributes. The quality is classified into two categories: "high" (rating above 4.1) and "poor" (rating below 4.1).

## Data Preprocessing
The data used in this project was obtained from https://www.wine.com/. Several steps were taken to prepare the data for machine learning:

1. The reviews column was cleaned by removing punctuation and converting all text to lowercase.
2. Rows with null values in the reviews column were removed.
3. Rows with a 0 value in the rating or abv column or a value less than or equal to 8 in the rating_count column were removed.
4. Any rows with a non-numeric value in the year column were removed.
5. The price column was converted to an integer data type and rows with a value greater than or equal to 250 were removed.
6. The rating column was converted to a float data type.
7. Rows with a year value less than or equal to 2000 or greater than or equal to 2021 were removed.
8. Rows with a value in the varietal column that did not appear in at least three other rows were removed, as were rows with a value in the origin column that did not appear in at least three other rows.
9. Duplicate rows were removed based on the product_name column.
10. Two new columns, varietal_code and origin_code, were added to the DataFrame, containing integer codes that represent the values in the varietal and origin columns, respectively.

## Data Visualization
1. A heatmap of the correlations between different columns in the DataFrame was created.
2. A line plot showing the average price of wine by year was created.
3. A scatter plot showing the correlation between rating and rating count was created.
4. A bar plot showing the most common adjectives used in the reviews was created.
5. Bar plots and strip plots were created to show the correlation between price, rating, and origin.
6. Scatter plots were created to show the correlation between price, rating, and year for different wine origins.

## Machine Learning
Several machine learning models were trained and evaluated to classify the quality of wine:
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Extra Trees
5. AdaBoost
6. Gradient Boosting
7. LightGBM
8. MLP
9. SVC
10. Naive Bayes  

The performance of each model was evaluated using accuracy,cross-validation score and F1 score. The best-performing model was AdaBoostClassifier, with an accuracy of 77.81%, a cross-validation score of 75.24% and a f1 score of 63.38%.

## Conclusion
After analyzing and visualizing the data, we found some interesting insights about the wine industry. We also applied several machine learning techniques to predict the quality of a wine based on its characteristics and reviews. Out of the various models we tried, AdaBoostClassifier performed the best with an accuracy of 77%. However, it is important to note that all the models had a relatively high accuracy, indicating that there are strong correlations between the features and the target variable.



