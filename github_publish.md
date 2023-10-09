
# Übung: Veröffentliche ein Programm auf GitHub

In dieser Übung verwendest du Git, um ein Programm auf GitHub zu veröffentlichen.
Auch hier verwendest du die **Kommandozeile**.
Außerdem brauchst du einen Browser.

### Aufgabe 1: Erstelle ein GitHub-Projekt

* Lege ein Konto auf [GitHub](https://github.com/) an
* Erstelle dort ein neues Repository
* Gib dem Repository einen Namen und eine kurze Beschreibung
* Erstelle eine `README.md`-Datei (*optional*)
* Wähle die MIT-Lizenz aus (*optional*)

### Aufgabe 2: Erstelle eine lokale Arbeitskopie

* Gehe auf die Startseite Deines GitHub-Projekts
* Finde den grünen Knopf mit der Aufschrift **<> Code** (grün)
* Drücke darauf und kopiere die **HTTPS URL** des Projekts
* Öffne ein Kommandozeilenterminal
* Wechsle mit `cd` in das Verzeichnis, an dem das Projekt liegen soll (z.B. Desktop)
* Gib ein `git clone URL` und füge statt URL die kopierte Adresse ein

Es sollte ein neues Verzeichnis mit dem Namen deines Projekts entstehen.

### Aufgabe 3: Dateien hinzufügen

Füge dem Projektverzeichnis einige Dateien hinzu.
Dies können die Dateien aus dem ersten Teil sein.
Verwende `git add` und `git commit`, um die Änderungen dem Repository hinzuzufügen.

Falls du schon vorher ein Repository erstellt hast, achte darauf dass du die beiden nicht verwechselst.
Vor allem solltest du auf keinen Fall das `.git/`-Verzeichnis aus einem Repository in das andere kopieren.

### Aufgabe 4: Änderungen veröffentlichen

Nun kannst du alle Änderungen auf GitHub mit `git push` veröffentlichen.

Beim ersten Mal wünscht sich `git`, dass du Name und E-Mail konfigurierst.
Gib die angezeigten `git config ..`-Befehle ein oder folge den [Anweisungen im Abschnitt 'Konfiguration'](https://www.python4data.science/de/latest/productive/git/install-config.html).
Versuche `git push` dann erneut.

Aktualisiere die Webseite des Projekts im Browser.
Du solltest dort die Datei `hello.py` sehen.

### Aufgabe 5: Datenschutz

* Prüfe, ob sich im Projekt urheberrechtlich geschütztes Material oder persönliche Daten befinden
* Ergänze eventuelle Lizenzbestimmungen oder Namensnennungen in der README.md-Datei
* Mit `git rm DATEINAME` und `git commit` kannst Du Dateien ohne Nutzungsrechte löschen.

### Aufgabe 6: Kollaboration

Entwickle dein Projekt im Zweierteam weiter.

* Füge auf der Webseite unter **Settings -> Collaborators** eine zweite Autorin hinzu
* Mit `git clone` kann diese sich eine Kopie des Projekts besorgen wie oben beschrieben
* Wenn ihr Dateien ändert, müßt ihr die Änderungen jedes Mal mit `git add` und `git commit` einchecken.
* Mit `git push` könnt ihr eure Änderungen hochladen
* Mit `git pull` könnt ihr die aktuellste öffentliche Version des Codes anfordern

Fügt abwechselnd neue Dateien zum Repository hinzu.

### Aufgabe 7: Konflikte

Wenn ihr beide die gleiche Stelle in der gleichen Datei ändert, meldet `git pull` einen Konflikt.
Diesen müßt Ihr von Hand auflösen.
Editiert dazu die von `git status` als *merge conflict* angezeigte Datei.

In der Datei befinden sich Markierungen, die anzeigen, was von wem geschrieben wurde.
Entscheidet welche Teile ihr behalten möchtet und löscht die Markierungen.

Gebt anschließend wieder `git add` und `git commit` ein.

Wenn sich alle Änderungen mit `git push` hochladen lassen und das Programm noch funktioniert, habt ihr es richtig gemacht.

## Typische Probleme

#### git push funktioniert nicht!

Gib erst einmal ``git status`` ein und lies die Ausgabe aufmerksam.
Häufige Ursachen sind:

- du hast überhaupt noch nichts committet
- auf GitHub befinden sich andere Commits als bei dir. Führe zunächst `git pull` aus

#### git pull funktioniert nicht!

Gib erst einmal ``git status`` ein und lies die Ausgabe aufmerksam.
Häufige Ursachen sind:

- du hast noch nicht alle Änderungen committet. Führe ganz in Ruhe `git add` und `git commit` aus.
- es besteht ein merge Konflikt, den du auflösen musst
- es gibt gar keine neuen Änderungen

#### Ich glaube ich habe meine Arbeitskopie kaputt gemacht. Was jetzt?

Das ist nicht schlimm. Git soll ja gerade verhindern, dass etwas verloren geht.
Eine sichere Rettungsstrategie ist:

- erstelle eine Sicherheitskopie der gesamten Arbeitskopie
- gehe in ein anderes Verzeichnis, z.B. Desktop/
- erstelle eine neue Arbeitskopie mit `git clone`
- kopiere alles was du brauchst aus der Sicherheitskopie in die neue Arbeitskopie

#### Mein Problem ist hier nicht aufgeführt!

Schaue auf [First Aid Git](https://firstaidgit.io) nach.

