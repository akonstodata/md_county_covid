Analysis of county dynamics for COVID cases in Maryland
------------

INTRODUCTION
------------
The increase in COVID cases in a particular state will often be spread heterogeneously in that state: some counties will be experiencing tremendous growth, whereas others will not.  It will be helpful, then, to track dynamics of virus spread at the county level.  Below, we present results from a statistical model fit of counties in Maryland.  We hope this analysis will be complementary to the data provided by the MD Department of Health [[1]](https://coronavirus.maryland.gov/).  

We will be tracking which models fit cumulative growth the best: exponential, quadratic, or linear.  As the cumulative growth in positive cases slows, the growth function will shift from exponential to quadratic (concave up), and eventually to quadratic (concave down) and linear.  A switch to either of the latter two function types will indicate a substantial shift to slower growth dynamics, which is what we are looking and working for.

We show the crude CFR (case fatality rate), which is calculated as the number of deaths divided by the number of positive cases [[2]](https://en.wikipedia.org/wiki/Case_fatality_rate), for Maryland, and for each county where the positive case count exceeds 20 or the death count exceeds 1.  We include the percent positive cases as a function of the population for the state, as well as the counties.  We also include the percent positive cases and CFR for gender and race/ethnicity.

Contact: Anna Konstorum (konstorum.anna@gmail.com)

The Jupyter notebook for all updated results is found here [[3]](https://github.com/akonstodata/md_county_covid/blob/master/code/MD_COVID_Dynamics_model_choose_v2.ipynb).

CURRENT RESULTS
------------
Last update: 05/27/2020 8:00am EST

MARYLAND
------------

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_update.png)

------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_percent.png)
 
 ------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_county_stats.png)

 ------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_gender.png)
<sub> Note that while the positive percent for females is higher, CFR for males is higher.</sub>

 ------------
![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_types.png)
<sub> The low CFR for Hispanics coupled with a high positive proportion may indicate that this positive population represents a different distribution with respect to age or other attribute than other populations.  </sub>

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
MD Department of Health [[1]](https://coronavirus.maryland.gov/).  
The COVID Tracking Project [[4]](https://covidtracking.com/).    
U.S. Census (2019 population estimate for Maryland) [[5]](https://www.census.gov/quickfacts/fact/table/MD/PST045219#).  

REFERENCES and NOTES
------------
Case Fatality Risk Estimates from the CDC [[6]](https://wwwnc.cdc.gov/eid/article/26/6/20-0320_article).  

CityLab (04/03/2020) 'The Geography of Coronavirus' [[7]](https://www.citylab.com/equity/2020/04/coronavirus-spread-map-city-urban-density-suburbs-rural-data/609394/).    
Boston Globe (05/09/2020) 'A new analysis: Coronavirus death rate surged in Massachusetts locations that already faced challenges' [[8]](https://www.bostonglobe.com/2020/05/09/nation/disparities-push-coronavirus-death-rates-higher/?et_rid=1768511231).   
Baltimore Sun (05/12/2020) 'Latinos disproportionately hurt by coronavirus inMaryland, Baltimore and among Johns Hopkins patients' [[9]](https://www.baltimoresun.com/coronavirus/bs-md-covid-latinos-20200512-s3cjb6swbbfofmmfg7afmj3zw4-story.html).   

USAGE
------------
```
pipenv install
pipenv run jupyter notebook
```
