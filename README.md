# covid-19-explainable-healthy-diet-data

## Data Set Description

Our goal was to obtain a rich explanation of the variations in country-wise COVID-19 mortality rates. For that reason, a wider context was considered, consisting initially of multiple factors representing country-wise nutritional habits, enriched with past comorbidity prevalence, different economic and development factors, environmental and ecological variables. 
The data set contains information for 154 countries. The attributes were logically combined into three subgroups of data: dietary data, comorbidity data, and country development data. 

### Dietary data
The dietary data set consists of food supply data collected from the FAO database[1](http://www.fao.org/faostat/en/#home). The available features represent fat supply quantity, food supply measured in kg, food supply measured in kcal and protein supply quantity. The food groups are organized by the hierarchy defined by Food and Agriculture Organization (FAO)/WHO STAT, resulting in a total of 23 diet related features. The features are measured in percentage of the total country-wise food consumption. 

Analyzing how different nutritional patterns influence the outcomes of COVID-19 may give us the knowledge to identify food consumption patterns that countries with low case fatality rates exhibit. If deemed significant, these dietary patterns may be used in the prevention of a more severe escalation of the disease by adjusting our diet accordingly.

### Comorbidity data
It is widely considered that some chronic diseases influence the severity of symptoms and the outcome in COVID-19 infected patients [2](https://pubmed.ncbi.nlm.nih.gov/32489711/) [3](https://pubmed.ncbi.nlm.nih.gov/32377638/). We have considered establishing a relationship between mortalities caused by a wide variety of diseases and illnesses with the goal of achieving a broader and more relevant explanation of COVID-19 mortality rates. For this reason, we have collected country-wise data on past mortality rates attributed to 17 different groups of illnesses, to assess the impact of other comorbid conditions. We may consider that a similar distribution of comorbid conditions exist in the current population and use these factors as an estimate of the situation.

The comorbidity data set contains features representing the country-wise number of deaths due to different diseases, as organized by the highest level of ICD-10 categorization [4](https://icd.who.int/browse10/2010/en). The data set consists of 17 comorbidities.

### Country development data
In order to enrich the context as much as possible, we have further gathered data to represent country-wise economic and development status by adding HDI scores and GDP values dating from 2016 to the latest available date.  In addition, we have considered the percentage of obese and undernourished population of each country in order to obtain a more detailed characterization of different lifestyles.

Since countries that are close together often have similar lifestyle and dietary habits, we have included the minimum and maximum latitude and longitude of each country as spatial characteristics to consider the potential influence of the geographic location. 

Studies [5](https://pubmed.ncbi.nlm.nih.gov/32834583/)[6](https://www.medrxiv.org/content/10.1101/2020.04.20.20072934v1)[7](https://www.sciencedirect.com/science/article/pii/S0048969721033830) have evaluated environmental factors such as temperature and humidity as sole important factors in their analysis of the COVID-19 pandemic. Since temperature was shown to be an influential contributing factor, we have added annual and seasonal temperatures averaged for the past 10 years expressed in degrees Celsius. The geographic and temperature data for each country was gathered from Berkeley Earth [8](http://berkeleyearth.org/data/) and The World Bank Group [9](https://climateknowledgeportal.worldbank.org/download-data). 

This data is used to provide additional contextual insight and potential factors that may contribute to the outcome of COVID-19 cases in each country. The data set contains 25 attributes which represent the above-mentioned country characteristics.

### COVID-19 data
Finally, country-wise COVID-19 mortality rates were used as the response variable for modeling dependencies in the data and explainable analysis of the importance and impacts of each feature in the specific tasks. The variable was represented in percentage of every country’s total population.

Regression and cluster analysis was performed on each of the subgroups of data individually and on the full data set containing all of the attributes. A comparison between the obtained results is given in the sections that follow.
