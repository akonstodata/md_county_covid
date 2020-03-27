Analysis of county dynamics for COVID cases in Maryland
------------

INTRODUCTION
------------
The increase in COVID cases in a particular state will often be spread heterogenously in that state: some counties will be experiencing tremendous growth, whereas others will not.  It will be helpful, then, to track dynamics of virus spread at the county level.  Below, we present results from a statistical model fit of counties in Maryland.  We will be tracking which models fit cumulative growth the best: exponential, polynomial, or linear.  As virus growth spreads, the best model fit will veer away from exponential towards linear.  This is what we are looking for.

Contact: Anna Konstorum (konstorum.anna@gmail.com)

The Jupyter notebook for all updated results is found here [[1]](https://github.com/akonstodata/md_county_covid/blob/master/code/MD_COVID_Dynamics.ipynb)

CURRENT RESULTS
------------
Last update: 03/26/2020 8:00pm EST

MARYLAND
------------

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_update.png)

Prediction for number of total cases for 03/27 is 710

MARYLAND: three counties
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_3counties_update.png)

Prediction for number of cases for Montgomery county for 03/27 is 197.

Prediction for number of cases for Prince George's county for 03/27 is 120.

Prediction for number of cases for Anne Arundel county for 03/27 is 51. 

MARYLAND: Baltimore
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Baltimore_update.png)

Prediction for number of cases for Baltimore City for 03/27 is 97.

Prediction for number of cases for Baltimore County for 03/27 is 101. 

SOURCE DATA
------------
The COVID Tracking Project [[2]](https://covidtracking.com/).  
Earlier data from various news sources.


USAGE
------------
```
pipenv install
pipenv run jupyter notebook
```
