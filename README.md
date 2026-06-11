# Binance Futures Trading Bot

A Python-based command-line trading bot that places MARKET and LIMIT orders on Binance Futures Demo Trading using the Binance API.

## Features

* Place MARKET orders
* Place LIMIT orders
* Supports BUY and SELL orders
* Command-line interface using argparse
* Input validation
* Logging of API requests, responses, and errors
* Exception handling
* Secure API credential management using environment variables

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

## Installation

Clone the repository:

```bash
git clone https://github.com/Shxrlixn/binance-futures-trading-bot.git
cd binance-futures-trading-bot
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the root directory:

```env
API_KEY=your_api_key
API_SECRET=your_api_secret
```

## Usage

### MARKET BUY Order

```bash
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

### MARKET SELL Order

```bash
python cli.py --symbol BTCUSDT --side SELL --type MARKET --quantity 0.001
```

### LIMIT BUY Order

```bash
python cli.py --symbol BTCUSDT --side BUY --type LIMIT --quantity 0.002 --price 50000
```

### LIMIT SELL Order

```bash
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.002 --price 100000
```

## Logging

All API requests, responses, and errors are logged to:

```text
logs/trading_bot.log
```

Example log entries:

```text
INFO - MARKET ORDER | Symbol=BTCUSDT Side=BUY Qty=0.001
INFO - Response: {...}
ERROR - Side must be BUY or SELL
```

## Validation

The application validates:

* Order side (BUY / SELL)
* Order type (MARKET / LIMIT)
* Positive quantity values
* Price requirement for LIMIT orders

## Assumptions

* Binance Futures Demo Trading account is configured correctly.
* Valid API credentials are available.
* Futures permissions are enabled for the API key.
* Internet access is available during execution.

## Technologies Used

* Python 3
* python-binance
* python-dotenv
* argparse
* logging

## Author

Sherlien Molly D
