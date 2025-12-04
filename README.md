**Overview:**
This project applied the Seasonal Autoregressive Integrated Moving Average (SARIMA) model to forecast daily public transport passenger journeys.
The dataset exhibited strong weekly seasonality, trends, and non-stationarity, making SARIMA an appropriate choice. 
SARIMA extends ARIMA by modeling both trend and recurring seasonal patterns, which are common in transport demand data.

**Why SARIMA Was Chosen**

--High interpretability – Results can be easily communicated to operational and managerial teams.

--Strong performance with limited data – Effective even with smaller datasets, unlike neural networks.

--Built-in seasonality modeling – Captures weekday/weekend ridership cycles.

--Fast computation – Supports iterative forecasting and low-resource environments.

--Stable short-term predictions – Ideal for operational planning (e.g., 7-day forecasts).

--This combination of speed, accuracy, and clarity makes SARIMA suitable for transport demand forecasting.

**Model Configuration:**

The chosen model was:
SARIMA(1, 1, 1)(1, 1, 1)_7
Parameter	Meaning
p = 1	Yesterday’s value influences today.
d = 1	Differencing removes trend.
q = 1	Accounts for short-term noise.
P = 1	Today depends on the same weekday last week.
D = 1	Seasonal differencing removes weekly drift.
Q = 1	Smooths weekly noise fluctuations.
m = 7	Reflects strong 7-day weekly cycles.

This structure allowed the model to capture both day-to-day variation and weekly operational patterns.

**Strengths of the Model**

--Captures weekly ridership cycles: peak weekdays, low weekends, school-day patterns.
--Produces stable forecasts for planning local routes, peak services, and school transport.
--Computationally efficient: trains in seconds, suitable for repeated or real-time forecasting.
--Transparent parameterization: easy to explain to stakeholders.
--Handles non-stationarity through differencing.

**What I Learned**

How to analyze time series data for trends, seasonality, and stationarity.
The process of model selection and parameter tuning for SARIMA.
Importance of seasonal differencing in capturing weekly patterns.

**Conclusion**

The SARIMA(1,1,1)(1,1,1)_7 model effectively captured the inherent weekly rhythm of public transport data, delivering accurate, interpretable, and computationally efficient forecasts.
Its reliability makes it a strong choice for real-world transportation analytics and operational planning.
