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

    Today's date: 2020-04-18 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  54



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 4/17/20
    - Italy fatalities to date: 22745
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  7
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    day since start simulation: 27  => beta reduction factor: 0.46
    
    Fitting parameters N0 and beta
    Initial loss: 286098
    Optimization terminated successfully.
             Current function value: 1000.715076
             Iterations: 83
             Function evaluations: 161
    Estimated parameters:
    N0: 13263
    beta0 (contacts per day): 0.43
    R0: 2.14
    
    Final loss: 1000
    Initial/Final % loss: 0.35
    Normalized Loss (per million persons, per day) 0.306 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 75.0
    Initially infected/Total population (N0/N): 13263/60480000 (21.9 per 100,000)
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
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-18
       Infected: 1105664 (1.8%)
       Recovered: 13604478 (22.5%)
       Exposed to date: 14710142 (24.3%)
       In ICU: 1382
       Fatalities: 22674
     
    MEDIUM TERM FORECAST (75 days from model start date): 
       Percent of population exposed at end simulation: 27%
       Peak ICU admissions:  3263  on day 2020-03-29
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 27320



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-18 21:59:57.571399



```python

```
