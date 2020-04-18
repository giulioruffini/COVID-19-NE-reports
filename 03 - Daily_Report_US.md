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

    Today's date: 2020-04-17 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  46



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 4/17/20
    - US fatalities to date: 36773
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 1702885
    Optimization terminated successfully.
             Current function value: 3818.838366
             Iterations: 134
             Function evaluations: 250
    Estimated parameters:
    N0: 1951
    beta0 (contacts per day): 0.47
    R0: 2.35
    
    Final loss: 3818
    Initial/Final % loss: 0.22
    Normalized Loss (per million persons, per day) 0.248 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 76.0
    Initially infected/Total population (N0/N): 1951/327200000 (0.6 per 100,000)
    beta (per day): 0.5 , nu (per day): 0.2
    1/beta (days): 2.1 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 2.6  days, Initial R0: 2.4
    Interventions:
      1/beta at day 12.0  = 3.3  days, R0 = 1.53
      1/beta at day 37.0  = 4.4  days, R0 = 1.12
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-17
       Infected: 9102097 (2.8%)
       Recovered: 18219122 (5.6%)
       Exposed to date: 27321219 (8.4%)
       In ICU: 22755
       Fatalities: 36438
     
    MEDIUM TERM FORECAST (76 days from model start date): 
       Percent of population exposed at end simulation: 24%
       Peak ICU admissions:  26673  on day 2020-04-20
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 148300



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-17 22:00:22.837776

