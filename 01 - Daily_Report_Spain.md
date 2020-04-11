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

    Today's date: 2020-04-10 
    
    Country:  Spain
    - UCI database:  https://raw.githubusercontent.com/datadista/datasets/master/COVID%2019/ccaa_camas_uci_2017.csv
    - Total UCI beds:  4404
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  34



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_1.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_2.png)


    - Last day with data: 4/10/20
    - Spain fatalities to date: 16081
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-07
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 7  => beta reduction factor: 0.54
    day since start simulation: 24  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 40835
    Optimization terminated successfully.
             Current function value: 728.374440
             Iterations: 64
             Function evaluations: 128
    Estimated parameters:
    N0: 37927
    beta0 (contacts per day): 0.43
    R0: 2.13
    
    Final loss: 728
    Initial/Final % loss: 1.78
    Normalized Loss (per million persons, per day) 0.446 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 48.0
    Initially infected/Total population (N0/N): 37927/46660000 (81.3 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.3 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 3.1  days, Initial R0: 2.1
    Interventions:
      1/beta at day 7.0  = 4.3  days, R0 = 1.16
      1/beta at day 24.0  = 4.9  days, R0 = 1.02
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-10
       Infected: 1862979 (4.0%)
       Recovered: 8190996 (17.6%)
       Exposed to date: 10053975 (21.5%)
       In ICU: 5216
       Fatalities: 16381
     
    MEDIUM TERM FORECAST (48 days from model start date): 
       Percent of population exposed at end simulation: 28%
       Peak ICU admissions:  5698  on day 2020-03-31
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 24271



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_4.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_5.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_6.png)


     



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-10 21:59:45.292968

