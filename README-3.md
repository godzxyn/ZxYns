# ZxYn Hosting Bot

## GitHub upload
1. Create a new **Private** repository on GitHub.
2. Upload `bot.py`, `requirements.txt`, `Procfile`, and `.python-version` (you can upload the other included files too).
3. Commit the files.

## Deploy on a Python hosting provider
GitHub stores the source code; it does not keep this Telegram bot running by itself. Connect this repository to a hosting provider that supports a persistent Python web service.

- Build/install command: `pip install -r requirements.txt`
- Start command: `python bot.py`
- Environment variable: `BOT_TOKEN` = your Telegram bot token
- The included `Procfile` uses: `web: python bot.py`

Do not put the bot token in `bot.py`, GitHub commits, screenshots, or public messages. If a token was ever exposed, revoke it with BotFather and create a new one.

## Important storage note
The bot creates `exu_data/` and `exu_uploads/` beside `bot.py`. Many free hosting services erase local files when the service restarts or redeploys. Use a persistent disk/volume if you need uploaded scripts and database data to survive restarts. This bot runs uploaded scripts, so only allow trusted users to upload files.
