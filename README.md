# Kenya Food & Nutrition Security Analysis

## Project Overview
This project explores food price patterns across different locations and time periods in Kenya. The analysis uses food price data to understand how prices of commonly consumed food commodities vary across markets and administrative areas.The project also uses machine learning to predict average food prices based on factors such as location and time.The analysis is intended as a starting point for understanding food affordability in Kenya and can later be extended by incorporating poverty, nutrition and household-level indicators.
## Research Question
How do food prices vary across different locations and over time in Kenya and can these patterns be used to predict average food prices?
## Objectives
- Explore food price patterns across different locations in Kenya.
- Examine how food prices change over time.
- Compare average prices of selected food commodities.
- Identify locations with differences in average food prices.
- Build a machine learning model to predict average food prices.
- Identify the features that contribute most to the model's predictions.
## Dataset
The dataset contains food price observations from different markets and administrative areas in Kenya.
Key variables used in the analysis include:
- "price_date" — date of the observation
- "adm2_name" — administrative area
- "mkt_name" — market
- "lat" and "lon" — geographical coordinates
- "beans"— bean price
- "maize_fao" — maize price
- "livestock_goat_s_fao" — goat price
The dataset covers observations from 2007 to 2026.
## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- GitHub
## Analysis
The project followed several stages:
### 1. Data Exploration
The dataset was inspected to understand its structure, variables, missing values, locations and time period.
### 2. Exploratory Data Analysis
Food prices were examined across time and location. Monthly averages were used to identify price patterns while countylevel averages were used to compare differences between locations.The analysis focused particularly on beans and maize because these were among the available food price variables.
### 3. Feature Engineering
Additional variables were created from the date and food price information including:
- Year
- Month
- Quarter
- Average food price
- Food price index
The average food price was calculated from the available food price variables for each observation.
### 4. Machine Learning
A Random Forest Regression model was used to predict average food prices.
The model used:
- Year
- Month
- Quarter
- Latitude
- Longitude
- Administrative area
## Model Performance
The Random Forest model achieved the following results on the test data:
| Metric | Result |
| ------ | -----: |
| MAE    | 274.25 |
| RMSE   | 409.23 |
| R²     |   0.64 |

An R² of 0.64 means that the model explained approximately 64% of the variation in average food prices in the test data.
The model was also compared with a tuned Random Forest configuration. The tuned model performed worse on the test data so the original Random Forest model was retained as the final model.
## Key Findings
- Food prices varied across different locations and over time.
- Location was an important factor in predicting average food prices.
- Longitude was the most important feature in the Random Forest model.
- Year was also highly important suggesting that prices changed substantially over time.
- Several administrative areas contributed strongly to the model's predictions.
- The model captured a substantial proportion of price variation but some predictions still had noticeable errors.
## Actual vs Predicted Prices
The actual versus predicted analysis showed a positive relationship between the observed and predicted food prices. However, there was still some spread around the expected values showing that the model did not capture every factor affecting food prices.
## Limitations
This analysis focuses mainly on food prices and does not directly measure household food consumption, income, poverty or nutritional status.Food prices can also be affected by factors that were not included in the model such as:
- Weather and drought
- Transportation costs
- Market conditions
- Seasonal supply
- Household income
- Economic changes
Therefore food prices should be treated as one component of a broader food and nutrition security analysis.
## Future Work
Future versions of this project could combine food price data with:
- Poverty indicators
- Household income and expenditure data
- Nutrition indicators
- Food consumption data
- Climate and rainfall data
- Population and demographic information
This would allow a broader assessment of food affordability and nutrition security across different parts of Kenya.
## Conclusion
The analysis shows that food prices in Kenya vary across both location and time. The Random Forest model was able to explain a meaningful proportion of this variation with location and year among the strongest predictors.The project provides a foundation for further analysis of food affordability and nutrition security by combining food price information with socioeconomic, nutritional and environmental data.
