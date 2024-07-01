# weather-crime-relationship

Data preprocessing:

Categorical features have been Encoded
Text columns and columns that have no effect on the model have been dropped
Added 7 lagged values
Performed data imputation
Identified and treated outlier
Model training:

Trained a LightGBM model using GridSearchCV
Time Series Analysis:

We compared the performance of the model with and without including the weather features. And observed that weather data slightly improved model performance.
MAE	MSE	MAPE	RMSE
Model without weather	38.401318	2805.280708	0.055510	52.964901
Model with weather	37.860209	2654.924996	0.054174	51.525964
Further, we investigated to which degree weather features affect individual offenses. According to our results 'Motor Vehicle Theft' is the crime most affected by weather, while 'Fraud Offenses' and 'Drug/Narcotic Offenses' are impacted very little by weather, which confirms our intuition:
Crime type	Weather features importance
Motor Vehicle Theft	0.2243
Robbery	0.2046
Larceny/Theft Offenses	0.1826
Burglary/Breaking & Entering	0.086
Assault Offenses	0.083
Destruction/Damage/Vandalism of Property	0.0754
Drug/Narcotic Offenses	0.057
Fraud Offenses	0.041
Then we analyzed in more detail the influence of weather on individual crime types
3.1. Motor Vehicle Theft

The higher precipitation values affect crime rates in a positive way, which can be explained because streets are less busy during rain and rain also covers noise to a certain degree. In addition, during higher moon phases crime rates are more increased. We conclude that bad weather and more light during nighttime help this type of crime.

3.2. Larceny/Theft Offenses

Higher values of precipitation and windspeed impact Larceny/Theft Offenses in a negative way.

3.3. Assault Offenses

We see here that all temperature-related features are correlated to the crime rate, and the explanation is that these features as well as Assault Offenses display a clear seasonal pattern.

Conclusion
In conclusion, using a machine learning model and the data available we can see that certain crime types are affected by bad weather in a positive or negative way and that temperature levels also play a role in crime rates. But in order to determine a correlation between climate change and crime rates, we'd need higher granularity data as well as more accurate statistical tests.
