# Binance Futures Trading Bot

A Python-based command-line trading bot that places MARKET and LIMIT orders on Binance USDT-M Futures Demo Trading using the Binance API.

## Features

* Place MARKET orders
* Place LIMIT orders
* Supports BUY and SELL orders
* Command-line interface using argparse
* Input validation
* API request and response logging
* Exception handling for invalid inputs and API errors
* Secure credential management using environment variables

## Project Structure

```text
binance-futures-trading-bot/
│
├── bot/
│   ├── __init__.py
│   ├── client.py
│   ├── logging_config.py
│   ├── orders.py
│   └── validators.py
│
├── logs/
│   └── trading_bot.log
│
├── cli.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Setup

### 1. Clone Repository

```bash
git clone https://github.com/Shxrlixn/binance-futures-trading-bot.git
cd binance-futures-trading-bot
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Create Environment File

Create a `.env` file in the project root:

```env
BINANCE_API_KEY=your_api_key
BINANCE_SECRET_KEY=your_secret_key
```

## Usage

### MARKET BUY

```bash
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

### MARKET SELL

```bash
python cli.py --symbol BTCUSDT --side SELL --type MARKET --quantity 0.001
```

### LIMIT BUY

```bash
python cli.py --symbol BTCUSDT --side BUY --type LIMIT --quantity 0.002 --price 50000
```

### LIMIT SELL

```bash
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.002 --price 100000
```

## Logging

All requests and responses are stored in:

```text
logs/trading_bot.log
```

## Assumptions

* Binance Futures Demo Trading account is configured correctly.
* API credentials have Futures permissions enabled.
* Orders are executed on Binance Demo Trading environment only.
* Internet connection is available during execution.

## Technologies Used

* Python 3
* python-binance
* python-dotenv
* argparse
* logging

## Author

Sherlien
