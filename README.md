# Determining the Rent to Charge for An Apartment in Germany
## 1. Introduction
After investing much time, energy and money to prepare and stage an apartment for rent, the last thing a landlord wants to see is for the apartment to sit empty for a month, two months or more before the property clears. In real estate, as in other industries, time is money, and the longer a property remains on the market, the worse-off the financial performance of the asset. For one, expenses such as mortgage, property tax and heat still require payment regardless of whether or not the apartment is occupied.  An unrented property also draws suspicion from prospective tenants if it sits on the market for too long. Tenants may wonder about the hidden issues associated with such a property for it to stay so long on the market. Landlords are keenly aware of these concerns and strive to set the appropriate price for a unit. They may result to offering incentives, such as a month's free rent, or furniture, when things start getting desperate. Eventually, the landlord is forced to reduce the rent, and at times, do so at a price below monthly expenses, such that the property generates losses. 

The rent of an apartment that can be supported by the market depends on a wide variety of factors. Some factors are specific to the apartment, while others relate to the macro-economic conditions of the location in which the apartent is situated. These factors will examined in an effort to develop a rudimentary model that can assist a landlord in properly pricing an apartment.

### a. Project Objective
The goal of this project is to explore the asset-specific features and macro-economic factors that influence the rent stipulated for an apartment in an effort to create a rudimentary model that can assist landlords in setting their apartment rents in Germany.

### b. Data
The primary dataset used for our analysis was from Kaggle.ca. The data was originally scraped from Immoscout24 - the biggest real estate website in Germany. Immoscout24 lists both properties for rent and for sale, although only rental information was included with the dataset. The dataset (downloaded as a csv file) had over 268,000 rental listings, scraped on three days - September 22, 2018; May 10, 2019; and October 08, 2019 - such that the variation of market conditions could be analyzed over time. Each listing was described by 49 features comprising of location data, data on monthly expenses including rent, asset-specific data and time data. While there were initially more numerical features than categorical ones, we ended up with mostly categorical features after cleaning the dataset. The Kaggle dataset can be accessed at https://www.kaggle.com/corrieaar/apartment-rental-offers-in-germany.

The primary dataset was augmented by a state-wide macro-economic dataset extracted from Wikipedia. Each state was described by four main features such as its area, 2019 population, Human Development Index and GDP per capital in 2018. 


## 2. Data Aquisition and Cleaning
Acquiring data was relatively straightforward and consisted of importing the Kaggle csv file, as well as importing the Wikipedia dataset to the notebook from the related web link. Cleaning the data was more challenging, especially on the rental listings dataset, as preliminary analysis was required to transform features and determine which features to retain for exploration. 
- __Dealing with features having many missing values:__<br>
Features with missing values were examined to determine if there were any patterns associated with with missigness, if there was enough data to make the feature useful, and if imputation with a nominal value was possible. In so doing, we wanted to minimize data loss, but also make sure that only informative features were retained in the dataset. Of the 49 original features, under half of them had complete data and about 9 features had over 50% missing values. 
- Dealing with high-cardinality features
- Dealing with text features
- Dealing with highly skewed features and outliers
- Dealing with duplicate listings
- Dealing with incorrect cross-field validation values
- Dealing with inconsistent category names
- Dealing with features having concatenated values
- Preventing data leakage
- 
- 
## 3. Exploratory Data Analysis
## 4. Data Pre-processing and Model Creation
## 5. Model Application
## 6. Conclusion / Recommendations
## 7. Assumptions and Limitations

