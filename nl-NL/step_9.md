## Ruimte-vleermuis

Om het spel een beetje moeilijker te maken, maken we een vleermuis die sinaasappels naar het ruimteschip gooit.

![een vleermuis die een sinaasappel naar het ruimteschip gooit](images/bat-oranges.png)

\--- task \---

Voeg een `Bat (vleermuis)` sprite toe en zet de draaistijl op **links-rechts**.

\--- /task \---

\--- task \---

Zorg ervoor dat de `vleermuis` sprite zich van links naar rechts aan de bovenkant van het speelveld `verplaatst`{:class="block3motion"} door middel van een `herhaal`{:class="block3control"} blok.

![vleermuis sprite](images/bat-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
maak grootte (50) %
herhaal 
  neem (10) stappen
  keer om aan de rand
einde
```

Vergeet niet om je code te testen.

\--- /task \---

Als je naar de uiterlijken van de vleermuis kijkt, zie je dat deze vier verschillende heeft:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

Gebruik het `Volgend uiterlijk`{:class="block3looks"} blok om de vleermuis te laten vliegen als het beweegt.

\--- hints \---

\--- hint \---

Nadat de vleermuis is verplaatst, moet het het `volgend uiterlijk`{:class="block3look"} weergeven en vervolgens `wachten`{:class="block3control"} voor een korte tijd.

\--- /hint \---

\--- hint \---

Je moet deze blokken toevoegen aan jouw code:

```blocks3
wacht (0.3) sec.

volgend uiterlijk
```

\--- /hint \---

\--- hint \---

Your code should look like this:

```blocks3
wanneer groene vlag wordt aangeklikt
maak grootte (50) %
herhaal 
 neem (10) stappen
 keer om aan de rand

 + volgend uiterlijk
 + wacht (0.3) sec.
einde
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
wanneer groene vlag wordt aangeklikt
herhaal 
  wacht (willekeurig getal tussen (5) en (10)) sec.
  maak een kloon van (Orange v)
einde
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    wanneer groene vlag wordt aangeklikt
verdwijn

wanneer ik als kloon start
ga naar (Bat v)
verschijn
herhaal tot <raak ik (rand v)>?
  verander y met (-4)
einde
verwijder deze kloon
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    wanneer ik signaal [hit v] ontvang
verwijder deze kloon
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wacht tot < <raak ik (Hippo1 v)?> of <raak ik (Orange v)>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---