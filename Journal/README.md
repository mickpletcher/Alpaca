## TRADE JOURNAL — `journal_server.py` + `journal.html`

A web app to log every trade, track your P&L, and analyze patterns.

### Install
```
pip install flask
```

### Run
```
python journal_server.py
```
Then open **http://localhost:5000** in your browser.

### Features
- **Log Trade** — full trade details with setup, emotion, mistake, lesson
- **Trade History** — sortable table with P&L badges
- **Analytics** — win rate, avg win/loss, profit factor, streak, setup performance
- **AI Analysis** — auto-generates a coaching prompt from your last 30 trades. Paste into Claude for personalized feedback.
- **Export CSV** — download all trades for Excel analysis
- Data stored in `trades.db` (SQLite — stays on your machine)

### The AI Analysis Workflow
1. Trade for 2-4 weeks and log everything
2. Go to the **AI Analysis** tab
3. Click **Generate Prompt**
4. Copy the generated text
5. Paste into Claude and ask for coaching feedback
6. Claude will identify patterns in your wins/losses, emotional state, and setups
