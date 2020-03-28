Analysis of county dynamics for COVID cases in Maryland
------------

INTRODUCTION
------------
The increase in COVID cases in a particular state will often be spread heterogenously in that state: some counties will be experiencing tremendous growth, whereas others will not.  It will be helpful, then, to track dynamics of virus spread at the county level.  Below, we present results from a statistical model fit of counties in Maryland.  We will be tracking which models fit cumulative growth the best: exponential, polynomial, or linear.  As virus growth spreads, the best model fit will veer away from exponential towards linear.  This is what we are looking for.

Contact: Anna Konstorum (konstorum.anna@gmail.com)

The Jupyter notebook for all updated results is found here [[1]](https://github.com/akonstodata/md_county_covid/blob/master/code/MD_COVID_Dynamics.ipynb)

CURRENT RESULTS
------------
Last update: 03/28/2020 10:00am EST

MARYLAND
------------

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_update.png)

The best model for Maryland is the exponential model.  Prediction for number of total cases for 03/28 is 993.

MARYLAND: Montgomery and Prince George's Counties
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Mont_Prince_update.png)

The best model for Montgomery is the exponential model.  Prediction for number of total cases for 03/28 is 247.  

The best model for Prince Georges is the exponential model.  Prediction for number of total cases for 03/28 is 203.   

MARYLAND: Howard and Anne Arundel Counties
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Howard_AA_update.png)

The best model for Howard is the exponential model.  Prediction for number of total cases for 03/28 is 78.

The best model for Anne Arundel is the exponential model.  Prediction for number of total cases for 03/28 is 82.

MARYLAND: Baltimore
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Baltimore_update.png)

The best model for Baltimore City is the exponential model.  Prediction for number of total cases for 03/28 is 113.

The best model for Baltimore County is the exponential model.  Prediction for number of total cases for 03/28 is 140.

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
