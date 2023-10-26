# Problem description
The aim of the Water Supply Forecast Rodeo challenge is to create a probabilistic forecast model for the 0.10, 0.50, and 0.90 quantiles of seasonal water supply at 26 different hydrologic sites. In this first challenge stage, the Hindcast Stage, you will use historical data to simulate forecasts in the past. Accurate forecasts with well-characterized uncertainty will help water resources managers better operate facilities and manage drought conditions in the American West.

# Forecasting Task

In this challenge, the target variable is cumulative streamflow volume, measured in thousand acre-feet (KAF), at selected locations in the Western United States. Streamflow is the volume of water flowing in a river at a specific point, and seasonal water supply forecasting is the practice of predicting the cumulative streamflow—the total volume of water—over a specified period of time (the "season" or "forecast period"). The forecast season of interest typically covers the spring and summer. For most of the sites used in this challenge, the forecast season is April through July.

The date that the forecast is made is called the issue date. For example, a forecast for the April–July season issued on March 1 for a given site would use the best available data as of March 1 to predict the cumulative volume that flows through that site later that year from April through July. In this challenge, you will issue forecasts on the 1st, 8th, 15th, and 22nd of each month from January through July.

Here are some examples of operational water supply forecasts:

NRCS Streamflow Forecast Summary for the 2023 season for Montana sites, issued March 1, 2023
Northwest RFC Water Supply Forecast for the 2023 season for the south fork of the Flathead River near Hungry Horse Dam in Montana, issued March 1, 2023
The streamflow measurements of interest are of natural flow (also called unimpaired flow). This refers to the amount of water that would have flowed without influence from upstream dams or diversions. Observed flow measurements are naturalized by adding or subtracting known upstream influences.

## Qunatile Forecasting
Rather than predicting a single value for each forecast, your task is to produce a quantile forecast: the 0.10, 0.50 (median), and 0.90 quantiles of cumulative streamflow volume. Forecasting quantiles acknowledges the uncertainty inherent in predictions and provides a range representing a distribution of possible outcomes . The 0.50 quantile (median) prediction is the central tendency of the distribution, while the 0.10 and 0.90 quantile predictions are the lower and upper bounds of a centered 80%-confidence prediction interval.

Note that quantiles have the opposite notation compared with the "probability of exceedance" used in many of the operational water supply forecasts. For example, a 90% probability of exceedance is equivalent to the 0.10 quantile. Measurements should fall below the true 0.10 quantile value 10% of the time, and they should exceed it 90% of the time. For more information on probability of exceedance, see the section "Interpreting water supply forecasts" of this reference.

