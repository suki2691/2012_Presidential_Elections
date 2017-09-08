# 2012_Presidential_Elections
## Predicting the outcome of the 2012 elections at county level based on county attributes

Predicted whether a county voted for the Democratic or the Republican presidential candidate during the 2012 Presidential Elections. 

## Data sources-
- [County level election results](https://www.theguardian.com/news/datablog/2012/nov/07/us-2012-election-county-results-download#data)
- [US Census Bureau](https://www.census.gov/)
- [Center for Disease Control](https://www.cdc.gov/)
- [Bureau of Alcohol, Tobacco, Firearms and Explosives](https://www.atf.gov/)

## Features-
The main motivation behind many of the features were the common stereotypes of a typical Democrat and Republican voter, like-
- Number of Labor unions per county
- Number of Starbucks stores per county
- Number of gun stores per county
- Overall county health statistics - heart disease deaths, diabetes %, physical inactivity %, obesity %
- [County Business Patterns](https://www.census.gov/programs-surveys/cbp.html)
- Unemployment statistics
- Poverty statistics
- Migration- Domestic and International migration statistics
- General county demographics- race, median age

## Methodology-
- Determined the winner based on the votes. Party of the candidate with the highest number of votes won the county
- Alaska has boroughs instead of counties. The elections results were not available at borough level, so I assigned the state results to each of the boroughs (Mitt Romney won Alaska in 2012)
- To make it a binary classification problem, I changed the winning party to **Is Democrat** - ( 1 if the county voted Democrat, 0 otherwise)
- No county had voted for an Independent candidate
- It was an imbalanced class problem, with the Democrats winning around 600 counties out of a possible 3139 counties
- Identified each county for all the data tables using the county [FIPS code](https://www.census.gov/geo/reference/codes/cou.html)
- Joined all the data tables on the FIPS code
- Tried out a few classifiers to see which one accurately predicted the results. Gradient boosting algorithm won, with an accuracy of 88%

_Currently in the process of obtaining more attributes, feature engineering and improving model performance_

