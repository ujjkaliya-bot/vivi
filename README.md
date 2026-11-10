# Ishani Music Bot

Telegram group voice-chat music bot, rebranded from the supplied project.

## Railway deployment

1. Push this project folder to a GitHub repository.
2. In Railway, create a project and deploy from that GitHub repository.
3. Add the variables from `.env.example` in Railway **Variables**.
4. Use the included `Procfile` / `start` command. Keep the worker process running.
5. Check Railway Deploy Logs for startup errors.

## Required variables

`API_ID`, `API_HASH`, `BOT_TOKEN`, `OWNER_ID`, `LOGGER_ID`, `MONGO_DB_URI`, and `STRING_SESSION`.

Set `OWNER_USERNAME` to Ishani's actual Telegram username **without `@`**. `OWNER_ID` is currently set to the ID supplied for this configuration. Replace it if that ID does not belong to Ishani.

## Secrets

Never commit `.env`, Telegram bot tokens, Pyrogram string sessions, MongoDB credentials, or YouTube cookies. `.env` is ignored by Git. Rotate any credentials that have been shared publicly.

## Notes

- Python version is pinned in `runtime.txt`.
- Internal Python package paths retain the upstream `SHUKLAMUSIC` module name so imports continue to work; this is an internal code identifier, not displayed bot branding.
- The upstream license and required attribution notices are retained.
- This ZIP is prepared for deployment configuration; a live Telegram/Railway runtime test has not been performed here.
