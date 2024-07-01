# Weather & Crime Relationship

Data preprocessing:

Categorical features have been Encoded
Text columns and columns that have no effect on the model have been dropped
Added 7 lagged values
Performed data imputation
Identified and treated outlier
Model training:

Trained a LightGBM model using GridSearchCV

#Time Series Analysis:

I compared the model's performance with and without including the weather features. And observed that weather data slightly improved model performance.

Further, I investigated to which degree weather features affect individual offenses. According to the results 'Motor Vehicle Theft' is the crime most affected by weather, while 'Fraud Offenses' and 'Drug/Narcotic Offenses' are impacted very little by weather, which confirms our intuition.


# Motor Vehicle Theft

The higher precipitation values affect crime rates in a positive way, which can be explained because streets are less busy during rain and rain also covers noise to a certain degree. In addition, during higher moon phases crime rates are more increased. We conclude that bad weather and more light during nighttime help this type of crime.

# Larceny/Theft Offenses

Higher values of precipitation and windspeed impact Larceny/Theft Offenses in a negative way.

# Assault Offenses

We see here that all temperature-related features are correlated to the crime rate, and the explanation is that these features as well as Assault Offenses display a clear seasonal pattern.

# Conclusion

In conclusion, using a machine learning model and the data available we can see that certain crime types are affected by bad weather positively or negatively and that temperature levels also play a role in crime rates. But to determine a correlation between climate change and crime rates, we'd need higher granularity data and more accurate statistical tests.
