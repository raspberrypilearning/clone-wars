## Vliegende ruimte-nijlpaarden

Nu ga je veel vliegende nijlpaarden (flying hippos) toevoegen die proberen jouw spaceschip te vernietigen.

\--- task \---

Maak een nieuwe sprite met de 'Hippo1' afbeelding in de Scratch bibliotheek. Gebruik de **grootte** instelling om de `Hippo1` sprite even groot als de `Spaceship` sprite te maken.

![screenshot](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Stel de `Hippo` sprite's draaistijl in op **links-rechts**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Voeg code toe om als het spel begint de ` Hippo` Sprite te verbergen.

![hippo sprite](images/hippo-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt 
 verdwijn
```

\--- /task \---

\--- task \---

Voeg wat code toe aan de achtergrond om elke paar seconden een nieuwe `Hippo` (nijlpaard) te maken.

\--- hints \---

\--- hint \---

Wanneer de `groene vlag wordt geklikt`{:class="block3events"}, `herhaal`{:class="block3control"} `wacht`{:class="block3control"} `tussen 2 en 4 seconden`{:class="block3operators"} en vervolgens `maak een kloon van mijzelf`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Dit zijn de blokken die je nodig hebt:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- /hint \---

\--- hint \---

This is what your code should look like:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Each new hippo clone should appear at a random `x` position, and every clone should have a random speed.

\--- task \---

Create a new variable called `speed`{:class="block3variables"} that is for the `Hippo` sprite only.

[[[generic-scratch3-add-variable]]]

When you've done this correctly, the variable has the name of the sprite next to it, like this:

![screenshot](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

```blocks3
wanneer ik als kloon start
maak [snelheid v] (willekeurig getal tussen (2) tot (4)) 
ga naar x: (kies willekeurig (-220) tot (220)) y: (150) 
verschijn
```

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![screenshot](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---