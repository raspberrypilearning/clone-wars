## Weltraum-Fledermaus

Um Dein Spiel etwas schwieriger zu machen, wirst Du eine Fledermaus erschaffen, die Orangen auf das Raumschiff wirft.

![eine Fledermaus wirft eine Orange auf das Raumschiff](images/bat-oranges.png)

--- task ---

Füge eine `Bat` (englisch für Fledermaus) Figur hinzu und setze ihren Rotationsstil auf **Links/Rechts**.

--- /task ---

--- task ---

Lass die `"Bat"`-Figur `fortlaufend`{:class="block3control"} am oberen Rand der Bühne von Links nach Rechts `gehen`{:class="block3motion"}.

![Fledermaus Figur](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Denke daran, Deinen Code zu testen.

--- /task ---

Wenn Du dir die Kostüme der Fledermaus (also der "Bat"-Figur) ansiehst, siehst Du, dass es vier verschiedene gibt:

![screenshot](images/invaders-bat-costume.png)

--- task ---

Verwende den `nächstes Kostüm`{:class=„block3looks“}-Block um die Fledermaus ihre Flügel schlagen zu lassen, wenn sie sich bewegt.

--- hints ---


--- hint ---

Nachdem sich die Fledermaus bewegt hat, sollte sie zum `nächsten Kostüm wechseln`{:class="block3looks"} und dann für eine kurze Zeit `warten`{:class="block3control"}.

--- /hint ---

--- hint ---

Du musst diese Blöcke zu deinem Code hinzufügen:

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

Dein Code sollte so aussehen:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce
+ next costume
+ wait (0.3) seconds
end
```

--- /hint ---

--- /hints ---

--- /task ---

Jetzt lass die Fledermaus Orangen werfen!

--- task ---

Füge einr `Orange` Figur aus der Scratch-Bibliothek hinzu.

![Screenshot](images/invaders-orange.png)

--- /task ---

--- task ---

Füge Code zu deiner Fledermaus hinzu, sodass `wenn die Flagge angeklickt wird`{:class="block3events"}, die `Bat`-Figur `fortlaufend`{:class="block3control"} für eine `zufällige`{:class="block3operators"} Zeit, zwischen `5 und 10`{:class="block3operators"} Sekunden, `wartet`{:class="block3control"} und dann von der `Orange`-Figur `einen Klon erstellt`{:class="block3control"}.

![Fledermaus Figur](images/bat-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of (Orange v)
end
```

--- /task ---

--- task ---

Füge den Code zur `Orange` hinzu, damit jeder ihrer Klone von der `Bat`-Figur nach unten Richtung Boden der Bühne fällt.

![Orange Figur](images/orange-sprite.png)

```blocks3
	when flag clicked
	hide

	when I start as a clone
	go to (Bat v)
	show
	repeat until <touching (Rand v)?
		change y by (-4)
	end
	delete this clone
```

--- /task ---

--- task ---

Füge zu der `Orange`-Figur etwas mehr zum Code hinzu, sodass ein `Orange`-Klon auch verschwindet, wenn er die `Raumschiff`-Figur trifft, um dem Spieler die Möglichkeit zum zurückzusetzen zu geben:

![Orange Figur](images/orange-sprite.png)

```blocks3
	when I receive [getroffen v]
	delete this clone
```

--- /task ---

--- task ---

Ändere den Code deiner `Raumschiff`-Figur so, dass die Figur "getroffen" wird, wenn sie eine `Hippo` Figur oder eine `Orange` Figur berührt:

![raumschiff-Figur](images/rocket-sprite.png)

```blocks3
	wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

--- /task ---

--- task ---

Teste dein Spiel. Was passiert, wenn das Raumschiff von einer fallenden Orange getroffen wird?

--- /task ---