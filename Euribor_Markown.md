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
    ## 6174 2023-01-12 3.325
    ## 6175 2023-01-13 3.315
    ## 6176 2023-01-16 3.332
    ## 6177 2023-01-17 3.339
    ## 6178 2023-01-18 3.311
    ## 6179 2023-01-19 3.300

## Preview Forecast Rates Dataset

    ##         date forecast    lo_80    hi_80    lo_95    hi_95
    ## 1 2023-01-20 3.306838 3.279875 3.333801 3.265601 3.348074
    ## 2 2023-01-21 3.316290 3.275304 3.357275 3.253608 3.378972
    ## 3 2023-01-22 3.326659 3.273980 3.379339 3.246093 3.407225
    ## 4 2023-01-23 3.337223 3.274345 3.400102 3.241059 3.433388
    ## 5 2023-01-24 3.347842 3.275685 3.419998 3.237488 3.458196
    ## 6 2023-01-25 3.358473 3.277652 3.439294 3.234868 3.482077

    ##           date forecast    lo_80    hi_80    lo_95    hi_95
    ## 175 2023-07-13 5.155899 3.460153 6.851644 2.562479 7.749318
    ## 176 2023-07-14 5.166534 3.458389 6.874679 2.554151 7.778917
    ## 177 2023-07-15 5.177170 3.456595 6.897744 2.545778 7.808562
    ## 178 2023-07-16 5.187806 3.454772 6.920839 2.537360 7.838251
    ## 179 2023-07-17 5.198441 3.452919 6.943963 2.528896 7.867986
    ## 180 2023-07-18 5.209077 3.451037 6.967117 2.520387 7.897767

Last historic date is 2023-01-19, forecast range went from 2023-01-20 to
2023-07-18.

## 1 Year Historical + Forecast with 80% & 95% confidence intervals

![](Euribor_Markown_files/figure-gfm/one_historical_year_and_forecast_period-1.png)<!-- -->

## All Historic Data + Forecast with 95% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_95_confidence_interval-1.png)<!-- -->

## All Historic Data + Forecast with 80% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_80_confidence_interval-1.png)<!-- -->
