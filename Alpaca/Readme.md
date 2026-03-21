## ALPACA PAPER TRADING — `alpaca_paper.py`

Paper trade with real market data and $0 risk. Required before trading real money.

### Setup (5 minutes)
1. Create a FREE account at https://alpaca.markets
2. Navigate to **Paper Trading** section
3. Click **Generate API Keys**
4. Edit `alpaca_paper.py` — replace:
   ```python
   ALPACA_API_KEY    = "YOUR_PAPER_API_KEY"
   ALPACA_SECRET_KEY = "YOUR_PAPER_SECRET_KEY"
   ```

### Install
```
pip install alpaca-trade-api pandas
```

### Commands
```bash
python alpaca_paper.py status           # Account balance and day trade count
python alpaca_paper.py quote SPY        # Live bid/ask/spread
python alpaca_paper.py buy  SPY 1       # Buy 1 share at market
python alpaca_paper.py sell SPY 1       # Sell 1 share at market
python alpaca_paper.py positions        # Open positions + P&L
python alpaca_paper.py orders           # Pending orders
python alpaca_paper.py bot              # Run live EMA crossover bot (paper)
```

### The Bot
`python alpaca_paper.py bot` runs a live EMA crossover strategy, checking price every 60 seconds during market hours. It will print every bar and flag buy/sell signals. This is the real-time version of what the backtester tested.

### Important: PDT Rule
The account status command shows your day trade count. If you make 4+ day trades in 5 days with under $25k in your account, your account gets flagged. Paper account has a $100k default — no issue. Real account: keep equity above $25k or trade on a cash account.
