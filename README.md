# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

*Accessing data by using APIs.

*Cleaning and transforming data using Python

*Loading data into a database using Python

*Performing EDA, including using both statistics and visualizations

*Identifying trends and patterns in data using statistical models

*Interpreting the results of the statistical models

## Process

The project was develop in 4 stages that are presented in the diagram below:

![Project Process - Flow Structure](/data/ProjectProcess.JPG) 

## Results

As part of the input for the DB of the project, it was decided to merge info collected from Yelp API with the one extracted from CitiBikes.

Particularly, Yelp API provided a more complete data becuase of the following:

*It contains a wider variety and higher amount of POIs.

*It has more features that contribute to enrich the analysis of this proyect (such as rating and reviews).

#### The regression model was built using the Backward Selection method.

In the 1st step of the method, all independent variables were included ('distance_to_station', 'rating', and 'reviews'). After running it was identified that, the R-square value of 0.007 is quite low and indicates that the model might not to be a good fit for the data. Regarding the p-values, 'dist2station' (0.265) and 'rating' (0.186) may not be statistically significant relevant. Therefore, in the next step 'dist2station' variable will be dropped.

Then, in the 2nd step of the method the 'distance_to_station' variable was dropped because it wasn't statistical significant relevant. 'rating' and 'reviews' independent variables were included in the model. As result, the value of the R-square obtained (0.007) continued being quite low. Additionally, the independent variable 'rating' exhibited a p-value of 0.191 making it not statistically significant relevant and the next candicate to be dropped in step 3.

Finally, in the 3rd step of the method, the variable 'rating' was dropped and was run with only the 'reviews' variables. In this last step, the model continued exhibiting a very low R-squared value of only 0.007. On the other, despite that the p-value of 'reviews' variable was zero, it was concluded that this model was NOT a good fit for the data (or in other words, it did not expalain the data).

## Challenges 

One downside of the Yelp API was that the Radius filter is not working. The 2 options were tested without sucess: i. passing the radius filter as part of the dictionary params and ii. including the this filter embeded in the Endpoint. Consequently, the resulting table from this API is almost 5 times bigger in comparison to the Foursquare one. 

## Future Goals

*I would try to implement more categories of the APIs aiming of finding more statistically significant variables that fit a regression model.

*I would explore a wider variety of POIs in the dataframe to feed the regression model.

