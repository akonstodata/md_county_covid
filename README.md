Analysis of county dynamics for COVID cases in Maryland
------------

INTRODUCTION
------------
The increase in COVID cases in a particular state will often be spread heterogeniously in that state: some counties will be experiencing tremendous growth, whereas others will not.  It will be helpful, then, to track dynamics of virus spread at the county level.  Below, we present results from a statistical model fit of counties in Maryland.  We will be tracking which models fit cumulative growth the best: exponential, quadratic, or linear.  As the cumulative growth in positive cases slows, the growth function will shift from exponential to quadratic (concave up), and eventually to quadratic (concave down) and linear.  A switch to either of the latter two function types will indicate a substantial shift to slower growth dynamics, which is what we are looking and working for.

We show the crude CFR (case fatality rate), which is calculated as the number of deaths divided by the number of positive cases, for Maryland, and for each county where the positive case count exceeds 20 or the death count exceeds 1.  We include the percent positive cases as a function of the population for the state, as well as the counties.  We also include the percent positive cases and CFR as a function of gender, and will include these attributes as a function of ethnicity and age shortly.

Contact: Anna Konstorum (konstorum.anna@gmail.com)

The Jupyter notebook for all updated results is found here [[1]](https://github.com/akonstodata/md_county_covid/blob/master/code/MD_COVID_Dynamics_model_choose.ipynb)

CURRENT RESULTS
------------
Last update: 04/19/2020 5:00pm EST

MARYLAND
------------

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_update.png)
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_percent.png)
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_county_stats.png)
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_gender.png)

MARYLAND: Montgomery and Prince George's Counties
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Mont_Prince_update.png)

MARYLAND: Howard and Anne Arundel Counties
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Howard_AA_update.png)

MARYLAND: Baltimore
------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_Baltimore_update.png)

SOURCE DATA
------------
The COVID Tracking Project [[2]](https://covidtracking.com/).  
U.S. Census[[3]](https://census.gov/).
Earlier data from various news sources.


USAGE
------------
```
pipenv install
pipenv run jupyter notebook
```
