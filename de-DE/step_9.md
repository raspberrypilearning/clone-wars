## Weltraum-Fledermaus

Um Dein Spiel etwas schwieriger zu machen, wirst Du eine Fledermaus erschaffen, die Orangen auf das Raumschiff wirft.

![eine Fledermaus wirft eine Orange auf das Raumschiff](images/bat-oranges.png)

\--- task \---

Füge eine `Bat` (englisch für Fledermaus) Figur hinzu und setze ihren Rotationsstil auf **Links/Rechts**.

\--- /task \---

\--- task \---

Lass die `"Bat"`-Figur `fortlaufend`{:class="block3control"} am oberen Rand der Bühne von Links nach Rechts `gehen`{:class="block3motion"}.

![Fledermaus Figur](images/bat-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
setze Größe auf (50)
wiederhole fortlaufend 
  gehe (10) er Schritt
  pralle vom Rand ab
end
```

Denke daran, Deinen Code zu testen.

\--- /task \---

Wenn Du dir die Kostüme der Fledermaus (also der "Bat"-Figur) ansiehst, siehst Du, dass es vier verschiedene gibt:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

Verwende den `nächstes Kostüm`{:class=„block3looks“}-Block um die Fledermaus ihre Flügel schlagen zu lassen, wenn sie sich bewegt.

\--- hints \---

\--- hint \---

Nachdem sich die Fledermaus bewegt hat, sollte sie zum `nächsten Kostüm wechseln`{:class="block3looks"} und dann für eine kurze Zeit `warten`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Du musst diese Blöcke zu deinem Code hinzufügen:

```blocks3
warte (0.3) Sekunden

wechsle zum nächsten Kostüm
```

\--- /hint \---

\--- hint \---

You code should look like this:

```blocks3
Wenn die grüne Flagge angeklickt
setze Größe auf (50)
wiederhole fortlaufend 
gehe (10) er Schritt
pralle vom Rand ab
  
+ wechsle zum nächsten Kostüm
+ warte (0.3) Sekunden
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
wiederhole fortlaufend 
  warte (Zufallszahl von (5) bis (10)) Sekunden
  erzeuge Klon von (Orange v)
end
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt
    verstecke dich

    Wenn ich als Klon entstehe
    gehe zu (Bat v)
    zeige dich
    wiederhole bis <wird (Rand v) berührt?> 
        ändere y um (-4)
    end
    lösche diesen Klon
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    Wenn ich [getroffen v] empfange
    lösche diesen Klon
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    warte bis <<wird (Hippo1 v) berührt?> oder <wird (Orange v) berührt?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---