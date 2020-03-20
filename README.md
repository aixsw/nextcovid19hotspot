# Next COVID-19 Hotspot
Estimator of next COVID-19 contagion hotspot: location, contagion and fatalities curve.

## What is this?
This is a Data Product(1) to assist in decision making for health and sanitation authorities with respect to allocation of hospital beds, tests, supplies, and general resources to deal with the COVID-19 outbreak given a certain city in Mexico.

## What's the central hypothesis?
The next contagion hotspot is given by:
1. High population density
2. High proportion of vulnerable population
3. High pollution by PM10
4. Venues and places of interest that incentivize going out (large markets -tianguis-, large parks and green public spaces, malls, etc.)

## What are the outputs?
1. Next contagion hotspot
2. Contagion curve
3. Fatalities curve

## What are the inputs?
1. Current city/neighborhood with contagion situation

## How does it work?
1. When a city/neighborhood is entered into the system, we use City, Uber and Didi Mobility data to select the top 3 points with the most flux of people coming out of the specified point. Then, **FOR EACH POINT:**
2. Population density is then obtained.
3. Demographics are then obtained to estimate the vulnerable population.
4. Pollution by PM10 of the area is obtained
5. Places of interest that can hold large crowds are identified
6. An estimation of the population affected is derived.
7. The estimation is fitted into an exponential curve.
8. The fatalities curve is then derived from the contagion curve.
9. **END FOR**
10. Potential points are then ranked.

## What data are required?
- Sankey diagram of disease spread (built by us)
- Pop Density by neighborhood across the country
- Uber/Didi/City Mobility Data
- Pollution map from meteo stations in the city (SEMARNAT?)
- DENUE for places of interest that can hold major crowds (INEGI)
- Demographics per borough across the country (INEGI)

## Further work

## Notes
(1): A Data product is a software-backed automated decision system that observes and learns about reality, emits a recommendation of an action backed by a prediction or an inference, REOBSERVES reality to pick up the effect of such action, and RELEARNS about the new reality changed by the action taken. It does this in an endless loop until the predictions "decay" and start to diverge from reality severely.
