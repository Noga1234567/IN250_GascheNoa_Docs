# Aufgabe Markdown und Git

## Reporitory & Markdown-Datei erstellen
Das Repository und die Markdown-Datei "git_basics.md" wurden Browser erstellt.

## Repository klonen
Das Repository wurde über das Terminal geklont.
Dafür wurde folgender Befehl verwendet:
git clone https://github.com/Noga1234567/IN250_GascheNoa_Docs.git
Danach wurde mit folgenden Befehlen die Datei "git_basics.md" geöffnet, um die Schritte zu dokumentieren:
cd .\IN250_GascheNoa_Docs\
code .\git_basics.md

## Markdown Cheatsheet kopieren & Commit erstellen
Das Cheatsheet für Markdown wurde mit folgendem Befehl in den aktuellen Pfad kopiert:
cp ..\cowsay-python\cowsay\markdown_basics.md
Mit folgendem Befehl wurde überprüft, welche Dateien geändert wurden:
git status
Mit folgendem Befehl wurden die geänderten Dateien zum Commit hinzugefügt:
git add .\markdown_basics.md .\git_basics.md
Mit folgenden Befehlen wurde der Commit ausgeführt und gepusht:
git commit -m "Initial commit"
git push -u origin main

## Gitignore File
Das .gitignore-File wurde mit folgendem Befehl erstellt und befüllt:
"*.log`nGeheimeBankInformationen.txt" | Set-Content -NoNewline .gitignore
Mit folgenden Befehlen wurden die Änderungen committed und gepusht:
git add .\.gitignore .\git_basics.md
git commit -m "Add gitignore"
git push

## Remote Origin
Zuerst wurde mit folgende Befehlen ein neues Verzeichnis erstellt und ausgewählt:
mkdir IN250_GascheNoa_Docs_init
cd .\IN250_GascheNoa_Docs_init\
Danach wurde der Remote Origin gesetzt:
git init
git remote add origin https://github.com/Noga1234567/IN250_GascheNoa_Docs.git
git remote -v
Mit folgenden Befehlen wurden die Repositories synchronisiert:
git fetch origin
git checkout -b main origin/main

### Beobachtung
Wenn auf dem Remote bereits Commits existieren, kommt sehr oft ein Push-Fehler wie "non fast forward". Dann muss  zuerst gepullt werden oder der Remote Stand eingebaut werden.

### Änderungen im alten Ordern vorher gepusht
Dann hat das Remote bereits eine Historie. Wenn im neuen "git init"-Ordner versucht wird zu pushen, ohne zuerst zu pullen, wird der Push in der Regel abgelehnt, weil die lokale Historie nicht auf dem neuesten Stand ist.

## Git in der Softwareentwicklung
- Jede Änderung kann mit einem Commit gespeichert werden. So sieht man später, wann etwas geändert wurde, wer es geändert hat und warum. Das ist hilfreich, wenn ein Bug auftaucht und herausgefunden werden muss, welche Änderung ihn verursacht hat.
- Wenn etwas kaputt geht, kannst prolemlos auf einen älteren, funktionierenden Stand zurückgekehrt werden.
- Mehrere Personen können parallel am selben Projekt arbeiten. Git hilft beim Zusammenführen der Änderungen. Konflikte werden sichtbar und können gezielt gelöst werden, statt dass Dateien überschrieben werden.
- Neue Features können in einem Branch entwickelt werden, ohne die stabile Hauptversion zu gefährden. Erst wenn alles passt, wird zusammengeführt.
- In vielen Teams laufen Änderungen über Pull Requests oder Merge Requests. Dadurch werden Änderungen geprüft, bevor sie in den Hauptstand kommen. Das reduziert Fehler und verbessert die Codequalität.

## Feuer: Git Commit - Git Push > Flucht
- Ein Commit ist erst einmal nur auf dem Computer im lokalen Repository gespeichert. Wenn der Laptop zerstört wird oder verloren geht, sind diese Commits weg.
- Erst mit "git push" landen die Änderungen auf GitHub oder einem anderen Remote Server. Dann sind sie auch dann noch vorhanden, wenn das Gerät kaputt geht.

## git_basics.md Commiten
Die Datei git_basics.md befand sich bereits im Repository.
Mit folgenden Befehlen wurde die Datei commited und gepusht:
git add .\git_basics.md
git commit -m "Add git basics documentation"