# Forex-Bot

XAUUSD-AI-Bot/
│
├── bot.py                     # Main entry point, runs the trading loop
├── config.py                  # MT5 credentials, Telegram token, AI keys, risk settings
├── requirements.txt           # Python dependencies
│
├── modules/
│   ├── mt5_connector.py       # Connect to MT5, fetch candles, open/close trades
│   ├── news_fetcher.py        # Fetch and parse news headlines
│   ├── ai_engine.py           # Sends price + news to AI, receives trade signal
│   ├── telegram_notifier.py   # Send Telegram messages
│   ├── risk_manager.py        # Risk checks: max trade size, SL/TP, daily limits
│   └── logger.py              # Logs trades, signals, and errors
│
└── README.md
