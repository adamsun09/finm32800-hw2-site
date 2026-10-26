# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures (ZQ)

Daily ohlcv-1d bars for 30-Day Fed Funds futures, pulled from the Databento GLBX.MDP3 dataset with the parent symbol ZQ.FUT, which returns every listed ZQ contract. Columns: date (tz-naive trading date, normalized from the 00:00 UTC bar timestamp), symbol, open, high, low, close, volume. A ZQ contract settles at 100 minus the calendar-day average effective federal funds rate over its contract month, so 100 - price is the market-implied average rate for that month. The symbol set includes calendar spreads (e.g. ZQU6-ZQZ6) alongside the outright monthly contracts (e.g. ZQU6); filter to outrights with fedwatch.filter_outright_contracts before using the prices. Far-dated contracts trade thinly and may have no bar on a given day.


## DataFrame Glimpse

```
Rows: 11818
Columns: 7
$ date   <datetime[ns]> 2026-10-22 00:00:00
$ symbol          <str> 'ZQ:BF J7-K7-N7'
$ open            <f64> -1.5
$ high            <f64> -1.5
$ low             <f64> -2.0
$ close           <f64> -2.0
$ volume          <u64> 537


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures (ZQ)                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Globex                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/                                   |
| Tags                           | Monetary Policy, Futures, Fedwatch, Fed Funds                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento Historical API via Python                                                   |
| Data available up to (min)     | 2026-10-22 00:00:00                                                             |
| Data available up to (max)     | 2026-10-22 00:00:00                                                             |
| Dataframe Path                 | /Users/adamsun/Documents/UChicago/Fall 2026/FINM 328/HW2/hw2-adamsun09/_data/fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file:///Users/adamsun/Documents/UChicago/Fall 2026/FINM 328/HW2/hw2-adamsun09/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-26 15:20:03           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

