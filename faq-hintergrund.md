# FAQ: Bewegter Hintergrund

## Schritt 1: Spezialeffekte
Oft soll sich der Hintergrund bewegen, damit das Spiel aussieht, als würde man fliegen oder fahren. Der einfachste Weg in MakeCode dafür sind die eingebauten **Bildschirm-Effekte**!

## Schritt 2: Sterne im Hintergrund
Lass uns einen Retro-Weltraum-Effekt einbauen, bei dem Sterne dauerhaft auf dich zufliegen.

* Gehe zur Kategorie **Szene** (dunkelgrün).
* Scrolle ganz nach unten zu "Bildschirm Effekte".
* Ziehe den Block `starte Bildschirm Effekt Konfetti` in deinen grünen Start-Block.
* Klicke auf das Wort "Konfetti" und ändere es zu **Sternenfeld** (oder Sternenregen / Blizzard).

🕹️ **Teste es:** Schau auf den Simulator! Du hast jetzt einen endlos bewegten Hintergrund.

```blocks
effects.starField.startScreenEffect()
```