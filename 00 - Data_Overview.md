![](./images/logo.png)
# Data overview (JHU datagrabber)
Neuroelectrics research team, March 2020

v1.0 G. Ruffini, R. Sanchez-Todo

This is a book to grab data from JHU and plot it for some countries, estimating also Rt and fatality doubling times using a simple logfit of the last 7 days.

*Note that the doubling and Rt data reflects infection rates about 11 days ago*


```python
from ne_epidemic.utilities import data_grabber_JHU
from ne_epidemic.param_estimate import get_doubling_time
```

# Spain


```python
df, firstdate = data_grabber_JHU(country="Spain")
_ = get_doubling_time(df, nu=1/5, ndays=7)
```

    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 7 / 2020
    - Days since first fatalities:  228



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_3_1.png)



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_3_2.png)


    - Last day with data: 10/20/20
    - Spain fatalities to date: 34210
     



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_3_4.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2


# Italy


```python
df, firstdate = data_grabber_JHU(country="Italy")
_ = get_doubling_time(df, nu=1/5, ndays=7)
```

    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  2 / 24 / 2020
    - Days since first fatalities:  240



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_5_1.png)



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_5_2.png)


    - Last day with data: 10/20/20
    - Italy fatalities to date: 36705
     



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_5_4.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2


# Portugal


```python
df, firstdate = data_grabber_JHU(country="Portugal")
_ = get_doubling_time(df, nu=1/5, ndays=7)
```

    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 20 / 2020
    - Days since first fatalities:  215



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_7_1.png)



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_7_2.png)


    - Last day with data: 10/20/20
    - Portugal fatalities to date: 2213
     



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_7_4.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2


# France


```python
df, firstdate = data_grabber_JHU(country="France")
_ = get_doubling_time(df, nu=1/5, ndays=7)
```

    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 5 / 2020
    - Days since first fatalities:  230



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_9_1.png)



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_9_2.png)


    - Last day with data: 10/20/20
    - France fatalities to date: 33636
     



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_9_4.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2


# United States


```python
df, firstdate = data_grabber_JHU(country="US")
_ = get_doubling_time(df, nu=1/5, ndays=7)
```

    - Fatalities database:  https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv
    - First day with more than 5 casualties (m/d/y):  3 / 2 / 2020
    - Days since first fatalities:  233



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_11_1.png)



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_11_2.png)


    - Last day with data: 10/20/20
    - US fatalities to date: 221052
     



![png](00%20-%20Data_Overview_files/00%20-%20Data_Overview_11_4.png)


    Note: a quadratic fit is carried out on the last days of log2(fatality data).
          The derivative of the quadratic is used to estimate doubling time and R(t).
    Rt estimated from doubling time using nu= 0.2

