# Considering Bias in Data

## Goal
The objective of this project is to investigate the presence of bias in data, particularly in Wikipedia articles, focusing on articles about cities in various states of the United States. Through the amalgamation of a dataset containing Wikipedia articles and another dataset containing state populations, you will utilize the ORES machine learning service to gauge the quality of these city-based articles.

The task involves conducting an in-depth analysis of the representation of US cities on Wikipedia and the discrepancies in the quality of articles across different states. The analysis should be presented through a comprehensive set of tables showcasing the following information:

1. A comparison of the states with the most and least coverage of cities on Wikipedia relative to their respective populations.

2. Identification of the states with the highest and lowest proportion of high-quality articles about cities.

3. A ranking of US geographical regions based on articles per person and the proportion of high-quality articles.

## Data Source
### Wikipedia Data
This analysis consist multiple datasets from Wikipia API:
* The Wikipedia Category:Lists of cities in the United States by state was crawled to generate a list of Wikipedia article pages about US cities from each state. https://en.wikipedia.org/wiki/Category:Lists_of_cities_in_the_United_States_by_state
* ORES: machine learning system predicted quality scores for each article in the Wikipedia dataset. This data is retrieved by re-using following sample code by Dr. David W. McDonald: https://github.com/aprilggg/data-512-homework_2/blob/main/wp_page_info_example.ipynb, https://github.com/aprilggg/data-512-homework_2/blob/main/wp_ores_liftwing_example.ipynb. This code is licensed CC-BY: https://creativecommons.org/licenses/by/4.0/

### Population and Region Data
* The US Census Bureau provides updated population estimates for every US state. I will be using the file contains estimated populations of all US states for 2022: https://www.census.gov/data/tables/time-series/demo/popest/2020s-state-total.html 
* The 'region' demarcation within the US is not one standardized and fixed thing. For this analysis, you will use the regional and divisional agglomerations as defined by the US Census Bureau: https://docs.google.com/spreadsheets/d/14Sjfd_u_7N9SSyQ7bmxfebF_2XpR8QamvmNntKDIQB0/edit?usp=sharing

## Output Tables
After processing the data, I have stored the dataset intended for analysis under the name 'wp_scored_city_articles_by_state.csv'. This file includes the following attributes:

* state: Included 48 states in the United States.
* regional_division: The division to which each state belongs, as per the US Census Bureau's classification.
* population: The population of each state, obtained from the 'POPESTIMATE2022' attribute.
* article_title: The title of the Wikipedia page corresponding to each city, along with its respective state.
* revision_id: The revision ID obtained from the Wikipedia API during the retrieval process.
* article_quality: The predicted article quality score assigned by the ORES model.

## Research Implications

