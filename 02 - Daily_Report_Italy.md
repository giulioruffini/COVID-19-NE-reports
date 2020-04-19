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

    Today's date: 2020-04-19 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  55



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 4/18/20
    - Italy fatalities to date: 23227
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  7
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    day since start simulation: 27  => beta reduction factor: 0.46
    
    Fitting parameters N0 and beta
    Initial loss: 290801
    Optimization terminated successfully.
             Current function value: 1126.226022
             Iterations: 91
             Function evaluations: 173
    Estimated parameters:
    N0: 12963
    beta0 (contacts per day): 0.43
    R0: 2.15
    
    Final loss: 1126
    Initial/Final % loss: 0.39
    Normalized Loss (per million persons, per day) 0.339 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 76.0
    Initially infected/Total population (N0/N): 12963/60480000 (21.4 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.3 , 1/nu (days): 5.0
    IFR: 0.0016666666666666668
    Initial Doubling time: 3.0  days, Initial R0: 2.1
    Interventions:
      1/beta at day 13.0  = 3.6  days, R0 = 1.4
      1/beta at day 16.0  = 3.6  days, R0 = 1.4
      1/beta at day 27.0  = 5.1  days, R0 = 0.99
    Latency for intervention effect on fatalities (days): 7
    Infected_to_Detected_ratio: 6
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-19
       Infected: 1060080 (1.8%)
       Recovered: 13864034 (22.9%)
       Exposed to date: 14924114 (24.7%)
       In ICU: 1325
       Fatalities: 23106
     
    MEDIUM TERM FORECAST (76 days from model start date): 
       Percent of population exposed at end simulation: 27%
       Peak ICU admissions:  3277  on day 2020-03-29
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 27551



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-19 12:12:56.598990



```python

```
