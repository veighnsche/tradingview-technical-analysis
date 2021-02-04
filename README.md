# tradingview-technical-analysis

## Installation

`npm i tradingview-technical-analysis`

## Usage

```

const analyze = require('tradingview-technical-analysis');
const tickers = ['BINANCE:BTCUSDT'];
const resolutions = ['1m','5m','15m','1h','4h','1d','1W','1M'];
const indicators = ['Recommend.All'];

const results = analyze(tickers, resolutions, indicators);

console.log(results)

```

## Response

```

{
    "BINANCE:BTCUSDT": {
        "signals": {
            "1m": {
                "Recommend.Other":"NEUTRAL",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "5m":{
                "Recommend.Other":"BUY",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "15m": {
                "Recommend.Other":"BUY",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "1h": {
                "Recommend.Other":"BUY",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "4h": {
                "Recommend.Other":"NEUTRAL",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "1D": {
                "Recommend.Other":"BUY",
                "Recommend.All":"STRONG_BUY",
                "Recommend.MA":"STRONG_BUY"
            },"1W":{
                "Recommend.Other":"NEUTRAL",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            },
            "1M": {
                "Recommend.Other":"NEUTRAL",
                "Recommend.All":"BUY",
                "Recommend.MA":"STRONG_BUY"
            }
        }
    }
}


```
## Arguments

### Ticker

Any exchange + pair available on Tradingview in uppercase `{exchange}:{pair}` format. I.e. `BINANCE:BTCUSDT`

### Resolutions

The following values are accepted:

```

'1m'
'5m'
'15m'
'1h'
'4h'
'1D'
'1W'
'1M'

```

### Indicators

The following indicators are (or will be) supported. Lines commented out are not yet implemented.

```

    "Recommend.Other",
    "Recommend.All",
    "Recommend.MA",
    /*"RSI",
    "RSI[1]",
    "Stoch.K",
    "Stoch.D",
    "Stoch.K[1]",
    "Stoch.D[1]",
    "CCI20",
    "CCI20[1]",
    "ADX",
    "ADX+DI",
    "ADX-DI",
    "ADX+DI[1]",
    "ADX-DI[1]",
    "AO",
    "AO[1]",
    "Mom",
    "Mom[1]",
    "MACD.macd",
    "MACD.signal",
    "Rec.Stoch.RSI",
    "Stoch.RSI.K",
    "Rec.WR",
    "W.R",
    "Rec.BBPower",
    "BBPower",
    "Rec.UO",
    "UO",
    "close",
    "EMA5",
    "SMA5",
    "EMA10",
    "SMA10",
    "EMA20",
    "SMA20",
    "EMA30",
    "SMA30",
    "EMA50",
    "SMA50",
    "EMA100",
    "SMA100",
    "EMA200",
    "SMA200",
    "Rec.Ichimoku",
    "Ichimoku.BLine",
    "Rec.VWMA",
    "VWMA",
    "Rec.HullMA9",
    "HullMA9",
    "Pivot.M.Classic.S3",
    "Pivot.M.Classic.S2",
    "Pivot.M.Classic.S1",
    "Pivot.M.Classic.Middle",
    "Pivot.M.Classic.R1",
    "Pivot.M.Classic.R2",
    "Pivot.M.Classic.R3",
    "Pivot.M.Fibonacci.S3",
    "Pivot.M.Fibonacci.S2",
    "Pivot.M.Fibonacci.S1",
    "Pivot.M.Fibonacci.Middle",
    "Pivot.M.Fibonacci.R1",
    "Pivot.M.Fibonacci.R2",
    "Pivot.M.Fibonacci.R3",
    "Pivot.M.Camarilla.S3",
    "Pivot.M.Camarilla.S2",
    "Pivot.M.Camarilla.S1",
    "Pivot.M.Camarilla.Middle",
    "Pivot.M.Camarilla.R1",
    "Pivot.M.Camarilla.R2",
    "Pivot.M.Camarilla.R3",
    "Pivot.M.Woodie.S3",
    "Pivot.M.Woodie.S2",
    "Pivot.M.Woodie.S1",
    "Pivot.M.Woodie.Middle",
    "Pivot.M.Woodie.R1",
    "Pivot.M.Woodie.R2",
    "Pivot.M.Woodie.R3",
    "Pivot.M.Demark.S1",
    "Pivot.M.Demark.Middle",
    "Pivot.M.Demark.R1"*/

    ```