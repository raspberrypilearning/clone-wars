## Blitze

Jetzt geben Sie dem Raumschiff die Möglichkeit, Blitzschläge abzufeuern!

\--- task \---

Fügen Sie den ` Blitz hinzu ` Sprite aus der Scratch-Bibliothek.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Wenn das Spiel beginnt, sollte das `Lightning` Sprite ausgeblendet sein, bis das Raumschiff seine Laserkanonen abgefeuert hat.

Fügen Sie diesen Code zum `Lightning` Sprite hinzu:

![Blitz-Sprite](images/lightning-sprite.png)

```blocks3
Wenn grüne Flagge geklickt 
verstecken
```

\--- /task \---

Im Moment ist der Blitz wirklich groß im Vergleich zum Raumschiff!

\--- task \---

Fügen Sie unterhalb des Codes, über den das `Lightning` Sprite bereits verfügt, einige Blöcke hinzu, um das Sprite zu verkleinern und umzudrehen.

![Blitz-Sprite](images/lightning-sprite.png)

```blocks3
Größe einstellen auf (25)%
Punkt in Richtung (-90)
```

Jetzt sieht es so aus, als würde es ein spitzes Ende abfeuern - zuerst aus dem Raumschiff.

\--- /task \---

\--- task \---

Fügen Sie dem Sprite `Spaceship` einen neuen Code hinzu, um einen neuen Klon des Blitzes zu erstellen, wenn die Taste <kbd>Space</kbd> gedrückt wird.

\--- hints \---

\--- hint \---

`Wenn die grüne Flagge angeklickt wird`{: class = "block3control"}, überprüfen Sie `für immer`{: class = "block3control"} `wenn`{: class = "block3control"} die `-Leertaste gedrückt wird`{: class = "block3sensing"} und in diesem Fall `einen Klon des Lightning`Sprites {: class = "block3control"} erstellen.

\--- /hint \---

\--- hint \---

Hier sind die Blöcke, die Sie benötigen:

```blocks3
wenn <> dann
ende

für immer
ende

erstelle einen Klon von (Lightning v)

<key (space v) pressed?>

wenn die Flagge angeklickt wird
```

\--- /hint \---

\--- hint \---

So sollte Ihr neuer Code aussehen:

![Raketen-Sprite](images/rocket-sprite.png)

```blocks3
Wenn das Flag für immer auf
geklickt hat, wird
    wenn <key (space v) pressed?> dann
        ein Klon von (Lightning v)
    Ende
Ende erstellt
```

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Immer wenn das Spiel einen `Lightning` Sprite-Klon erstellt, sollte der Klon erscheinen und sich dann nach oben bewegen, bis er den oberen Bereich der Bühne erreicht. Dann sollte der Klon verschwinden.

Fügen Sie diesen Code dem `Lightning` Sprite hinzu, sodass Klone davon nach oben verschoben werden, bis sie den Rand der Bühne berühren. Anschließend werden sie gelöscht.

![Blitz-Sprite](images/lightning-sprite.png)

```blocks3
    Wenn ich als Klon beginne
    gehe zu (Raumschiff v)
    zeige
    wiederhole bis <touching (edge v) ?>
        ändere y um (10)

    lösche diesen Klon
```

\--- /task \---

\--- task \---

Drücken Sie die <kbd>-Leertaste</kbd> , um zu testen, ob sich der Blitz richtig bewegt.

\--- /task \---