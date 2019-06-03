# Git-Kurs Cheat-Sheet

## Konsole

- `pwd` – *print working directory* gibt akutelle Position in Ordnerstruktur aus
- `cd <pfad>` – *change directory* wechselt in angegebenen Ordner
  - `cd ..` – wechselt in den übergeorneten Ordner
- `mkdir <ordnername>` – *make directory* erstellt neuen Ordner
- `ls` – zeigt alle im aktuellen Ordner befindlichen Dateien und Ordner an
- `touch <dateiname>` – erstellt neue Datei
- `cat <dateiname>` – gibt Inhalt der angegebenen Datei auf der Konsole aus
- `vim <dateiname>` – öffnet Datei im Editor *vim* (auch andere Editoren wie *vi*, *nano* etc. möglich)
- `echo "<text>"` – gibt angegebenen Text auf der Konsole aus
  - `echo “<text>“ >> <dateiname.md>` – schreibt Text in angegebene Datei

## Git

- `git init` – initialisiert ein Git-Repository im aktuellen Ordner
- `git status` – gibt aktuellen Status des Repositorys aus (*working directory*, *staging area*, *untracked files* ...)
- `git config --list` – gibt aktuelle Git-Einstellungen aus; innerhalb eines Repositorys zusätlich Repo-Einstellungen
  - `git config --global user.name "<John Doe>"` – setzt Nutzernamen (üblicherweise GitHub/GitLab-Profilname)
  - `git config --global user.email <johndoe@example.com>` – setzt E-Mail-Adresse (üblicherweise GitHub/GitLab-E-Mail)
- `git add <dateiname>` – fügt Datei zur *staging area* hinzu
  - `git add .` – fügt alle neuen oder geänderten Dateien in diesem Ordner (rekursiv) zur *staging area* hinzu
- `git reset` – entfernt alle Dateien aus der *staging area* (Gegenteil von `git add .`)
  - `git reset <dateiname>` – entfernt eine bestimmte Datei aus der *staging area*
- `git commit` – fügt alle Elemente aus der *staging area* dem Repository hinzu
  - `git commit -m "<commit-message>"` – gibt zusätlich eine commit-Nachricht an, die ansonsten von Git angefordert würde
- `git log` – zeigt eine Liste der bisherigen commits an
- `git diff` – zeigt den Unterschied zwischen *working directory* und *repository*/letztem commit
   - `git diff --cached` – zeigt den Unterschied zwischen *staging area* und *repository*/letztem commit
- `git branch` – zeigt alle (lokal) verfügbaren branches an
  - `git branch <branch-name>` – erstellt einen neuen branch
  - `git branch -d <branch-name>` – löscht den angegebenen branch
- `git checkout <branch-name>` – wechselt auf den angegebenen branch
- `git merge <branch-name>` – vereint den angegebenen branch mit dem, in welchem man sich aktuell befindet (Änderungen des angegebenen branches werden in aktuellen übernommen)
- `git clone <link>` – lädt ein remote gehosteten Repository herunter
- `git fetch` – prüft auf Änderungen auf remote hosts
- `git pull` – lädt den aktuellen Stand vom remote host herunter
  - `git pull origin master` – gibt explizit an, welcher remote host und welcher branch heruntergeladen werden sollen
- `git push` – lädt den aktuellen Stand auf remote host hoch
  - `git push origin master` – gibt explizit an, auf welchen remote host und welchen branch hochgeladen werden soll
