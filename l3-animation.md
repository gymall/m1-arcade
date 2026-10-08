# Skill: Animationen (Figuren bewegen)

## Schritt 1: Leben einhauchen
Eine Figur, die starr über den Bildschirm rutscht, wirkt wie eine Statue. Wir wollen ihr Beine machen! Eine Animation im Computer ist nichts anderes als ein **Daumenkino**: Viele Bilder werden ganz schnell hintereinander abgespielt.

* Klicke im Menü in der Mitte auf **Erweitert** (unten), damit mehr Kategorien erscheinen.
* Gehe zur Kategorie **Animation** (türkis).
* Ziehe den Block `animiere mySprite` in deinen Code (z.B. direkt in den Start-Block).

```blocks
let mySprite: Sprite = null
animation.runImageAnimation(
mySprite,
[img`
    . . . . . . . . . . . . . . . .
    `],
500,
true
)
```

## Schritt 2: Das Daumenkino zeichnen
* Klicke auf das Plus-Symbol `+` in dem Animations-Block, um ein weiteres Bild hinzuzufügen.
* Klicke auf das erste Bild und zeichne deine Figur.
* Klicke auf das zweite Bild und zeichne die Figur mit leicht veränderten Beinen oder Armen.
* **Die Zeit:** Stelle die Zeit (z.B. `500 ms`) ein. Das ist die Geschwindigkeit, wie schnell das Daumenkino umgeblättert wird.
* **Die Schleife:** Stelle den Schalter auf `AN`, damit sich die Animation immer wiederholt.

## Schritt 3: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem dein Animations-Block zu sehen ist.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Die Lebenswelt:** Eine Computer-Animation funktioniert genau wie ein **Daumenkino** oder ein Zeichentrickfilm. Erkläre in deinen eigenen Worten, wie dabei im Gehirn die Illusion von echter Bewegung entsteht.
2. **Gamedesign:** Warum machen Animationen ein Spiel besser? Wie wirkt ein Videospiel auf dich, wenn sich die Beine der Figuren beim Laufen nicht bewegen würden?
