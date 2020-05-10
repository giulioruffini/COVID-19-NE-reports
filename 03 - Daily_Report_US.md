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

    Today's date: 2020-05-09 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  68



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 5/8/20
    - US fatalities to date: 77180
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 2511273
    Optimization terminated successfully.
             Current function value: 11766.882017
             Iterations: 110
             Function evaluations: 212
    Estimated parameters:
    N0: 16906
    beta0 (contacts per day): 0.4
    R0: 2.01
    
    Final loss: 11766
    Initial/Final % loss: 0.47
    Normalized Loss (per million persons, per day) 0.529 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 98.0
    Initially infected/Total population (N0/N): 16906/327200000 (5.2 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.5 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 3.4  days, Initial R0: 2.0
    Interventions:
      1/beta at day 12.0  = 3.8  days, R0 = 1.31
      1/beta at day 37.0  = 5.2  days, R0 = 0.96
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-05-09
       Infected: 3496688 (1.1%)
       Recovered: 38999825 (11.9%)
       Exposed to date: 42496513 (13.0%)
       In ICU: 8741
       Fatalities: 77999
     
    MEDIUM TERM FORECAST (98 days from model start date): 
       Percent of population exposed at end simulation: 16%
       Peak ICU admissions:  15526  on day 2020-04-19
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 103799



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-05-09 22:00:48.187844

