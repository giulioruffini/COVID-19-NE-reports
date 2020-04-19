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

    Today's date: 2020-04-18 
    
    Country:  Spain
    - UCI database:  https://raw.githubusercontent.com/datadista/datasets/master/COVID%2019/ccaa_camas_uci_2017.csv
    - Total UCI beds:  4404
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  42



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_1.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_2.png)


    - Last day with data: 4/17/20
    - Spain fatalities to date: 20002
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-07
    - Infection to death latency (days):  12
    
    Intervention list:
    day since start simulation: 7  => beta reduction factor: 0.48
    day since start simulation: 24  => beta reduction factor: 0.22
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 59355
    Optimization terminated successfully.
             Current function value: 782.633045
             Iterations: 66
             Function evaluations: 133
    Estimated parameters:
    N0: 31458
    beta0 (contacts per day): 0.43
    R0: 2.17
    
    Final loss: 782
    Initial/Final % loss: 1.32
    Normalized Loss (per million persons, per day) 0.399 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 102.0
    Initially infected/Total population (N0/N): 31458/46660000 (67.4 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.3 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 3.0  days, Initial R0: 2.2
    Interventions:
      1/beta at day 7.0  = 4.8  days, R0 = 1.04
      1/beta at day 24.0  = 10.6  days, R0 = 0.47
      1/beta at day 37.0  = 4.8  days, R0 = 1.04
    Latency for intervention effect on fatalities (days): 12
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-18
       Infected: 692346 (1.5%)
       Recovered: 9900419 (21.2%)
       Exposed to date: 10592765 (22.7%)
       In ICU: 1938
       Fatalities: 19800
     
    MEDIUM TERM FORECAST (102 days from model start date): 
       Percent of population exposed at end simulation: 25%
       Peak ICU admissions:  6413  on day 2020-03-26
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 23490



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_4.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_5.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_6.png)


     



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-18 21:59:38.293474

