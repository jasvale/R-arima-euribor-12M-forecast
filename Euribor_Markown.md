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
    ## 6036 2022-07-01 0.961
    ## 6037 2022-07-04 0.897
    ## 6038 2022-07-05 0.939
    ## 6039 2022-07-06 0.839
    ## 6040 2022-07-07 0.821
    ## 6041 2022-07-08 0.972

## Preview Forecast Rates Dataset

    ##         date  forecast     lo_80    hi_80     lo_95    hi_95
    ## 1 2022-07-09 0.9952586 0.9696638 1.020853 0.9561147 1.034402
    ## 2 2022-07-10 1.0089400 0.9702217 1.047658 0.9497255 1.068155
    ## 3 2022-07-11 1.0180273 0.9685244 1.067530 0.9423191 1.093736
    ## 4 2022-07-12 1.0269798 0.9681027 1.085857 0.9369350 1.117025
    ## 5 2022-07-13 1.0357995 0.9683596 1.103239 0.9326590 1.138940
    ## 6 2022-07-14 1.0444883 0.9690134 1.119963 0.9290594 1.159917

    ##           date forecast     lo_80    hi_80        lo_95    hi_95
    ## 175 2022-12-30 1.575259 0.5581312 2.592386  0.019696540 3.130821
    ## 176 2022-12-31 1.575943 0.5543912 2.597494  0.013614440 3.138271
    ## 177 2023-01-01 1.576617 0.5506530 2.602581  0.007540390 3.145694
    ## 178 2023-01-02 1.577281 0.5469166 2.607646  0.001474461 3.153088
    ## 179 2023-01-03 1.577936 0.5431821 2.612689 -0.004583280 3.160454
    ## 180 2023-01-04 1.578580 0.5394497 2.617711 -0.010632766 3.167793

Last historic date is 2022-07-08, forecast range went from 2022-07-09 to
2023-01-04.

## 1 Year Historical + Forecast with 80% & 95% confidence intervals

![](Euribor_Markown_files/figure-gfm/one_historical_year_and_forecast_period-1.png)<!-- -->

## All Historic Data + Forecast with 95% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_95_confidence_interval-1.png)<!-- -->

## All Historic Data + Forecast with 80% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_80_confidence_interval-1.png)<!-- -->
