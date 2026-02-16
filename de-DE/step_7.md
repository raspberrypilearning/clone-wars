## Flusspferde, die verschwinden

Wenn das Raumschiff explodiert, sollten alle Flusspferde verschwinden, damit sich die Spieler des Spiels erholen können.

--- task ---

Füge der Raumschiff-Figur Code hinzu, damit sie eine `Nachricht "getroffen" an alle sendet`{:class="block3events"}, wenn das Raumschiff `ein Hippo berührt`{:class="block3sensing"}.

![raumschiff-Figur](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (getroffen v)
+ broadcast (getroffen v)
```

--- /task ---

--- task ---

Alle `Hippo` Figur-Klone empfangen die Nachricht "getroffen", und Du kannst sie anweisen zu verschwinden, wenn das Raumschiff getroffen wird, indem Du der `Hippo` Figur diesen Code hinzufügst:

![Hippo Figur](images/hippo-sprite.png)

```blocks3
when I receive [getroffen]
delete this clone
```

--- /task ---

--- task ---

Um zu überprüfen, ob der neue Code funktioniert, klicke auf die grüne Flagge und lass das Raumschiff mit einem Flusspferd kollidieren.

![screenshot](images/invaders-hippo-collide.png)

--- /task ---

Nachdem das Raumschiff explodiert ist, erscheinen neue `Hippo` Klone, aber das Raumschiff ist immer noch explodiert! Das Raumschiff muss sich nach einem Treffer selbst zurücksetzen.

--- task ---

Füge am Ende des Codes der `Raumschiff` Figur einen `warte`{:class="block3control"}-Block hinzu, um eine kleine Pause zu haben, bevor wieder Flusspferde angezeigt werden. Füge dann einen `fortlaufend`{:class="block3control"}-Block um den gesamten Code hinzu, damit der Code wiederholt ausgeführt wird.

![raumschiff-Figur](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (getroffen v)
broadcast (getroffen v)
+ wait (1) seconds
end
```

--- /task ---