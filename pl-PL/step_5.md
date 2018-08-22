## Latające kosmo-hipopotamy

Dodajmy wiele latających hipopotamów, które spróbują zniszczyć twój statek kosmiczny.

+ Create a new sprite with the `Hippo1` image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![zrzut ekranu](images/invaders-hippo.png)

+ Set the `Hippo` sprite's rotation style to be left-right only.

[[[generic-scratch-sprite-rotation-style]]]

+ Dodaj kod, aby ukryć duszka `Hipopotam` kiedy gra się zaczyna.

\--- hints \--- \--- hint \--- Kod do tego jest dokładnie taki sam jak kod, którego używasz, aby ukryć duszka `Błyskawica` kiedy gra się zaczyna. \--- /hint \--- \--- hint \--- To jest kod, którego będziesz potrzebować:

```blocks
kiedy kliknięto zieloną flagę
ukryj
```

\--- /hint \--- \--- /hints \---

+ Switch to the Stage by clicking on it in the bottom panel.

+ Add some code to the Stage to create a new hippo every few seconds.

\--- hints \--- \--- hint \--- When the green flag is clicked: Repeatedly...

+ Zaczekaj od 2 do 4 sekund
+ Stwórz klona duszka hipopotama

\--- /hint \--- \--- hint \--- Here are the blocks you will need: ![Clone hippo hint](images/clone-hippo-hint.png)

\--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of [Hippo1 v]
end
```

\--- /hint \--- \--- /hints \---

+ Switch back to the `Hippo` sprite.

Każdy nowy hipopotam powinien pojawić się w przypadkowej pozycji x i każdy powinien mieć losową prędkość.

+ Create a new variable called `speed`{:class="blockdata"} that is for the `Hippo` sprite only.

[[[generic-scratch-add-variable]]]

Będziesz wiedział, że zrobiłeś to poprawnie, gdy zobaczysz, że zmienna ma nazwę ikonki obok niej, tak jak poniżej:

![zrzut ekranu](images/invaders-var-test.png)

+ When each hippo clone starts, pick a random speed and starting place before showing it on the screen.

```blocks
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

+ Test your code by clicking the green flag. Does a new hippo appear every few seconds? At the moment your hippos won't move.

+ The hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks you just added:

```blocks
repeat until <touching [lightning v] ?>
    move (speed) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

+ Test out your hippo code. You should see a new hippo clone appear every few seconds, each moving at its own speed.
    
    ![zrzut ekranu](images/hippo-clones.gif)

+ Test your laser cannon. If you hit a hippo, does it vanish?