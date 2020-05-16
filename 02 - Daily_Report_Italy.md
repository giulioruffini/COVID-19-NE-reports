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

    Today's date: 2020-05-15 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  81



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 5/14/20
    - Italy fatalities to date: 31368
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  14
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    day since start simulation: 27  => beta reduction factor: 0.61
    
    Fitting parameters N0 and beta
    Initial loss: 454201
    Optimization terminated successfully.
             Current function value: 2007.860791
             Iterations: 75
             Function evaluations: 144
    Estimated parameters:
    N0: 41362
    beta0 (contacts per day): 0.35
    R0: 1.77
    
    Final loss: 2007
    Initial/Final % loss: 0.44
    Normalized Loss (per million persons, per day) 0.41 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 102.0
    Initially infected/Total population (N0/N): 41362/60480000 (68.4 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.8 , 1/nu (days): 5.0
    IFR: 0.0016666666666666668
    Initial Doubling time: 4.5  days, Initial R0: 1.8
    Interventions:
      1/beta at day 13.0  = 4.3  days, R0 = 1.16
      1/beta at day 16.0  = 4.3  days, R0 = 1.16
      1/beta at day 27.0  = 4.6  days, R0 = 1.09
    Latency for intervention effect on fatalities (days): 14
    Infected_to_Detected_ratio: 6
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-05-15
       Infected: 412547 (0.7%)
       Recovered: 18655673 (30.8%)
       Exposed to date: 19068220 (31.5%)
       In ICU: 515
       Fatalities: 31092
     
    MEDIUM TERM FORECAST (102 days from model start date): 
       Percent of population exposed at end simulation: 32%
       Peak ICU admissions:  2854  on day 2020-03-28
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 32845



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-05-15 22:00:23.235343



```python

```
