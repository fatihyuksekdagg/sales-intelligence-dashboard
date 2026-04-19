# Signals Panel

A real-time trading signal dashboard built with Flask and vanilla JavaScript. Displays long/short/flat signals with entry, stop-loss, and take-profit levels. Includes a client-side PnL simulation engine.

## Features

- **Signal Feed** — displays 20 most recent signals across crypto, forex, and equities
- **Filtering** — search by symbol, filter by direction (long/short/flat), date range
- **PnL Simulator** — configure capital, commission, TP/SL percentages and run backsim
- **REST API** — `/api/signals` endpoint returns JSON signal data
- **Deployable** — ready for Render.com free tier (render.yaml included)

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Flask 3.0 |
| Frontend | Vanilla JS, Chart.js, CSS Grid |
| Deploy | Gunicorn + Render.com |

## Quick Start

```bash
git clone https://github.com/fatihyuksekdagg/signals-panel.git
cd signals-panel

python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

pip install -r requirements.txt
python app.py
# Open http://localhost:8000
```

## API

```
GET /api/signals
```

Returns a JSON array of signal objects:

```json
[
  {
    "timestamp": "2024-01-15T10:00:00Z",
    "symbol": "BTCUSDT",
    "side": "long",
    "entry": 42500.50,
    "stop": 41650.49,
    "tp": 43775.52,
    "confidence": 0.82
  }
]
```

## Disclaimer

For educational purposes only. Signals are simulated and do not constitute financial advice.

---

Built by [Fatih Yüksekdağ](https://github.com/fatihyuksekdagg)
