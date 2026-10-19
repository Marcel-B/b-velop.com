# b-velop.com

Statische Website von b-velop (Marcel Benders, freiberufliche Softwareentwicklung).

Kein Build-Schritt: `index.html`, `styles.css` und `assets/` lassen sich direkt auf jeden Webserver legen.
Lokal ansehen: `python3 -m http.server` und http://localhost:8000 öffnen.

## Deployment

Jeder Push auf `main` lädt die Seite per SFTP zu STRATO hoch (`.github/workflows/deploy.yml`, manuell auch unter *Actions → Deploy zu STRATO → Run workflow*).
Benötigte Repository-Secrets: `STRATO_SFTP_HOST`, `STRATO_SFTP_USER`, `STRATO_SFTP_PASSWORD`, optional `STRATO_REMOTE_DIR` (Standard `/`).
Dateien auf dem Server werden überschrieben, aber nie gelöscht.
