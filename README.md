# Crypto Signal Desk

A single-file, browser-based dashboard for analysing crypto (and NVDA via Binance's stock perpetual) with live data.

## Run it

Open `index.html` in a browser. If the page is blank, serve the folder locally:

```bash
python -m http.server 8765
```

then open <http://localhost:8765>.

No install, no API keys. Data comes from Binance's public market-data endpoints.

## Features

- Live candlestick chart with EMA 20/50/200, Bollinger Bands, Supertrend, VWAP, volume, RSI and MACD
- Buy/sell score (-1 to +1) from the indicator votes, with a plain-language "Why" list
- Support/resistance from swing points, plus entry, stop and two targets drawn on the chart
- Multi-timeframe verdicts, setup grade (A/B/C) and position-size calculator
- Backtester (with/without higher-timeframe and ADX filters) and a multi-coin test
- Alerts: browser notification + sound, price level, optional Telegram

## Honest caveat

Backtests across 9-10 symbols showed the score does **not** reliably beat buy-and-hold, and the
filters did not clearly help. Use it as an analysis and discipline tool, not an auto-trading signal.
It does not place orders. Not financial advice.

## Privacy

Telegram bot token and chat ID, if you enter them, are stored only in your browser's local storage.
They are never written to this repository.
