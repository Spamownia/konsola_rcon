# DayZ RCON Announcer

Prosty skrypt Pythona do wysyłania powiadomień o restartach serwera DayZ przez BattlEye RCON.

## Konfiguracja
Edytuj env vars na Render.com lub lokalnie:
- `RCON_HOST`, `RCON_PORT`, `RCON_PASSWORD` – dane RCON z BEServer.cfg.
- `TIMEZONE` – np. `Europe/Warsaw`.
- `RESTART_HOURS` – lista godzin, np. `0,6,12,18`.
- `WARNINGS` – JSON z warn, np. `{"30": "ZA 30 MIN!", ...}`.
- `SHUTDOWN_MESSAGE` – wiadomość o restarcie.

## Deploy na Render.com
1. Połącz repo z Render.
2. New > Background Worker.
3. Build: `pip install -r requirements.txt`.
4. Start: `python dayz_restart_announcer.py`.
5. Dodaj env vars.
6. Deploy!

## Lokalny test
`pip install -r requirements.txt`
Ustaw env w terminalu, np. `export RCON_HOST=...`
`python dayz_restart_announcer.py`
