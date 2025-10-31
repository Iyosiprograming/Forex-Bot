# 🛠️ XAUUSD AI Trading Bot — Under Construction

> ⚠️ This project is under development.  

A simple AI-powered bot for trading **Gold (XAU/USD)** using MT5.  
The bot uses **price action**, **news events**, and **Mistral AI signals** to make trades and sends notifications via **Telegram**.

---

## 🔹 Features

- Trades only during **London & New York sessions**  
- Fetches latest **news headlines** from Google News every 10 minutes  
- Filters trades using **price action** (4H, 1H, 15m, 1m)  
- Considers **high-impact news & global events**  
- Uses **AI engine** to generate trade signals:
  - Trade type: Buy / Sell / No Trade  
  - Entry price  
  - SL / TP  
  - Lot size (based on AI confidence)  
  - SL trailing guidance  
- Executes trades in **MT5**, adjusting ±10 pips if AI signal is delayed  
- Stops price-action filter until current trade closes  
- Sends **real-time notifications** via Telegram  
- Provides **end-of-session summary**: total trades, wins, losses, % gain/loss  

---

## 📂 Folder Structure

```

Forex-Bot/
│
├── bot.py                     # Main loop: session control, coordinate modules
├── config.py                  # MT5 credentials, AI keys, Telegram token, risk settings
├── requirements.txt           # Python dependencies
├── README.md                  # Project overview
│
├── modules/
│   ├── mt5_connector.py       # Fetch candles, balance, open/close trades
│   ├── news_fetcher.py        # Fetch Google News headlines every 10 min
│   ├── price_action_filter.py # Price action filter for 4H, 1H, 15m, 1m
│   ├── ai_engine.py           # Send data to AI → trade signal
│   ├── trade_executor.py      # Open/close trades, adjust ±10 pips if needed
│   ├── sl_trailing.py         # Manage SL trailing based on AI guidance
│   ├── session_manager.py     # London/New York session logic
│   ├── risk_manager.py        # Lot sizing, max trade size, daily limits
│   ├── telegram_notifier.py   # Send Telegram messages for trades & summary
│   └── logger.py              # Logs trades, signals, errors

````

---

## ⚡ Setup

1. Clone the repo:

```bash
git clone https://github.com/Iyosiprograming/Forex-Bot.git
cd Forex-Bot
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file with:

```txt
MT5_LOGIN=your_mt5_login
MT5_PASSWORD=your_mt5_password
MT5_SERVER=your_mt5_server
TELEGRAM_TOKEN=your_telegram_token
AI_API_KEY=your_ai_key
```

4. Run the bot:

```bash
python bot.py
```

---

## 🧩 How It Works

1. Bot starts during **London / New York sessions**
2. Fetches **price data** + **news headlines**
3. Filters trades using **price action** + **news impact**
4. Sends data to **AI engine** → receives trade signal (entry, SL, TP, lot size, SL trailing)
5. Executes trade in **MT5**, adjusts ±10 pips if AI is delayed
6. Sends **real-time notifications** via Telegram
7. At session end, calculates **total trades, wins, losses, % gain/loss**

---

> ⚠️ **Note:** Keep the bot simple and test on a **demo account** first.
> Open-source and modular: easy to extend and contribute.

```
