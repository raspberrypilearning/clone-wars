## Blitze

Jetzt gibst Du dem Raumschiff die Möglichkeit, Blitze abzufeuern!

--- task ---

Füge die `"Lightning"` (englisch für Blitz) Figur aus der Scratch-Bibliothek hinzu.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Wenn das Spiel beginnt, sollte die `Lightning` Figur versteckt sein, bis das Raumschiff seine Laserkanonen abgefeuert hat.

Füge diesen Code zur `"Lightning"` Figur hinzu:

![Blitz-Figur](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

Im Moment ist der Blitz wirklich groß im Vergleich zum Raumschiff!

--- task ---

Füge unter dem schon vorhandenen Code, der `Lightning`-Figur, einige Blöcke hinzu um die Figur kleiner zu machen und auf den Kopf zu stellen.

![Blitz-Figur](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Jetzt sieht es so aus, als würde er mit dem spitzen Ende voran aus dem Raumschiff abgefeuert.

--- /task ---

--- task ---

Füge der `Raumschiff`-Figur Code hinzu, um jedesmal einen neuen Klon des Blitzes zu erstellen, wenn die <kbd>Leertaste</kbd> gedrückt wird.

--- hints ---


--- hint ---

`Wenn die grüne Flagge angeklickt wird`{:class="block3events"}, überprüfe `fortlaufend`{:class="block3control"} und `falls`{:class="block3control"} die `Leertaste gedrückt wird`{:class="block3sensing"} dann `erzeuge einen Klon der Lightning`{:class="block3control"} Figur.

--- /hint ---

--- hint ---

Hier sind die Blöcke die du brauchst:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (Leertaste v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

So sollte dein neuer Code aussehen:

![raumschiff-Figur](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (Leertaste v) pressed?> then
		create clone of (Lightning v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Immer wenn das Spiel einen Klon der `Lightning` Figur erstellt, sollte der Klon erscheinen und sich dann nach oben bewegen, bis er den oberen Bereich der Bühne erreicht. Dann sollte der Klon verschwinden.

Füge diesen Code der `Lightning` Figur hinzu, sodass Klone davon nach oben verschoben werden, bis sie den Rand der Bühne berühren und anschließend gelöscht werden.

![Blitz-Figur](images/lightning-sprite.png)

```blocks3
	when I start as a clone
	go to (Raumschiff v)
    show
	repeat until <touching (Rand v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

Drücke die <kbd>Leertaste</kbd>, um zu testen, ob sich der Blitz richtig bewegt.

--- /task ---