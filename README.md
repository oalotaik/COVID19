### Necessary Packages
Pandas, NumPy, Matplotlib, GeoPandas, and Seaborn

### Motivation
To analyze the relationship between COVID-19 and demographics, food deserts, food insecurity, and health factors


### Files
1. raw_data folder: contains the raw data that was used in the notebook `data_collections_preprocessing.ipynb`. You can find more info about the source and features of each dataset within the notebook.
2. `data_collections_preprocessing.ipynb`: notebook for preparing data (collecting data from multiple sources then preprocessing)
3. `initial_analysis.ipynb`: notebook for conducting basic analysis at the county level (for the first time)
4. `covid_cases_in_US.png`: A high resolution map visualizing the number of cases in US counties (output from `initial_analysis.ipynb`)
5. `analysis_2nd_attempt.ipynb`: a second attempt at analyzing data with more EDA for the features.
6. `county_data.csv` and `county_data2.csv`: county-level data regarding demographics, food deserts, food insecurity, and health factors (result of `data_collections_preprocessing.ipynb`). The `county_data2.csv` is just a more recent version.
7. `covid_daily.csv`: daily, cumulative counts of COVID-19 cases and deaths for US counties (result of `data_collections_preprocessing.ipynb`)

### Some Interesting Results
1. Strong correlation found between population density and COVID-19 occurrences
2. Correlation found between COVID-19 cases and low food accessibility. COVID-19 cases tend to decrease in counties with low access to a supermarket. This could be an indication that supermarkets help spread the virus more, and whoever has low access to them is a little safer. This is true except if the population who has low access is black. These findings are based on  Spearman's rank correlation coefficient. This coefficient is negative (-0.4 to -0.6) between COVID-19 cases and all low food access factors. However, it's positive (0.34) between COVID-19 cases and 'lablack1', which is % of black population who live beyond 1 mile from a supermarket. This is most likely due to the fact that counties with higher % black population tend to have more density (people/mile). 
3. Pearson correlation coefficient between COVID-19 and % of black population is low (0.04); however, Pearson coefficient is not appropriate here since the % of black population is not normally distributed (highly skewed). Therefore, Spearman coefficient is more suitable and it's higher (0.46). This suggests a monotonic relationship. But again, this could be explained by population density, which has a strong correlation with COVID-19 occurrences.

### Acknowledgement
1. Thanks to FeedingAmerica for providing data regarding food insecurity.
2. Thanks to New York Times for providing COVID-19 data
