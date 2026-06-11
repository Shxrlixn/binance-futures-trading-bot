# Binance Futures Trading Bot

A command-line trading bot built in Python that places MARKET and LIMIT orders on Binance Futures Demo Trading using the Binance API.

## Features

- Place MARKET orders
- Place LIMIT orders
- Input validation
- Error handling
- Logging of API requests and responses
- Secure API key management using environment variables

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

Create a `.env` file:

```env
BINANCE_API_KEY=your_api_key
BINANCE_SECRET_KEY=your_secret_key
```

## Usage

### Market Buy

```bash
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

### Limit Buy

```bash
python cli.py --symbol BTCUSDT --side BUY --type LIMIT --quantity 0.002 --price 50000
```

## Logging

Logs are stored in:

```text
logs/trading_bot.log
```

## Technologies Used

- Python
- Binance Futures API
- python-binance
- python-dotenv
- Logging Module

## Author

Sherlien Molly D
