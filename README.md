# 🛠️ XAUUSD AI Trading Bot — Under Construction

> ⚠️ This project is currently under development.  

A simple AI-powered bot for trading **Gold (XAU/USD)** using MT5.  
The bot uses **price action**, **news events**, and **AI signals** to make trades and sends notifications via **Telegram**.

---

## 🔹 Features

- Trades only during **London & New York sessions**  
- Filters trades using **price action** (4H, 1H, 15m, 1m)  
- Considers **high-impact news & global events**  
- Uses **AI engine** to generate trade signals (entry, SL, TP, lot size)  
- Executes trades in **MT5** with optional trailing stop  
- Sends **real-time notifications** via Telegram  
- Provides **daily summary**: total trades, wins, losses, PnL  

---

## 📂 Folder Structure

```

XAUUSD-AI-Bot/
│
├── bot.py                     # Main trading loop
├── config.py                  # MT5, Telegram, AI keys, risk settings
├── requirements.txt           # Python dependencies
├── README.md                  # Project overview
│
├── modules/
│   ├── mt5_connector.py       # MT5 connection & trade execution
│   ├── news_fetcher.py        # Fetch and filter news headlines
│   ├── ai_engine.py           # AI signal generation
│   ├── risk_manager.py        # Risk checks and limits
│   ├── telegram_notifier.py   # Telegram notifications
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

1. Fetch **price data** + **news headlines**
2. Filter trades via **price action** + **news impact**
3. Send data to **AI engine** → receive trade signal (entry, SL, TP, lot size)
4. Run **risk checks**
5. Execute trade via **MT5**
6. Send **Telegram notifications** for trades & daily summary

---

> ⚠️ **Note:** Keep the bot simple and test on a **demo account** first.
> Open-source and modular: easy to add new features.

```
