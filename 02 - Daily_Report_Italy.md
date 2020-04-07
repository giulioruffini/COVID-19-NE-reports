![](./images/logo.png)
# COVID19 Model - Daily Report Italy

---

**Neuroelectrics research team**  
March 2020  
Main Authors: G Ruffini and R Sanchez-Todo and MC Biagi

Curator: MC Biagi

Contributors: E Lleal

---


```python
%matplotlib inline
from ne_epidemic.utilities import sir_prediction_from_country
sir_prediction_from_country('Italy')
```

    Today's date: 2020-04-07 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  43



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 4/6/20
    - Italy fatalities to date: 16523
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    
    Fitting parameters N0 and beta
    Initial loss: 251598
    Optimization terminated successfully.
             Current function value: 899.185863
             Iterations: 79
             Function evaluations: 153
    Estimated parameters:
    N0: 26622
    beta0 (contacts per day): 0.38
    R0: 1.91
    
    Final loss: 899
    Initial/Final % loss: 0.36
    Normalized Loss (per million persons, per day) 0.346 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 64.0
    Initially infected/Total population (N0/N): 26622/60480000 (44.0 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.6 , 1/nu (days): 5.0
    IFR: 0.0016666666666666668
    Initial Doubling time: 3.8  days, Initial R0: 1.9
    Interventions:
      1/beta at day 13.0  = 4.0  days, R0 = 1.24
      1/beta at day 16.0  = 4.0  days, R0 = 1.24
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 6
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-07
       Infected: 2405945 (4.0%)
       Recovered: 10669114 (17.6%)
       Exposed to date: 13075059 (21.6%)
       In ICU: 3007
       Fatalities: 17781
     
    MEDIUM TERM FORECAST (64 days from model start date): 
       Percent of population exposed at end simulation: 34%
       Peak ICU admissions:  3026  on day 2020-04-04
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 31976



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-07 06:53:51.674822



```python

```


```python

```
