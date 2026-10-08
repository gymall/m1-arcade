# Skill: Töne & Musik (Game-Juice)

## Schritt 1: Hintergrundmusik
Ein Spiel ohne Ton ist wie ein Kino ohne Lautsprecher. Musik sorgt für die richtige Stimmung!

* Gehe zur Kategorie **Musik** (pink).
* Ziehe den Block `spiele Melodie im Hintergrund ab` in deinen grünen Start-Block.
* Klicke auf das graue Quadrat und komponiere deine eigene Musik oder wähle oben den Reiter "Galerie" für fertige Lieder.

```blocks
music.playMelody("E B C5 A B G A F ", 120)
```

## Schritt 2: Soundeffekte (Audio-Feedback)
Musik ist toll, aber der Spieler braucht auch **Audio-Feedback**. Das bedeutet: Wenn im Spiel etwas Wichtiges passiert (z.B. eine Münze einsammeln, ein Treffer oder ein Sprung), muss ein passendes Geräusch kommen.

* Suche in deinem eigenen Code die Stelle, wo etwas Wichtiges passiert (z.B. in deiner Wenn-Dann-Kollision, wenn Punkte gesammelt werden).
* Gehe zu **Musik** und ziehe den Block `spiele Sound ba ding ab` genau an diese Stelle. 
* *Tipp: Klicke auf "ba ding", um andere Geräusche zu finden.*

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    music.playSoundEffect(music.createSoundEffect(WaveShape.Sine, 5000, 0, 255, 0, 500, SoundExpressionEffect.None, InterpolationCurve.Linear), SoundExpressionPlayMode.UntilDone)
})
```

## Schritt 3: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem man sieht, wo du Musik oder einen Soundeffekt in deinen Code eingebaut hast.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Gamedesign (Feedback):** Ein Sound beim Einsammeln von Punkten nennt man "Audio-Feedback". Warum ist dieses Feedback für den Spieler wichtig? (Stell dir vor, du spielst *Super Mario* und das Ping-Geräusch bei den Münzen fehlt komplett).
2. **Die Lebenswelt:** Nenne ein Beispiel aus dem echten Leben (außerhalb von Videospielen), bei dem Töne (Audio-Feedback) absichtlich genutzt werden, um Menschen zu zeigen, dass etwas geklappt hat oder es ein Problem gibt (z.B. an der Supermarktkasse oder beim Auto).
