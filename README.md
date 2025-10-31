XAUUSD-AI-Bot/
│
├── bot.py                     # Main loop: runs trading sessions
├── config.py                  # MT5 credentials, Telegram token, AI keys, risk settings
├── requirements.txt           # Python dependencies
├── README.md                  # Project overview
│
├── modules/                   # Core modules
│   ├── mt5_connector.py       # Connect to MT5, fetch candles, open/close trades
│   ├── news_fetcher.py        # Fetch and parse news headlines
│   ├── ai_engine.py           # AI: price + news → trade signal
│   ├── risk_manager.py        # Risk checks: lot size, SL/TP, daily limits
│   ├── telegram_notifier.py   # Send Telegram messages
│   └── logger.py              # Logs trades, signals, errors
