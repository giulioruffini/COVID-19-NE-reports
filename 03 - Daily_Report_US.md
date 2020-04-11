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

    Today's date: 2020-04-10 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  39



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 4/10/20
    - US fatalities to date: 18586
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 1318804
    Optimization terminated successfully.
             Current function value: 1149.390473
             Iterations: 147
             Function evaluations: 281
    Estimated parameters:
    N0: 611
    beta0 (contacts per day): 0.51
    R0: 2.57
    
    Final loss: 1149
    Initial/Final % loss: 0.09
    Normalized Loss (per million persons, per day) 0.088 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 69.0
    Initially infected/Total population (N0/N): 611/327200000 (0.2 per 100,000)
    beta (per day): 0.5 , nu (per day): 0.2
    1/beta (days): 1.9 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 2.2  days, Initial R0: 2.6
    Interventions:
      1/beta at day 12.0  = 3.0  days, R0 = 1.67
      1/beta at day 37.0  = 4.1  days, R0 = 1.23
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-10
       Infected: 6486362 (2.0%)
       Recovered: 9512229 (2.9%)
       Exposed to date: 15998591 (4.9%)
       In ICU: 16215
       Fatalities: 19024
     
    MEDIUM TERM FORECAST (69 days from model start date): 
       Percent of population exposed at end simulation: 32%
       Peak ICU admissions:  42760  on day 2020-04-23
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 190447



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-10 22:00:31.827007

