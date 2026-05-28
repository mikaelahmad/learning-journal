# GitHub Workflow Cheatsheet

## Setup einmalig
- SSH-Key generieren: `ssh-keygen -t ed25519 -C "email"`
- Public Key bei GitHub hinterlegen
- Verbindung testen: `ssh -T git@github.com`

## Neues Remote-Repo verknüpfen
- `git remote add origin git@github.com:USER/REPO.git`
- `git remote -v` — zeigt verknüpfte Remotes
- `git push -u origin main` — erster Push mit Upstream-Tracking

## Standard-Workflow (täglich)
- Lokal: `git add .` → `git commit -m "..."` → `git push`
- Status checken: `git status`, `git log`

## Konzepte
- **origin** — Standard-Name für den ersten Remote (kein magischer Begriff)
- **main** — Default-Branch-Name (früher `master`)
- **upstream tracking** — verbindet lokalen Branch mit Remote-Branch, sodass `git push` ohne Argumente funktioniert
