# Woche 1 — Setup & Werkzeuge

**Phase 1: Fundament + Habits | Woche 1 von 104**

## Ziel dieser Woche

Du baust noch nichts Großes. Du installierst die Werkzeuge, mit denen du die nächsten 24 Monate arbeitest, und legst die Habit-Infrastruktur an. Am Ende der Woche: WSL2 läuft, Git verstehst du auf Alltagsniveau, Anki ist eingerichtet mit ersten echten Karten, GitHub-Profil ist aufgeräumt, `learning-journal`-Repo existiert.

**Wichtig:** Es wird sich diese Woche anfühlen, als würdest du nicht "richtig programmieren". Das ist Absicht. Werkzeuge zuerst, dann die Arbeit damit.

## Anki diese Woche

Tagesziel: **5–10 neue Karten/Tag, alle Reviews machen.** Da du gerade erst startest, hast du noch keine Reviews — die kommen ab Tag 2.

Erstelle Karten nur zu Dingen, die du selbst angewendet hast. Beispiele kommen unten in den Tagesblöcken.

## Montag — WSL2 + Linux-Setup (2h)

**90 Min: WSL2 installieren und einrichten**

- Folge der offiziellen Microsoft-Anleitung: <https://learn.microsoft.com/en-us/windows/wsl/install>
- Installiere Ubuntu 22.04 LTS (nicht "Ubuntu" ohne Versionsnummer — die ist Rolling und kann Probleme machen).
- Nach Installation: `sudo apt update && sudo apt upgrade -y` ausführen.
- Installiere Windows Terminal aus dem Microsoft Store (falls noch nicht da).
- Konfiguriere Windows Terminal so, dass Ubuntu der Standard ist.

**30 Min: Erste Linux-Befehle anwenden**

In deinem WSL-Terminal — *tippen, nicht copy-pasten*. Muscle memory ist der Punkt:

- `pwd` — wo bin ich?
- `ls -la` — was ist hier?
- `cd ~` — Home-Verzeichnis
- `mkdir projects && cd projects` — Verzeichnis anlegen und reingehen
- `touch test.txt && echo "hello" > test.txt && cat test.txt`
- `rm test.txt`

**Anki-Karten heute (Beispiele):**
- F: "Wie installiert man Updates in Ubuntu?" → A: "sudo apt update && sudo apt upgrade"
- F: "Was macht `cd ~`?" → A: "Wechselt ins Home-Verzeichnis des aktuellen Users"
- F: "Wozu der `-la`-Flag bei `ls`?" → A: "Long format + alle Files inkl. versteckter (.dotfiles)"

5 Karten reichen heute.

## Dienstag — Git Basics (2h)

**60 Min: Git installieren und Pro Git Buch Kapitel 1–2**

- In WSL: `sudo apt install git`
- Konfiguration: `git config --global user.name "Dein Name"` + `git config --global user.email "deine@email.com"`
- Lies Pro Git Buch (kostenlos): <https://git-scm.com/book/en/v2> — Kapitel 1 (Getting Started) + Kapitel 2.1–2.3 (Basics).
- **Englisch-Block (Teil der 60 Min):** Lies das auf Englisch, auch wenn es anstrengt. Notiere unbekannte Begriffe in dein "English-Tech"-Anki-Deck.

**30 Min: Erste Übung — eigenes Repo lokal**

In deinem `~/projects`-Ordner:

```
mkdir git-practice && cd git-practice
git init
echo "# My first repo" > README.md
git status
git add README.md
git commit -m "Initial commit"
echo "line two" >> README.md
git diff
git add . && git commit -m "Add second line"
git log
```

Verstehe jeden Befehl. Nicht nur abtippen.

**30 Min: 30 Min Anki + Reviews**

- Reviews von gestern (5 Karten).
- 5–8 neue Karten zu Git: `git add` vs `git commit`, `git status`, was macht `git init`, was zeigt `git log`, Unterschied working directory / staging area / repository.

**Anki-Beispiele:**
- F: "Was ist der Unterschied zwischen `git add` und `git commit`?" → A: "`add` bringt Änderungen in die Staging Area, `commit` schreibt sie in die History."
- F: "Was ist die Staging Area?" → A: "Zwischenzone zwischen Working Directory und Repository, in der man auswählt, was im nächsten Commit landet."

## Mittwoch — GitHub + erstes Remote-Repo (2h)

**90 Min: GitHub-Workflow**

- Falls noch nicht: SSH-Key für GitHub einrichten. Anleitung: <https://docs.github.com/en/authentication/connecting-to-github-with-ssh>. Auf Englisch lesen.
- Erstelle auf GitHub ein neues Repo: `learning-journal` (public, ohne README).
- Verknüpfe lokal:
  ```
  cd ~/projects && mkdir learning-journal && cd learning-journal
  git init
  git branch -M main
  git remote add origin git@github.com:DEINUSER/learning-journal.git
  ```
- Erstelle eine `README.md` mit folgendem Inhalt (Englisch — das ist dein erstes Stück Public-Facing Englisch):

  ```markdown
  # Learning Journal

  Personal log of my journey from Medieninformatik student to backend engineer.
  Started: 2026-05-14.

  ## Structure
  - `weeks/` — weekly plans and retrospectives
  - `notes/` — concept notes
  - `projects/` — links to project repos
  ```

- `git add . && git commit -m "Initialize learning journal" && git push -u origin main`

- Erstelle den Ordner `weeks/` und speichere diesen Wochenplan als `weeks/W01-setup.md` ab. Push.

**30 Min: GitHub-Profil aufräumen**

- Profilbild hinzufügen (kein Avatar-Default).
- Bio schreiben: 1–2 Sätze, auf Englisch. Beispiel: *"Medieninformatik student transitioning to backend engineering. Currently learning C#, .NET, and the fundamentals of distributed systems."*
- Erstelle ein "Profile README" — Repo mit deinem Username als Name (z.B. `meinusername/meinusername`). README.md wird auf deinem Profil angezeigt. Halte es minimal — Vorzeigen kommt später, wenn du was zu zeigen hast.

**30 Min: Anki**

- Reviews + 5 neue Karten zu Git-Remote/GitHub-Workflow.
- Z.B.: F: "Was macht `git push -u origin main`?" → A: "Pusht den main-Branch zu origin und setzt Upstream-Tracking für zukünftige `git push` ohne Argumente."

## Donnerstag — Editor-Setup + Englisch-Block (2h)

**60 Min: Editor einrichten**

Wähl einen — nicht beides:

**Option A: VS Code** (empfohlen für Anfang, breites Ökosystem)
- Installiere VS Code auf Windows.
- Installiere Extension "WSL" — damit kannst du WSL-Projekte direkt öffnen.
- Installiere die C# Dev Kit Extension.
- Lerne 10 Tastaturkürzel auswendig: Strg+P (File Search), Strg+Shift+P (Command Palette), Strg+, (Settings), Strg+` (Terminal), Strg+B (Sidebar), Alt+Pfeile (Zeile verschieben), Strg+D (nächstes Vorkommen), Strg+/ (Kommentar), F12 (Go to Definition), Strg+Shift+F (Suche im Projekt).

**Option B: JetBrains Rider** (besser für ernsthafte C#-Arbeit, kostenlos für Studenten)
- Beantrage JetBrains Student Pack: <https://www.jetbrains.com/community/education/#students>
- Installiere Rider.
- Lerne auch hier 10 Shortcuts.

Egal welche Option: **Erstelle ein Hello-World C#-Projekt.**
```
dotnet new console -n HelloWorld
cd HelloWorld
dotnet run
```
Push das Projekt in ein neues Repo `csharp-playground` auf GitHub. Das wird dein Spielwiese-Repo für die nächsten Wochen.

**30 Min: Englisch-Block**

Lies diesen Artikel: <https://www.cloudflare.com/learning/dns/what-is-dns/>

- Sehr gut geschrieben, mittlere Länge, technisch aber zugänglich.
- Schreibe danach in deinem Journal (`learning-journal/notes/dns-summary.md`) eine 5-Satz-Zusammenfassung auf Englisch. Auch wenn dein Englisch wackelt — *gerade weil es wackelt*.
- Push.

**30 Min: Anki**

- Reviews (jetzt langsam 10–15 Karten fällig).
- 5 neue Karten: 3 zu Editor-Shortcuts, 2 zu DNS aus dem Englisch-Block.

## Freitag — PUFFER (2h, optional)

Heute ist Puffer-Tag. **Nutze ihn so:**

- Wenn du diese Woche einen Tag verpasst hast: Hol nach.
- Wenn alles geklappt hat: **Nimm dir frei.** Ernsthaft. Das System lebt nur, wenn du nicht in jeden freien Tag was reinpresst.
- Wenn du *Lust* hast (nicht "muss"): Spiel mit der Kommandozeile. `htop` installieren und gucken, was läuft. `tree` installieren. Schau dir an, was in deinem `.bashrc` steht.

## Samstag — Crash Course CS Folge 1+2 + Wochenreview (2h)

**90 Min: Crash Course Computer Science**

- YouTube: <https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo>
- Schau Folge 1 ("Early Computing") und Folge 2 ("Electronic Computing").
- Untertitel auf Englisch (nicht Deutsch). Wenn du was nicht verstehst: Pause, nochmal, ggf. Begriff in Anki.
- Mache dir Notizen in `learning-journal/notes/crashcourse-cs-01-02.md`. **In eigenen Worten**, nicht Transkript. Push.

**30 Min: Anki**

- Reviews + 8–10 neue Karten zu Computing-Geschichte und Konzepten (z.B. "Was ist ein Vakuumröhrenrechner?", "Warum waren Transistoren ein Durchbruch?", "Was ist ein Bit?").

## Sonntag — Crash Course CS Folge 3+4 + Wochenreview (2h)

**60 Min: Crash Course Folge 3+4**

- Folge 3 ("Boolean Logic & Logic Gates"), Folge 4 ("Representing Numbers and Letters with Binary").
- Notizen in `crashcourse-cs-03-04.md`. Push.

**30 Min: Wochenreview**

Schreibe `weeks/W01-review.md` mit folgenden 5 Fragen:

1. Was habe ich diese Woche gebaut/installiert/eingerichtet?
2. Was habe ich konzeptionell verstanden, das ich vorher nicht verstand?
3. Wo bin ich hängengeblieben? (Konkret!)
4. Wie viele Anki-Karten habe ich jetzt insgesamt? (Anki zeigt das in der Statistik.)
5. Was ist mein Vorsatz für Woche 2?

Push.

**30 Min: Sonntag-Routine etablieren**

Heute *keine* neuen Anki-Karten. Nur Reviews. Sonntag ist Anki-leichter Tag, damit der Montag-Stack nicht riesig wird.

Schreib mir am Sonntagabend (oder Montagmorgen) mit deinem Status-Block (siehe unten, ausgefüllt) — dann gebe ich dir Woche 2.

---

## Status-Block (am Ende der Woche ausfüllen und kopieren)

```
STATUS: Woche 1 von 104, Phase 1 (Fundament + Habits), aktuelles Thema: Setup + CS-Basics.
Karriere-Fokus: Backend (.NET/C#), Ziel US-Remote oder Auswanderung in 24+ Monaten.
Zeitaufwand aktuell: 14h/Woche (Hochfahren auf 20-25h ab Monat 3 geplant).

Bisher gebaut/eingerichtet:
- WSL2 + Ubuntu 22.04 läuft
- Git konfiguriert, SSH-Key bei GitHub
- Repo: learning-journal (mit weeks/, notes/)
- Repo: csharp-playground (HelloWorld läuft)
- VS Code oder Rider eingerichtet
- Anki installiert, 3 Decks: CS-Fundamentals, Backend-Tech, English-Tech

Aktuelle Anki-Stats: ~XX Karten total, davon ~YY in CS-Fundamentals, ZZ in English-Tech.
Verpasste Tage diese Woche: [0 / Tag X]
Wochenreview-Highlight: [1 Satz]

Nächste Schritte (Woche 2): Crash Course CS Folgen 5-12 (Hardware-Grundlagen), erste C#-Übungen auf Exercism, "Code" von Petzold beginnen.

Plan-Quelle: github.com/DEINUSER/learning-journal
```

---

Wenn du diesen Plan in deinem Repo speicherst (`weeks/W01-setup.md`), bist du sofort produktiv und ich muss dir keine generische Anleitung mehr geben. Ab Woche 2 kommt am Sonntag der nächste Plan — du gibst mir den ausgefüllten Status-Block + kurzen Kommentar ("Mittwoch verpasst", "C# Setup hat 30 Min mehr gedauert"), und ich passe Woche 2 an deine Realität an.

Viel Erfolg. Schreib mir nächsten Sonntag.