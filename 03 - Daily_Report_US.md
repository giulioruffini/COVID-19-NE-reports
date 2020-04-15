![](./images/logo.png)
# COVID19 Model - Daily Report US

---

**Neuroelectrics research team**  
March 2020  
* Main Author: G Ruffini and R Sanchez-Todo  
* Contributors: R Salvador, MC Biagi, E Lleal
* Curator: G Ruffini

---


```python
%matplotlib inline
from ne_epidemic.utilities import sir_prediction_from_country
sir_prediction_from_country('US')
```

    Today's date: 2020-04-14 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  43



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 4/14/20
    - US fatalities to date: 25757
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 1547315
    Optimization terminated successfully.
             Current function value: 3492.961795
             Iterations: 138
             Function evaluations: 253
    Estimated parameters:
    N0: 1748
    beta0 (contacts per day): 0.47
    R0: 2.37
    
    Final loss: 3492
    Initial/Final % loss: 0.23
    Normalized Loss (per million persons, per day) 0.243 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 73.0
    Initially infected/Total population (N0/N): 1748/327200000 (0.5 per 100,000)
    beta (per day): 0.5 , nu (per day): 0.2
    1/beta (days): 2.1 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 2.5  days, Initial R0: 2.4
    Interventions:
      1/beta at day 12.0  = 3.2  days, R0 = 1.55
      1/beta at day 37.0  = 4.4  days, R0 = 1.13
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-14
       Infected: 7312875 (2.2%)
       Recovered: 13594213 (4.2%)
       Exposed to date: 20907088 (6.4%)
       In ICU: 18282
       Fatalities: 27188
     
    MEDIUM TERM FORECAST (73 days from model start date): 
       Percent of population exposed at end simulation: 24%
       Peak ICU admissions:  27896  on day 2020-04-21
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 145481



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-14 22:00:17.523329

