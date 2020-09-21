Analysis of county dynamics for COVID cases in Maryland
------------

INTRODUCTION
------------
The increase in COVID cases in a particular state will often be spread heterogeneously in that state along socioeconomic boundaries and other factors (such as age, gender, etc.).  It will be helpful, then, to track dynamics of virus spread while incorporating these factors in order to ascertain potentially sensitive groups and regions.  Below, we present results from a statistical model fit of COVID dynamics in Maryland.  We hope this analysis will be complementary to the data provided by the MD Department of Health [[MD Health Dept]](https://coronavirus.maryland.gov/).  

We will be tracking which models fit cumulative growth the best: exponential, quadratic, or linear.  As the cumulative growth in positive cases slows, the growth function will shift from exponential to quadratic (concave up), and eventually to quadratic (concave down) and linear.  A switch to either of the latter two function types will indicate a substantial shift to slower growth dynamics, which is what we are looking and working for.

We include in our analysis the crude CFR (case fatality rate), which is calculated as the number of deaths divided by the number of positive cases [[CDC CFR]](https://en.wikipedia.org/wiki/Case_fatality_rate).  As can be observed below, the CFR can give an indication of which groups and regions may be most vulnerable to COVID.

Contact: Anna Konstorum (konstorum.anna@gmail.com)

The Jupyter notebook for all updated results is found here [[source_code]](https://github.com/akonstodata/md_county_covid/blob/master/code/MD_COVID_Dynamics_model_choose_v3.ipynb).

CURRENT RESULTS
------------
Last update: 09/20/2020 

MARYLAND COVID DYNAMICS OVERVIEW
------------
We begin with a plot of cumulative COVID cases and hospitalizations for Maryland.  The predictions are based on a model fit to the last ten days of the data. 

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_model.png)

We also include a visualization of the historical model type: red indicates an exponential model, orange a quadratic (up) model, and green a quadratic (down) or linear model.  Note that the models start off in red/orange territory, and by mid-April are in orange/green territory.

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_COVID_models.png)

<sub> We will include shortly milestone events in Marlyand with respect to closures and re-openings as an overlay for the graph </sub>


MARYLAND COVID DYNAMICS: RACE/ETHNICITY
------------
We consider cumulative COVID cases for African American, Asian, Hispanic, and White races/ethnicities in proportion to the population of these groups in Maryland.  We also track the crude Case Fatality Rate for each race/ethnicity.
 
 ![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_race.png)
 
We observe that while the Hispanic population has the largest case load with respect to their population, they have the lowest CFR.  While MD does not release age-by-race data, we hypothesize that this phenomenon can be explained by the average age of a COVID-positive Hispanic patient to be much lower than for another race.  Hispanics make up a large proportion of essential workers in Maryland, which would increase exposure for individuals of working age [[BaltimoreSun05122020]](https://www.baltimoresun.com/coronavirus/bs-md-covid-latinos-20200512-s3cjb6swbbfofmmfg7afmj3zw4-story.html).   
 
 The second observation is that the CFR for all races/ethnicities except for Hispanics tends to increase, then decrease with time (with the highest rate found in Asian and White populations).  We surmise that this is due to a higher case load in older White and Asian populations relative to other races/ethnicities, especially in the early stages of the pandemic.  The subsequent decrease in CFRs could be explained by a rise in case-load of younger populations, which would decrease the CFR.  In the next section, we will see this is indeed the case. 
 
MARYLAND COVID DYNAMICS: AGE
------------

We now consider the age distribution of COVID cases in Maryland (first two panels, each line represents the percent of cases attributed to that age group at that time), and the CFR for each age group.

![](https://github.com/akonstodata/md_county_covid/blob/master/results/MD_age.png)

There are many interesting points to observe here.  While the 50-69 age group tends to have the highest percent of cases (which is decreasing), we also see that the oldest age group (70+) has a high peak early in the pandemic (which may correspond to spread in nursing homes), followed by a decline.  While the older age groups are declining, we see an increase in the younger age groups over time, the fastest increase is in the 20-29 age group, which could be attributed to social gatherings post reopening.  We also begin to see a steeper increase in the 10-19 age group after September 2020, most likely due to school reopenings.

Note also the large difference in CFR in the age groups: the 70+ age group has a very high CFR  of > 3.0 that continues to grow (which can be explained by a slower growth in cases than deaths), whereas the 50-to-69 age group peaks at 0.5 CFR, and the rest of the age groups are below 0.25 CFR.  If we consider these results alongside the earlier CFR results for different races/ethnicities, we can more confidently hypothesize that all but Hispanic races/ethnicities are showing a decline in CFRs due to a decrease in the age distribution of COVID positive cases.  We can also surmise that the races/ethnicities with the oldest populations of positive patients are Asian and White populations, which again can be attributed to socioeconomic stratification.


COMING SOON: ANALYSIS BY COUNTY
------------

We have already seen how simple analyses can bring insights into the disparate impact of COVID on different populations in Maryland.  We will continue this analysis by looking at county dynamics.  Counties show very different rates of positivity and CFRs, and we will use what we have learned so far in the current analysis to better understand why.



SOURCE DATA
------------
MD Department of Health Datasets [[MD Health Dept Datasets]](https://coronavirus.maryland.gov/https://coronavirus.maryland.gov/datasets/).  
U.S. Census (2019 population estimate for Maryland) [[U.S. Census]](https://www.census.gov/quickfacts/fact/table/MD/PST045219#).  

REFERENCES and NOTES
------------
Case Fatality Risk Estimates from the CDC [[CDC CFR]](https://wwwnc.cdc.gov/eid/article/26/6/20-0320_article).  

CityLab (04/03/2020) 'The Geography of Coronavirus' [[CityLab Geo]](https://www.citylab.com/equity/2020/04/coronavirus-spread-map-city-urban-density-suburbs-rural-data/609394/).    
Boston Globe (05/09/2020) 'A new analysis: Coronavirus death rate surged in Massachusetts locations that already faced challenges' [[BostonGlobe05092020]](https://www.bostonglobe.com/2020/05/09/nation/disparities-push-coronavirus-death-rates-higher/?et_rid=1768511231).   
Baltimore Sun (05/12/2020) 'Latinos disproportionately hurt by coronavirus in
Maryland, Baltimore and among Johns Hopkins patients' [[BaltimoreSun05122020]](https://www.baltimoresun.com/coronavirus/bs-md-covid-latinos-20200512-s3cjb6swbbfofmmfg7afmj3zw4-story.html).   
[More updated references coming soon!]

USAGE
------------
```
pipenv install
pipenv run jupyter notebook
```
