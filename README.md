# House-Price-prediction

## Abstract

House price prediction using Kijiji data involves estimating house values based on factors such as location, number of bedrooms, bathrooms, and other features. Four models were trained on a dataset of houses posted on Kijiji, considering factors that may affect home prices. These models make predictions about the price of a new house based on its characteristics, benefiting real estate agents, homebuyers, and homeowners in determining property values.

## Scraping Data from Kijiji

The initial steps involved scraping data using search links created from Kijiji. Data from about fifteen thousand posting links were gathered, and after cleaning and removing duplicates, seven thousand unique posting links remained. During the scraping process, null values were encountered, requiring adjustments and delays in the scraping program.

## Data Wrangling Steps

The dataset, consisting of 10 columns and 7975 rows, underwent cleaning and modification. Outliers in the 'price' column were addressed by flooring and capping at 6% and 99% quantile values. Data distribution analysis revealed outliers in the 'bathrooms' column, corrected manually. Inconsistencies were further addressed by removing data where the number of bathrooms exceeded bedrooms. Data distribution analysis revealed a concentration of data in the Ontario region, leading to the encoding of the 'province' column.

## Modeling

Five relevant features were selected based on a correlation plot, and the 'mapRadius' column was dropped. Linear regression visualizations were created, showcasing the potential for a regression model. A baseline model with Random Forest Regressor was created, and data were trimmed to improve the distribution. Log transformation was applied to the price column for normalization. After removing outliers, the Random Forest model exhibited improved validation R2 scores.

## Conclusion/Findings

- Models performed well in training but underperformed in validation/testing due to a lack of data points.
- The Random Forest Regressor and XGBoost Regressor showed the best performance with this dataset.
