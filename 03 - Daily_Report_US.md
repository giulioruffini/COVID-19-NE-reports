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

    Today's date: 2020-04-27 
    
    Country:  US
    - UCI database:  https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19
    - Total UCI beds:  96596
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  56



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_1.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_2.png)


    - Last day with data: 4/26/20
    - US fatalities to date: 54881
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-02
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 12  => beta reduction factor: 0.65
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 2102590
    Optimization terminated successfully.
             Current function value: 9994.814364
             Iterations: 123
             Function evaluations: 236
    Estimated parameters:
    N0: 6281
    beta0 (contacts per day): 0.43
    R0: 2.15
    
    Final loss: 9994
    Initial/Final % loss: 0.48
    Normalized Loss (per million persons, per day) 0.545 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 86.0
    Initially infected/Total population (N0/N): 6281/327200000 (1.9 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.3 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 3.0  days, Initial R0: 2.2
    Interventions:
      1/beta at day 12.0  = 3.6  days, R0 = 1.4
      1/beta at day 37.0  = 4.9  days, R0 = 1.03
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-27
       Infected: 6630617 (2.0%)
       Recovered: 30490399 (9.3%)
       Exposed to date: 37121016 (11.3%)
       In ICU: 16576
       Fatalities: 60980
     
    MEDIUM TERM FORECAST (86 days from model start date): 
       Percent of population exposed at end simulation: 18%
       Peak ICU admissions:  18578  on day 2020-04-19
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 118053



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_4.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_5.png)



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_6.png)


     



![png](03%20-%20Daily_Report_US_files/03%20-%20Daily_Report_US_1_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-27 22:00:21.444340

