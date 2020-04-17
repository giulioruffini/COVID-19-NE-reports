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

    Today's date: 2020-04-16 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  45



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 4/16/20
    - US fatalities to date: 32917
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 1652785
    Optimization terminated successfully.
             Current function value: 3795.490701
             Iterations: 139
             Function evaluations: 267
    Estimated parameters:
    N0: 2022
    beta0 (contacts per day): 0.47
    R0: 2.34
    
    Final loss: 3795
    Initial/Final % loss: 0.23
    Normalized Loss (per million persons, per day) 0.252 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 75.0
    Initially infected/Total population (N0/N): 2022/327200000 (0.6 per 100,000)
    beta (per day): 0.5 , nu (per day): 0.2
    1/beta (days): 2.1 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 2.6  days, Initial R0: 2.3
    Interventions:
      1/beta at day 12.0  = 3.3  days, R0 = 1.53
      1/beta at day 37.0  = 4.5  days, R0 = 1.12
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-16
       Infected: 8294041 (2.5%)
       Recovered: 16395694 (5.0%)
       Exposed to date: 24689735 (7.5%)
       In ICU: 20735
       Fatalities: 32791
     
    MEDIUM TERM FORECAST (75 days from model start date): 
       Percent of population exposed at end simulation: 24%
       Peak ICU admissions:  26331  on day 2020-04-20
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 143803



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-16 22:00:16.756205

