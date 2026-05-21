# Linux Commands Cheatsheet

## Navigation
- `pwd` — print working directory → **Wo bin ich?**
- `ls -la` — listet alle Dateien im Detail (inkl. versteckter) → **Was ist hier?**
- `cd ~` — wechselt ins Home-Verzeichnis → **Wie komme ich „nach Hause"?**
- `cd ..` — eine Ebene hoch → **Wie gehe ich einen Schritt zurück?**

## Dateien & Ordner
- `mkdir <name>` — erstellt einen neuen Ordner → **Wie erstelle ich Struktur?**
- `mkdir projects && cd projects` — erstellt Ordner und wechselt direkt rein
- `touch <name>` — erstellt eine leere Datei → **Wie erzeuge ich eine leere Datei?**
- `cat <name>` — zeigt Inhalt einer Datei → **Wie lese ich aus?**
- `rm <name>` — löscht eine Datei → **Wie räume ich auf?**

## Text in Dateien schreiben
- `echo "text" > file` — schreibt Text in Datei (**überschreibt!**) → **Wie schreibe ich rein?**
- `echo "text" >> file` — hängt Text am Ende an (überschreibt nicht)

## System
- `sudo apt update && sudo apt upgrade -y` — Updates installieren
  - `update` = neue Paketliste laden
  - `upgrade` = Updates installieren
  - `-y` = automatisch bestätigen

## Konzepte
- `sudo` — führt Befehl mit Admin-Rechten aus (für Systemänderungen)
- `&&` — verkettet zwei Befehle (zweiter läuft nur, wenn erster erfolgreich)
- `~` — Kurzschreibweise für dein Home-Verzeichnis
- `>` vs `>>` — überschreiben vs. anhängen