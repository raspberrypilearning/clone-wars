## Weltraum-Flusspferde

Jetzt wirst Du viele fliegende Flusspferde hinzufügen, die versuchen dein Raumschiff zu zerstören.

--- task ---

Erstelle eine neue Figur mit dem "Hippo1" (englisch für Flusspferd) Bild aus der Scratch-Bibliothek. **Verkleinere** sie um die `Hippo` Figur auf eine ähnliche Größe wie das `Raumschiff` zu bringen.

![screenshot](images/invaders-hippo.png)

--- /task ---

--- task ---

Stelle den Rotationsstil der `Hippo` Figur auf **Links/Rechts** um.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

Füge Code hinzu, um die `Hippo` Figur zu Beginn des Spiels zu verstecken.

![Hippo Figur](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

Füge der Bühne Code hinzu, um alle paar Sekunden einen neuen `Hippo` Klon zu erstellen.

--- hints ---


--- hint ---

Wenn die `grüne Flagge angeklickt wird`{:class="block3events"}, `warte`{:class="block3control"} `wiederholt`{:class="block3control"} `zwischen 2 und 4 Sekunden`{:class="block3operators"} und dann `erstelle einen Klon der Hippo-Figur`{:class="block3control"}.

--- /hint ---

--- hint ---

Hier sind die Blöcke die du brauchst:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

So sollte dein Code aussehen:

![Bühnen Figur](images/stage-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (2) to (4)) secs
	create clone of (Hippo1 v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

Jeder neue Hippo-Klon sollte an einer zufälligen `x` Position erscheinen und jeder Klon sollte eine zufällige Geschwindigkeit haben.

--- task ---

Erstelle eine neue Variable mit dem Namen `Geschwindigkeit`{:class="block3variables"}, die nur für die `Hippo` Figur gilt.

[[[generic-scratch3-add-variable]]]

Wenn Du das richtig gemacht hast, steht der Name der Figur neben der Variable, so wie hier:

![screenshot](images/invaders-var-test.png)

--- /task ---

--- task ---

Für jeden `Hippo` Klon der startet, wähle eine zufällige Geschwindigkeit und eine zufällige Startposition. Zeige dann den Klon auf dem Bildschirm an.

```blocks3
when I start as a clone
set [Geschwindigkeit v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

Teste deinen Code. Erscheint alle paar Sekunden ein neues Nilpferd?

--- /task ---

Im Moment bewegen sich die Nilpferde nicht.

--- task ---

Jedes Nilpferd sollte sich zufällig bewegen, bis es von einem Blitz getroffen wird. Füge dazu den folgenden Code unter die Blöcke ein, die bereits im Skript der `Hippo` Figur enthalten sind:

```blocks3
repeat until <touching (lightning v) ?>
	move (Geschwindigkeit :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```	

--- /task ---

--- task ---

Teste deinen Code erneut. Du solltest alle paar Sekunden einen neuen Hippo-Klon sehen, und jeder Klon sollte sich mit einer anderen Geschwindigkeit bewegen.

--- no-print ---

![screenshot](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

Teste jetzt die Laserkanone des Raumschiffs. Wenn ein Blitz ein Flusspferd trifft, verschwindet das Flusspferd?

--- /task ---