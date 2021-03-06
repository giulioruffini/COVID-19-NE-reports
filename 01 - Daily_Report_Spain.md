![](./images/logo.png)
# COVID19 Model - Daily Report Spain

---

**Neuroelectrics research team**  
March 2020  
* Main Author: G Ruffini and R Sanchez-Todo  
* Contributors: R Salvador, MC Biagi, E Lleal
* Curator: G. Ruffini

---

### This report focuses on modeling fatalites, and hence reflects infection dynamics 1-2 weeks ago


```python
%matplotlib inline
from ne_epidemic.utilities import sir_prediction_from_country
sir_prediction_from_country('Spain')
```

    Today's date: 2020-06-24 
    
    Country:  Spain
    - UCI database:  https://raw.githubusercontent.com/datadista/datasets/master/COVID%2019/ccaa_camas_uci_2017.csv
    - Total UCI beds:  4404
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  109



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_1.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_2.png)


    - Last day with data: 6/23/20
    - Spain fatalities to date: 28325
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-07
    - Infection to death latency (days):  13
    
    Intervention list:
    day since start simulation: 7  => beta reduction factor: 0.52
    day since start simulation: 24  => beta reduction factor: 0.48
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 1879011
    Optimization terminated successfully.
             Current function value: 7728.067056
             Iterations: 79
             Function evaluations: 156
    Estimated parameters:
    N0: 28905
    beta0 (contacts per day): 0.34
    R0: 1.69
    
    Final loss: 7728
    Initial/Final % loss: 0.41
    Normalized Loss (per million persons, per day) 1.519 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 169.0
    Initially infected/Total population (N0/N): 28905/46660000 (61.9 per 100,000)
    beta (per day): 0.3 , nu (per day): 0.2
    1/beta (days): 3.0 , 1/nu (days): 5.0
    IFR: 0.01
    Initial Doubling time: 5.0  days, Initial R0: 1.7
    Interventions:
      1/beta at day 7.0  = 5.7  days, R0 = 0.88
      1/beta at day 24.0  = 6.2  days, R0 = 0.81
      1/beta at day 37.0  = 6.2  days, R0 = 0.81
    Latency for intervention effect on fatalities (days): 13
    Infected_to_Detected_ratio: 1
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-06-24
       Infected: 8441 (0.0%)
       Recovered: 2847721 (6.1%)
       Exposed to date: 2856162 (6.1%)
       In ICU: 118
       Fatalities: 28477
     
    MEDIUM TERM FORECAST (169 days from model start date): 
       Percent of population exposed at end simulation: 6%
       Peak ICU admissions:  6079  on day 2020-03-27
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 28806



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_4.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_5.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_6.png)


     



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-06-24 21:59:55.031976

