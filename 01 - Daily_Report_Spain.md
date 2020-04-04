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

    Today's date: 2020-04-04 
    
    Country:  Spain
    - UCI database:  https://raw.githubusercontent.com/datadista/datasets/master/COVID%2019/ccaa_camas_uci_2017.csv
    - Total UCI beds:  4404
    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  28



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_1.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_2.png)


    - Last day with data: 4/3/20
    - Spain fatalities to date: 11198
     
    
    Model Initial parameters:
    - Initial simulation day is March:  2020-03-07
    - Infection to death latency (days):  11
    
    Intervention list:
    day since start simulation: 7  => beta reduction factor: 0.57
    day since start simulation: 24  => beta reduction factor: 0.48
    
    Fitting parameters N0 and beta
    Initial loss: 24015
    Optimization terminated successfully.
             Current function value: 235.019801
             Iterations: 67
             Function evaluations: 133
    Estimated parameters:
    N0: 32561
    beta0 (contacts per day): 0.44
    R0: 2.18
    
    Final loss: 235
    Initial/Final % loss: 0.98
    Normalized Loss (per million persons, per day) 0.18 
    
    
    _____________________________________________________________________
     
    MODEL PARAMETERS:
    
    Model name: optimized 2 pars
    
    Simulated days: 42.0
    Initially infected/Total population (N0/N): 32561/46660000 (69.8 per 100,000)
    beta (per day): 0.4 , nu (per day): 0.2
    1/beta (days): 2.3 , 1/nu (days): 5.0
    IFR: 0.002
    Initial Doubling time: 2.9  days, Initial R0: 2.2
    Interventions:
      1/beta at day 7.0  = 4.1  days, R0 = 1.23
      1/beta at day 24.0  = 4.8  days, R0 = 1.04
    Latency for intervention effect on fatalities (days): 11
    Infected_to_Detected_ratio: 5
    
    
    _____________________________________________________________________
    
    MODEL'S OUTPUTS FOR TODAY: 2020-04-04
       Infected: 2256432 (4.8%)
       Recovered: 6056426 (13.0%)
       Exposed to date: 8312858 (17.8%)
       In ICU: 6318
       Fatalities: 12112
     
    MEDIUM TERM FORECAST (42 days from model start date): 
       Percent of population exposed at end simulation: 28%
       Peak ICU admissions:  6324  on day 2020-04-04
       (note model does not account for long ICU stays)
       Total fatalities at end of simulation: 23521



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_4.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_5.png)



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_6.png)


     



![png](01%20-%20Daily_Report_Spain_files/01%20-%20Daily_Report_Spain_2_8.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2
    
    Run finished 2020-04-04 17:59:26.367506

