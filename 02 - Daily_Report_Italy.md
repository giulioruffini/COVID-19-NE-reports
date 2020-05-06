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

    Today's date: 2020-05-05 
    
    Country:  Italy
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  71



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_1.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_2.png)


    - Last day with data: 5/5/20
    - Italy fatalities to date: 29315
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-02-24
    - Infection to death latency (days):  14
    
    Intervention list:
    day since start simulation: 13  => beta reduction factor: 0.65
    day since start simulation: 16  => beta reduction factor: 0.65
    day since start simulation: 27  => beta reduction factor: 0.61
    
    Fitting parameters N0 and beta
    Initial loss: 422356
    Optimization terminated successfully.
             Current function value: 1671.054878
             Iterations: 81
             Function evaluations: 154
    Estimated parameters:
    N0: 43540
    beta0 (contacts per day): 0.35
    R0: 1.77
    
    Final loss: 1671
    Initial/Final % loss: 0.4
    Normalized Loss (per million persons, per day) 0.384 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 92.0
    Initially infected/Total population (N0/N): 43540/60480000 (72.0 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.8 , 1/nu (days): 5.0
    IFR: 0.0016666666666666668
    Initial Doubling time: 4.5  days, Initial R0: 1.8
    Interventions:
      1/beta at day 13.0  = 4.3  days, R0 = 1.15
      1/beta at day 16.0  = 4.3  days, R0 = 1.15
      1/beta at day 27.0  = 4.6  days, R0 = 1.08
    Latency for intervention effect on fatalities (days): 14
    Infected_to_Detected_ratio: 6
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-05-05
       Infected: 661715 (1.1%)
       Recovered: 17459248 (28.9%)
       Exposed to date: 18120963 (30.0%)
       In ICU: 827
       Fatalities: 29098
     
    MEDIUM TERM FORECAST (92 days from model start date): 
       Percent of population exposed at end simulation: 32%
       Peak ICU admissions:  2846  on day 2020-03-27
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 31959



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_4.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_5.png)



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_6.png)


     



![png](02%20-%20Daily_Report_Italy_files/02%20-%20Daily_Report_Italy_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-05-05 23:51:41.955674



```python

```
