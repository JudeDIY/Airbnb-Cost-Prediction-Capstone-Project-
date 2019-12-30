# Airbnb-NEW YORK-Cost-Prediction-Capstone-Project-
Data based on the Airbnb listings of New York City boroughs, this dataset is used to find hidden patterns and other relevant information about the listings. How are rental properties scattered around the NYC Neighborhood? Prices varying from which factors, room types, local attractions. All this information used to predict the relevant Pricing of the listing to attract more customers.  
- Key skills: Linear Regression, Sklearn, Matplotlib, Tableau

This dataset has around 48,377 observations in it with 106 columns and it is a mix between categorical and numeric values.

In These 106 columns, 40 Columns provide a very rich amount of information for deep data exploration we can do on this dataset. We do already see some missing values, which will require cleaning and handling of NaN values. Later, we may need to continue with mapping certain values to ones and zeros for predictive analytics.

In our case, missing data that is observed does not need too much special treatment. Looking into the nature of our dataset we can state further things: columns "name" and "host_name" are irrelevant and insignificant to our data analysis, columns "cleaning_fee" and "security_deposit" need very simple handling. 

Label Encoding can be done to convert categorical features into numerical features

Columns [Price, extra_people, security_deposit, cleaning_fee] can be treated by removing the string variables and convert it into float dtype.

Columns [last_scraped, first_review, last_review, host_since] can be converted it into datetime dtype.

Calculating [List_duration] by Subtracting [last_review - first_review]
Calculating [hosting duration] by Subtracting [last_review - host_since]
Calculating [price_per_person] by Dividing [price - accommodates]

Calculate [Distance] from Latitude and Longitude  
Distance - Calculate distance by using the latitude and longitude of the center point of New York. 
And by Subtracting it with the hotel_latitude and hotel_longitude using Distance Formula.

Results without Feature Engineering:
The model performance for training set R2 score is 0.698782957074438
The model performance for testing set R2 score is 0.7899394341859203

Results with Feature Engineering:
The model performance for training set R2 score is 0.698782957074438
The model performance for testing set R2 score is 0.7899394341859203

Data Insights:

1. Price of Most of the Listings are $105 - $150.
2. Price of Shared room is lower than private room and entire house/ apartment
3. price of Rooms in Manhattan and Brooklyn boroughs are more than the rooms in boroughs
4. 75% of people spend 5 nights
5. There is a 50% chance that the rooms will be available for at least 45 days 
6. Manhattan has Highest number of listings
7. Brooklyn has more Number of listings after Manhattan 
8. Most of the Listings are Entire Home/apartments and private rooms 
9. 95% of them have reviews per month less than 10 
10. Most(75%) of the host listing count are less than 50 
11. Bronx has less number of night stays as compared to other
12. Where Manhattan and Brooklyn collect High Security Deposit.
13. Where Astoria and Brooklyn receives highest No.of.Reviews.  
14. Hotel Room And Entire home/apt is High Priced.
15. Long Island City and Brooklyn has the highest Cost Per Person

Business Recommendation:

By Using this Airbnb New York dataset we are predicting that the price suggested by Airbnb is cost effective or expensive.
Thus XG Boost Performs Better With and Without Feature Engineering.
