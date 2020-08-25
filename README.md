# Capital Bikeshare Data Analysis

___

## Overview

This was our final group project for **Methods of Applied Statistics In R** which enabled us to apply the techniques we learned from the class.  As part of the project, we simulated that we were a team of Data Scientists hired by Capital Bikeshare Company to come up with data driven answers to help them with their decisions. Bike-sharing rental process is highly correlated to the environmental and seasonal settings. For instance, weather conditions, precipitation, day of week, season, hour of the day, etc. can affect the rental behaviors. The core data set is related to the two-year historical log corresponding to years 2011 and 2012 from Capital Bikeshare system, Washington D.C., USA which is publicly available in http://capitalbikeshare.com/system-data. Our source aggregated the data on two hourly and daily basis. They extracted and added the corresponding weather and seasonal information. Weather information were extracted from http://www.freemeteo.com. 

There were 2 business questions we tried to address using the datasets described above. The first use case -- **Operational Expenses Analysis** which we predicted the manpower needed to cater extra demand and to reduce operational expenses. The second use case -- **Targeted Marketing Strategy Analysis** which would help the company to have a targeted marketing strategy to help them efficiently spend their budget.

## Team Approach

For the interest of each member to learn for this project we decided to split the work. 2 members worked separately on each use cases and the remaining member reviewed both strategy to make sure it aligns to the questions we want to be answered.

## Discussion

### Use Case 1 - Operational Expenses Analysis

While the final model contained a large number of predictors, making it difficult to interpret. The results indicate that it is very good at explaining the relationship between weather, season and bike sharing rentals. We tried evaluating using BIC to reduce the size of the final model, however, doing so resulted in a lowered adjusted R-squared and higher LOOCV-RMSE, so we preferred the AIC selected model.

As expected by looking this model, the weather situation is an especially important predictor. Both by itself and in its interactions with other predictors, indicating that rain has a significant impact on the number of rentals, especially the interaction between light rain and windspeed.

The high adjusted R-squared of the model shows that a very large portion of the variance in the data can be explained by this model, which would make it very useful for predicting demand for bikes and consequently predicting the operational cost for the Capital Bike Share.

### Use Case 2 - Targeted Marketing Strategy Analysis

On our preliminary assumption, Winter will be the season that would need an enhanced marketing strategy but it turned out upon finding the best model, Spring is the season that would require a better marketing strategy to attract additional customers.

If given additional time, we would like to explore why Spring season got the lowest prediction compared to our initial assumption of Winter season. Are there any methods that would lead us to a different best model? Are people biking a lot during Winter because they want the excitement of having snow and cold temperature? It will also be interesting to gather data around how often a customer rents a bike, a comparison of registered versus casual bike riders, and the type of bicycle – mountain bike, fat bike, or road bike.

To read the detailed report, please visit [Capital Bike Dataset Analysis](https://github.com/mikealpas/team_outliers/blob/master/Team_Outlier_Final_Proj.pdf)


