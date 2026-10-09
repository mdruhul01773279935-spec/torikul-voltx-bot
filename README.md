# Torikul Voltx Bot

A Telegram bot.

## Setup

This repo does **not** contain a hardcoded bot token. Before running it (locally or on any
hosting provider), you must set the `BOT_TOKEN` environment variable to your bot's token
(get one from [@BotFather](https://t.me/BotFather) on Telegram).

### Local run

```bash
pip install -r requirements.txt
export BOT_TOKEN="your:bot-token-here"
python voltx_bot.py
```

### Render (or similar) deployment

1. Create a new **Web Service** pointing at this repo.
2. Build Command: `pip install -r requirements.txt`
3. Start Command: `python voltx_bot.py`
4. Under **Environment**, add a variable:
   - Key: `BOT_TOKEN`
   - Value: your real bot token
5. Deploy.

The bot will refuse to start (with a clear error message) if `BOT_TOKEN` is not set, instead
of silently failing.
