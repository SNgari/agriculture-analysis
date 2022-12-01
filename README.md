# Agricultural Data Analysis

An analysis of agriculture-related metrics for a number of countries for the years 2000 & 2005 from the [Systema Globalis Dataset](https://github.com/open-numbers/ddf--gapminder--systema_globalis/tree/master/countries-etc-datapoints).

## Files in Repo

1. [The analysis notebook](ag_project.ipynb).

## Table of Contents
- [Background](#background)
- [Dataset](#dataset)
- [Libraries](#libraries)
- [Summary of Process](#summary-of-process)
- [Key Insights](#key-insights)

## Background
##### This project was the first of the projects in Udacity's Data Analyst Nano Degree
Food is an important part of every life. Without it, we wouldn't have the energy to pursue our dreams and goals. But how does food production relate to the general wellness of nations? How does the agricultural industry affect important factors such as GDP, employment, food supply to its citizens, and land usage? In this project, I look at these variables and investigate how they vary from country to country across the globe.

## Dataset
The datasets used were from Systema Globalis. They contain the progression of variables in different countries across the years. The variables selected for this project were:
+ [Land area under agricultural use (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--agricultural_land_percent_of_land_area--by--geo--time.csv)
+ [Daily food supply per person per day (kcal)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--food_supply_kilocalories_per_person_and_day--by--geo--time.csv)
+ [Agricultural GDP (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--agriculture_percent_of_gdp--by--geo--time.csv)
+ [Female Agricultural workers (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--female_agriculture_workers_percent_of_female_employment--by--geo--time.csv)
+ [Male Agricultural workers (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--male_agriculture_workers_percent_of_male_employment--by--geo--time.csv)
+ [Agricultural water usage (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--agricultural_water_withdrawal_percent_of_total--by--geo--time.csv)
+ [Total Agricultural workers (%)](https://raw.githubusercontent.com/open-numbers/ddf--gapminder--systema_globalis/master/countries-etc-datapoints/ddf--datapoints--agriculture_workers_percent_of_employment--by--geo--time.csv)

All variables with a `%` represent the agricultural portion of the variable from the whole nation's total of the variable. For example, `female agricultural workers` is a measure of female workers in agriculture as a percentage of female workers across all other industries in the given country.
 
## Libraries
The analysis was done in Jupyter Notebook. The libraries used were:  
| | |
|--- |---|
| Pandas | Numpy 
|Seaborn |Matplotlib pyplot|
|Functools||
## Summary of Process
1. Gathering - gathering and merging the different datasets
2. Cleaning - selecting datsets from 2000 & 2005 only and tidying up the data
3. Analyzing:  
In this section, I sought to figure out:
> - The top & bottom 5 countries by each of the metrics 
> - The countries that didn't meet the minimum recommended daily food supply per person> - How the other variables affect daily food supply 
> - Which countries saw the highest increase in land area, GDP, ag workers, and food supply within the 5-year gap between 2000 and 2005

## Key Insights
### Top & Bottom Fives
+ Many of the countries that have agriculture taking up huge proportions of their land, gdp, and employment struggle to provide their citizens with the minimum recommended daily food supply. Exceptions were Lebanon and Ukraine which topped the list in daily food supply.

+ Countries that grew 'thirsty' crops (eg. rice and sugarcane) spent large amounts of water that at first glance seemed disproportionate to the agricultural land area.
+ Developed countries like USA and UAE topped in daily food supply despite not allocating as much to agriculture percentagewise.

### Minimum daily food supply per person.
+ Yemen, Sierra Leone, and Angola were unable to cross over the minimum value (2250 kcal) within the 5-year gap (2000-2005)
> #### Disclaimer:
>This doesn't mean that they were the only ones. Our data didn't give information on all our variables of interest from all countries of the world.
There were some gaps in our data that led to the exclusion of data from other countries. An example is that not all the countries in our initial 2000 data were in the 2005 data.

### How daily food supply relates to the other 6 variables
+ Land area under agriculture had a slight positive relationship to daily food supply. This however, was among developing countries.
+ GDP, and agricultural employment had a negative relationship with daily food supply
+ Water usage had no effect on daily food supply in 2000, but a somewhat negative relationship in 2005
### 2000 Vs 2005 increase in land, employment, GDP, and food supply
+ Land Area: 
Sierra Leone and Angola were the only coutries that increased in land area under agriculture.
+ GDP: Nigeria and the Dominican Republic were the only ones to see an increase in the share of agriculture to their GDPs
+ Ag Workers: Angola and Ecuador were the only countries that saw increase in the proportion of ag workers
+ Daily food supply: All the countries in the top 5 list had an increase in food supply.

### Special Note:
+ A country worth noting is Sierra Leone. It's 13% increase in land area under agriculture only accounted for 4.62% increase in daily food supply. Sierra Leone was also one of the countries that were unable to meet the minimum recommended daily food supply in 2005.

+ Angola is another country worth noting. A 2% increase in land area under agriculture led to a 15.9% increase in daily food supply. Perhaps Sierra Leone should learn a bit from Angola. Angola, however, suffers the same problem as Sierra Leone in that despite their increases in daily food supply, they weren't able to provide the minimum daily recommended food supply of 2250kcal in 2005.
