# Skill: Verzweigung (Wenn-Dann-Sonst)

## Schritt 1: Entweder-Oder
Du kennst bereits die normale Bedingung (*WENN der Spieler den Gegner berührt, DANN verliere ein Leben*). Oft reicht das aber nicht. Was ist, wenn der Computer zwei verschiedene Wege gehen soll?

Dafür gibt es die vollständige **Verzweigung** (WENN - DANN - SONST). 
*Beispiel: WENN der Spieler 10 Punkte hat, DANN gewinnt er das Spiel, SONST sagt ihm der Computer: "Sammle noch mehr Punkte!"*

## Schritt 2: Die Verzweigung einbauen
Lass uns überprüfen, ob der Spieler genug Punkte hat, um durch eine Tür zu gehen oder ein Level zu beenden. Wir testen das auf Knopfdruck.

* Gehe zu **Controller** und hole den Block `wenn Taste A gedrückt`.
* Gehe zu **Logik** (hellblau) und ziehe den Block `wenn wahr dann ... ansonsten ...` hinein. (Das "ansonsten" ist unser SONST).
* Gehe nochmal zu **Logik** und hole dir aus dem Bereich "Vergleiche" den Block `0 = 0` (einen Vergleichs-Operator) und setze ihn in das `wahr`. Ändere das `=` zu einem `>` (größer als).

## Schritt 3: Die Bedingung füllen
Jetzt füllen wir die Lücken:
* Ziehe bei **Info** den runden Block `Punktzahl` in die erste `0`.
* Trage in die zweite `0` die Zahl `10` ein.
* Füge bei `dann` den Block `Spiel über (Gewonnen)` aus der Kategorie **Spiel** ein.
* Füge bei `ansonsten` den Block `mySprite sagt "Sammle mehr!"` aus der Kategorie **Sprites** ein.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (info.score() > 10) {
        game.gameOver(true)
    } else {
        mySprite.sayText("Sammle mehr Punkte!")
    }
})
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem man sieht, wo du eine "Wenn-Dann-Ansonsten"-Verzweigung in deinem Spiel nutzt.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Was ist der Unterschied zwischen einer einfachen Bedingung (nur WENN-DANN) und einer vollständigen Verzweigung (WENN-DANN-SONST)?
2. **Die Lebenswelt:** Im Alltag nutzen wir ständig Verzweigungen in unserem Kopf. Schreibe eine alltägliche Entscheidung als WENN-DANN-SONST Satz auf. (Beispiel: *WENN es regnet, DANN nehme ich den Regenschirm, SONST setze ich eine Sonnenbrille auf.*)
