Forecasting EURIBOR 12M with ARIMA using R
================

## Euribor Arima Forecast

Simple R Markdown that pulls historic 12M EURIBOR rates from
<https://www.euribor-rates.eu> in JSON format and performs an ARIMA
(Autoregressive integrated moving average) forecast for the next 180
days.

## Preview Historical Rates Dataset

    ##         date  rate
    ## 1 1999-01-01 3.213
    ## 2 1999-01-04 3.209
    ## 3 1999-01-05 3.187
    ## 4 1999-01-06 3.176
    ## 5 1999-01-07 3.158
    ## 6 1999-01-08 3.139

    ##            date  rate
    ## 6344 2023-09-13 4.112
    ## 6345 2023-09-14 4.159
    ## 6346 2023-09-15 4.169
    ## 6347 2023-09-18 4.191
    ## 6348 2023-09-19 4.216
    ## 6349 2023-09-20 4.222

## Preview Forecast Rates Dataset

    ##         date forecast    lo_80    hi_80    lo_95    hi_95
    ## 1 2023-09-21 4.228672 4.200063 4.257281 4.184918 4.272426
    ## 2 2023-09-22 4.234248 4.191558 4.276938 4.168959 4.299537
    ## 3 2023-09-23 4.239396 4.184492 4.294300 4.155427 4.323365
    ## 4 2023-09-24 4.244325 4.178509 4.310142 4.143668 4.344983
    ## 5 2023-09-25 4.249148 4.173342 4.324954 4.133213 4.365084
    ## 6 2023-09-26 4.253919 4.168804 4.339034 4.123747 4.384091

    ##           date forecast    lo_80    hi_80    lo_95    hi_95
    ## 175 2024-03-13 5.051651 3.479726 6.623576 2.647599 7.455703
    ## 176 2024-03-14 5.056371 3.473351 6.639391 2.635350 7.477392
    ## 177 2024-03-15 5.061091 3.466950 6.655232 2.623063 7.499119
    ## 178 2024-03-16 5.065811 3.460525 6.671098 2.610737 7.520885
    ## 179 2024-03-17 5.070531 3.454074 6.686988 2.598373 7.542689
    ## 180 2024-03-18 5.075251 3.447598 6.702904 2.585970 7.564532

Last historic date is 2023-09-20, forecast range went from 2023-09-21 to
2024-03-18.

## 1 Year Historical + Forecast with 80% & 95% confidence intervals

    ## Warning: Using `size` aesthetic for lines was deprecated in ggplot2 3.4.0.
    ## ℹ Please use `linewidth` instead.

![](Euribor_Markown_files/figure-gfm/one_historical_year_and_forecast_period-1.png)<!-- -->

## All Historic Data + Forecast with 95% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_95_confidence_interval-1.png)<!-- -->

## All Historic Data + Forecast with 80% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_80_confidence_interval-1.png)<!-- -->
