# Skill: Zählschleifen (Genau abzählen)

## Schritt 1: Zählen lassen
Du hast schon die Endlos-Schleife kennengelernt, die Gegner immer wieder spawnt. Manchmal wollen wir aber, dass etwas *genau 5-mal* oder *genau 10-mal* passiert (und dann stoppt).

Dafür gibt es in der Informatik die **Zählschleife** (auch FOR-Schleife genannt). Sie zählt für uns mit!

## Schritt 2: Genau 5 Münzen spawnen
Wir wollen, dass am Start des Spiels genau 5 Münzen auf dem Bildschirm verteilt werden. Nicht mehr und nicht weniger.

* Gehe zu **Schleifen** (grün) und ziehe den Block `für Index von 0 bis 4` in deinen Start-Block. *(Achtung: Informatiker fangen oft bei 0 an zu zählen. Von 0 bis 4 sind genau 5 Durchläufe!)*
* Hole aus **Sprites** den Block `setze mySprite auf` und lege ihn in die Schleife. Nenne ihn "Münze".
* Ziehe auch den Block `setze mySprite x auf 0` aus **Sprites** in die Schleife.

## Schritt 3: Zufällig verteilen
Jetzt sorgen wir dafür, dass die 5 Münzen kreuz und quer auf dem Bildschirm auftauchen.

* Ändere das `x` im Block auf `position (x, y)`.
* Gehe zu **Mathematik** (lila) und ziehe zwei `wähle eine zufällige Zahl` Blöcke in die X- und Y-Werte. 
* Trage für X `0 bis 160` und für Y `0 bis 120` ein.

```blocks
let Münze: Sprite = null
for (let index = 0; index <= 4; index++) {
    Münze = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Food)
    Münze.setPosition(randint(0, 160), randint(0, 120))
}
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot von deiner eigenen Zählschleife hoch.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Was ist der Unterschied zwischen der Endlosschleife ("bei Spiel-Update alle 500 ms") und der Zählschleife? 
2. **Die Lebenswelt:** Nenne ein Beispiel aus deinem Alltag oder aus einem Brettspiel, bei dem du eine Zählschleife durchführst (also eine bestimmte Aktion exakt so oft wiederholst, bis eine bestimmte Zahl erreicht ist, z. B. beim Kartenspielen oder beim Sport).
