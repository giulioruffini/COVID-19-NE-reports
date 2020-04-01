# COVID-19 Models
![](./images/inscientia.jpg)

In this repository we (The Neuroelectrics and Starlab modeling teams) provide data analysis and projections of infection rates and fatalities using a compartment model. 

The goal is to peer into the future, at least a couple of weeks ahead, and to be able to do "what if" studies. What if the R0 is changed in such and such way?

We will update the model with real data as it comes while the COVID-19 crisis unfolds. We use SIR (and SEIR) to fit data on "detected infections", " "ICU entries" and "fatalities".  SIR has a list of parameters we can use (nu, beta, R0 = beta/nu, CFR etc).

Keep in mind that we are in a hurry (doubling time about 3 days), so please consider that perfection may be the enemy of usefulness.


## Modeling notes
For general notes on how the model is run and optimized see the docs folder.
### latency
The SIR model does not currently account for latency between exposure to symptoms/infectiousness. This is a factor to keep in mind.

Also, if we model fatalities as a proxy for current infections (simple approach), we are modeling historic data. What we see today is due to infections that happened up to 13 days ago ([median time delay of 13 days from illness onset to death](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7074197/) ago. In other words, we are modeling the past. 

When we add an intervention into the model, it needs to be delayed to adjust for this.

## Links and data sources
* [http://neuroelectrics.com](http://neuroelectrics.com)

* [http://starlab.es](http://starlab.es)

* [http://informecovid.org](http://informecovid.org)

* [JHU data repository](https://github.com/CSSEGISandData/COVID-19)


