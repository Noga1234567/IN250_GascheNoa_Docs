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
