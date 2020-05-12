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

    Today's date: 2020-05-11 
    
    Country:  Spain
    - UCI database:  https://raw.githubusercontent.com/datadista/datasets/master/COVID%2019/ccaa_camas_uci_2017.csv
    - Total UCI beds:  4404
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  65



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_1.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_2.png)


    - Last day with data: 5/10/20
    - Spain fatalities to date: 26621
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-07
    - Infection to death latency (days):  13
    
    Intervention list:
    day since start simulation: 7  => beta reduction factor: 0.52
    day since start simulation: 24  => beta reduction factor: 0.48
    day since start simulation: 37  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 133882
    Optimization terminated successfully.
             Current function value: 1876.621110
             Iterations: 72
             Function evaluations: 139
    Estimated parameters:
    N0: 47851
    beta0 (contacts per day): 0.4
    R0: 2.01
    
    Final loss: 1876
    Initial/Final % loss: 1.4
    Normalized Loss (per million persons, per day) 0.619 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 125.0
    Initially infected/Total population (N0/N): 47851/46660000 (102.6 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.5 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 3.4  days, Initial R0: 2.0
    Interventions:
      1/beta at day 7.0  = 4.8  days, R0 = 1.05
      1/beta at day 24.0  = 5.2  days, R0 = 0.96
      1/beta at day 37.0  = 5.2  days, R0 = 0.96
    Latency for intervention effect on fatalities (days): 13
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-05-11
       Infected: 289015 (0.6%)
       Recovered: 13129444 (28.1%)
       Exposed to date: 13418459 (28.8%)
       In ICU: 809
       Fatalities: 26258
     
    MEDIUM TERM FORECAST (125 days from model start date): 
       Percent of population exposed at end simulation: 30%
       Peak ICU admissions:  6339  on day 2020-03-27
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 28027



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_4.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_5.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_6.png)


     



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-05-11 21:59:57.426949

