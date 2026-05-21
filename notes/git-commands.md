# Git Commands Cheatsheet

## Repository starten
- `git init` — neues lokales Repo in aktuellem Ordner anlegen

## Status & History
- `git status` — was ist geändert, getrackt, staged?
- `git log` — Liste aller Commits
- `git diff` — was hat sich seit letztem Commit geändert?

## Änderungen committen
- `git add <datei>` — Datei in Staging Area
- `git add .` — alle Änderungen im Ordner staged
- `git commit -m "message"` — staged Änderungen committen

## Konzepte
- **Working Directory** — deine echten Dateien
- **Staging Area** — was im nächsten Commit landen soll
- **Repository** — die History aller Commits