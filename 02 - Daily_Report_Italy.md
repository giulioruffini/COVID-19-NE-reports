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

    Today's date: 2020-05-24 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  90



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 5/23/20
    - Italy fatalities to date: 32735
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  14
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    day since start simulation: 27  => beta reduction factor: 0.61
    
    Fitting parameters N0 and beta
    Initial loss: 482296
    Optimization terminated successfully.
             Current function value: 2464.618110
             Iterations: 83
             Function evaluations: 156
    Estimated parameters:
    N0: 39313
    beta0 (contacts per day): 0.36
    R0: 1.78
    
    Final loss: 2464
    Initial/Final % loss: 0.51
    Normalized Loss (per million persons, per day) 0.453 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 111.0
    Initially infected/Total population (N0/N): 39313/60480000 (65.0 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.8 , 1/nu (days): 5.0
    IFR: 0.0016666666666666668
    Initial Doubling time: 4.4  days, Initial R0: 1.8
    Interventions:
      1/beta at day 13.0  = 4.3  days, R0 = 1.16
      1/beta at day 16.0  = 4.3  days, R0 = 1.16
      1/beta at day 27.0  = 4.6  days, R0 = 1.09
    Latency for intervention effect on fatalities (days): 14
    Infected_to_Detected_ratio: 6
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-05-24
       Infected: 265619 (0.4%)
       Recovered: 19398311 (32.1%)
       Exposed to date: 19663930 (32.5%)
       In ICU: 332
       Fatalities: 32330
     
    MEDIUM TERM FORECAST (111 days from model start date): 
       Percent of population exposed at end simulation: 33%
       Peak ICU admissions:  2860  on day 2020-03-28
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 33448



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-05-24 22:00:08.873689



```python

```
