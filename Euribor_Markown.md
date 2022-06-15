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
    ## 6015 2022-06-03 0.486
    ## 6016 2022-06-06 0.521
    ## 6017 2022-06-07 0.561
    ## 6018 2022-06-08 0.569
    ## 6019 2022-06-09 0.614
    ## 6020 2022-06-10 0.680

## Preview Forecast Rates Dataset

    ##         date  forecast     lo_80     hi_80     lo_95     hi_95
    ## 1 2022-06-11 0.6999370 0.6749289 0.7249450 0.6616904 0.7381835
    ## 2 2022-06-12 0.7161014 0.6784959 0.7537069 0.6585887 0.7736140
    ## 3 2022-06-13 0.7306368 0.6826266 0.7786469 0.6572116 0.8040620
    ## 4 2022-06-14 0.7449586 0.6878676 0.8020497 0.6576454 0.8322718
    ## 5 2022-06-15 0.7590700 0.6936588 0.8244811 0.6590323 0.8591077
    ## 6 2022-06-16 0.7729740 0.6997360 0.8462120 0.6609662 0.8849818

    ##           date forecast     lo_80    hi_80      lo_95    hi_95
    ## 175 2022-12-02 1.628878 0.6099724 2.647783 0.07059639 3.187160
    ## 176 2022-12-03 1.630000 0.6066190 2.653382 0.06487353 3.195127
    ## 177 2022-12-04 1.631106 0.6032610 2.658952 0.05915247 3.203060
    ## 178 2022-12-05 1.632196 0.5998987 2.664494 0.05343338 3.210959
    ## 179 2022-12-06 1.633270 0.5965322 2.670008 0.04771642 3.218823
    ## 180 2022-12-07 1.634328 0.5931618 2.675494 0.04200174 3.226654

Last historic date is 2022-06-10, forecast range went from 2022-06-11 to
2022-12-07.

## 1 Year Historical + Forecast with 80% & 95% confidence intervals

![](Euribor_Markown_files/figure-gfm/one_historical_year_and_forecast_period-1.png)<!-- -->

## All Historic Data + Forecast with 95% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_95_confidence_interval-1.png)<!-- -->

## All Historic Data + Forecast with 80% confidence interval

![](Euribor_Markown_files/figure-gfm/all_historic_year_and_forecast_80_confidence_interval-1.png)<!-- -->
