# Determining the Rent to Charge for An Apartment in Germany
## 1. Introduction
After investing much time, energy and money to prepare and stage an apartment for rent, the last thing a landlord wants to see is for the apartment to sit empty for a month, two months or more before the property clears. In real estate, as in other industries, time is money, and the longer a property remains on the market, the worse-off the financial performance of the asset. For one, expenses such as mortgage, property tax and heat still require payment regardless of whether or not the apartment is occupied.  An unrented property also draws suspicion from prospective tenants if it sits on the market for too long. Tenants may wonder about the hidden issues associated with such a property for it to stay so long on the market. Landlords are keenly aware of these concerns and strive to set the appropriate price for a unit. They may result to offering incentives, such as a month's free rent, or furniture, when things start getting desperate. Eventually, the landlord is forced to reduce the rent, and at times, do so at a price below monthly expenses, such that the property generates losses. 

The rent of an apartment that can be supported by the market depends on a wide variety of factors. Some factors are specific to the apartment, while others relate to the macro-economic conditions of the location in which the apartent is situated. These factors will examined in an effort to develop a rudimentary model that can assist a landlord in properly pricing an apartment.

### a. Project Objective
The goal of this project is to explore the asset-specific features and macro-economic factors that influence the rent stipulated for an apartment in an effort to create a rudimentary model that can assist landlords in setting their apartment rents in Germany.

### b. Data
The primary dataset used for our analysis was from Kaggle.ca. The data was originally scraped from Immoscout24 - the biggest real estate website in Germany. Immoscout24 lists both properties for rent and for sale, although only rental information was included with the dataset. The dataset (downloaded as a csv file) had over 268,000 rental listings, scraped on three days - September 22, 2018; May 10, 2019; and October 08, 2019 - such that the variation of market conditions could be analyzed over time. Each listing was described by 49 features comprising of location data, data on monthly expenses including rent, asset-specific data and time data. While there were initially more numerical features than categorical ones, we ended up with mostly categorical features after cleaning the dataset. The Kaggle dataset can be accessed here [dataset](https://www.kaggle.com/corrieaar/apartment-rental-offers-in-germany).

The primary dataset was augmented by a state-wide macro-economic dataset extracted from Wikipedia. Each state was described by four main features such as its area, 2019 population, Human Development Index and GDP per capital in 2018. 


## 2. Data Aquisition and Cleaning
Acquiring data was relatively straightforward and consisted of importing the Kaggle csv file, as well as importing the Wikipedia dataset to the notebook from the related web link. Cleaning the data was more challenging, especially on the rental listings dataset. Missing values, features with many categories, text features, (log-transformation) outliers, duplicate entries, cross-field valdiation of aggregation features, inconsistent category names, hyphenated values, and data leakage, were challenges that were resolved during the data cleaning process. Data definition - making sure that features had the appropriate datatype. Modelling base rent instead of total rent. The intent of data cleaning was to create a final dataset that was reflective of the ground truth. 
We explored individual feature
- Distribution of categorical features with barplots
- Distribution of numerical features with histograms and box plots
- Went from a shape of 268,859 x 49 to 267,690 x 30.
- String similarities of feature values
- Information on data wrangling steps could be reference here: [data_wrangling](http://localhost:8888/notebooks/Capstones/Capstone_2/german_apartment_rentals/notebooks/A_data_wrangling_final.ipynb). 

![State distribution of listings](https://github.com/femi-lujo/german_apartment_rentals/blob/final/reports/figures/state_listings_distr.png)
- 
## 3. Exploratory Data Analysis
The focus of exploratory data analysis was to investigate the relationship between the base rent and other variables, as a means to pre-select features for modelling. Guessing that location factors would highly influence base rent, new features were created that aggregated information at each location level. In order of resolution (from lowest to highest), the location levels include the state, city or town, municipality and zip code. This meant
- aggregation at the location levels of rentals dataset
-   aggregating by medians instead of means due to the skewed nature of most variables
- review of the influence of time features
- review of the influence of numerical features pertaining to the rentals dataset
- review of the influence of categorical features
- review of the influence of state wide features
- review of the influence of state density features
- 
## 4. Data Pre-processing and Baseline Model Creation
- Pre-processing step was to prepare the data and create a baseline model.
- Most imputation of numerical values
- Encoding of categorical features
- Scaling data
- Determining performance metrics
- Creating a baseline model
- 
## 5. Model Optimization and Selection
- Trialing other ways to improve the performance of the baseline model
- Cross-validation and dealing with overfitting
- Linear algorithms and tree-induction alogrithms
- Hyperparameter tuning
- Feature importance
- Performance
- 
## 6. Conclusion / Recommendations
- Model was good
- Assist landlords within an error band of +- something with 90% confidence interval
- Looking forward
-   Derive more features from text analysis of description and facilities field
-   Gathering of data every quarter rather than at random intervals may allow for better time-series analysis
-   Hyperparamter tuning a more robust approach like grid search or bayesian optimization rather than random search
-  
## 7. Assumptions and Limitations
- State-wide summary information was date agnostic
- Influence of COVID and other world events not captured in model
- How long a listing stayed 
- Gathering of data every quarter
