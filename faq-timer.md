# FAQ: Timer (Countdown)

## Schritt 1: Zeitdruck aufbauen
Ein Spiel wird oft spannender, wenn der Spieler nur begrenzt Zeit hat (z. B. um den Ausgang eines Labyrinths zu finden). Der Computer kann die Zeit ganz automatisch für dich rückwärts zählen!

## Schritt 2: Den Timer starten
* Gehe zur Kategorie **Info** (dunkelrot).
* Ziehe den Block `starte Countdown-Timer (s) 10` in deinen Start-Block.
* Ändere die Zahl `10` auf die Sekundenanzahl, die du dem Spieler geben möchtest (z. B. `30`).

```blocks
info.startCountdown(30)
```

## Schritt 3: Was passiert bei 0?
Wenn der Timer bei 0 ankommt, beendet das Spiel automatisch und der Spieler hat verloren ("Game Over"). Du musst dafür keine extra Bedingung programmieren, das macht MakeCode automatisch für dich!