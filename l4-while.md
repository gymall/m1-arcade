# Skill: Vorprüfende Schleife (Solange...)

## Schritt 1: Solange bis...
Die letzte und mächtigste Schleife ist die **vorprüfende Schleife** (auch WHILE-Schleife genannt). Sie wiederholt eine Aktion nicht nach Zeit oder einer festen Zahl, sondern *SOLANGE eine bestimmte Bedingung wahr ist*. 

*Beispiel: SOLANGE das Handy weniger als 100% Akku hat, lade es weiter auf.* Der Computer prüft hier VOR jedem Durchlauf, ob die Bedingung noch zutrifft.

## Schritt 2: Leben langsam aufladen
Lass uns einen Heiltrank simulieren. Wenn der Spieler Taste B drückt, soll sich das Leben aufladen, aber *nur solange* er weniger als 5 Leben hat.

* Gehe zu **Controller** und hole `wenn Taste B gedrückt`.
* Gehe zu **Schleifen** und ziehe den Block `solange wahr mache` hinein.
* Ziehe aus **Logik** den Vergleich `0 < 0` (kleiner als) in das Feld `wahr`.
* Lege in die erste `0` den runden Block `Leben` aus **Info**. In die zweite `0` tippst du die Zahl `5`.

## Schritt 3: Die Notbremse (Pause) einbauen!
**⚠️ ACHTUNG GEFAHR!** Eine WHILE-Schleife ist so rasend schnell, dass dein Browser abstürzen kann, wenn du sie nicht bremst!

* Gehe zu **Info** und ziehe `ändere Leben um 1` IN deine Schleife.
* Gehe zu **Schleifen** und ziehe UNBEDINGT den Block `pausiere 500 ms` direkt darunter in die Schleife. So kann man sehen, wie sich das Leben langsam auflädt.

```blocks
controller.B.onEvent(ControllerButtonEvent.Pressed, function () {
    while (info.life() < 5) {
        info.changeLifeBy(1)
        pause(500)
    }
})
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot deiner eigenen vorprüfenden Schleife (WHILE) hoch.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Was bedeutet es, dass eine Schleife "vorprüfend" ist? Was checkt der Computer, bevor er die Blöcke im Inneren ausführt?
2. **Die Lebenswelt:** Eine vorprüfende Schleife (WHILE) wiederholt etwas, *solange* ein Zustand zutrifft. Nenne ein alltägliches Beispiel beim Essen (z.B. mit einem Teller oder einem Glas), das genau wie eine WHILE-Schleife funktioniert.
