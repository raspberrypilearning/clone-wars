## Owocowy nietoperz

Aby uczynić grę była nieco trudniejszą, zróbmy owocowego nietoperza, który rzuca pomarańczami w statek kosmiczny.

+ Add a `Bat` sprite and set its rotation style to **left–right** only.

+ Make the `Bat` sprite `move`{:class="blockmotion"} from side to side across the top of the Stage `forever`{:class="blockcontrol"}. Remember to test out your code.

![zrzut ekranu](images/invaders-bat.png)

\--- hints \--- \--- hint \--- When the flag is clicked, the `Bat` sprite should forever

+ przesuń o 10 kroków
+ jeśli osiągnie krawędź, odbij się \--- /hint \--- \--- hint \--- To jest kod, którego potrzebujesz:

```blocks
kiedy kliknięto flagę
zawsze
    przesuń o (10) kroków
    jeśli na krawędzi, odbij się
koniec
```

\--- /hint \--- \--- /hints \---

Jeśli spojrzysz na kostiumy nietoperza, to zobaczysz, że ma już dwa:

![zrzut ekranu](images/invaders-bat-costume.png)

+ Use the `next costume`{:class="blocklooks"} block to make the bat flap its wings as it moves.

\--- hints \--- \--- hint \--- After the bat has moved, it should show the `next costume`{:class="blocklooks"} and then `wait`{:class="blockcontrol"} for a short time. \--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
next costume
wait (0.3) secs
```

\--- /hint \--- \--- hint \--- Here is the full code with the new code added:

```blocks
when flag clicked
forever
    move (10) steps
    if on edge, bounce
    next costume
    wait (0.3) secs
end
```

\--- /hint \--- \--- /hints \---

Now let's make the bat throw oranges.

+ Add a new `Orange` sprite from the Scratch library.

![zrzut ekranu](images/invaders-orange.png)

+ Add code to your bat so that, when the flag is clicked, it waits for a random time between 5 and 10 seconds and then creates a clone of the `Orange` sprite.

\--- hints \--- \--- hint \--- Look at the code you wrote when you created the `Lightning` sprite. The code you need now is very similar, except instead of an orange appearing when you press the **space** bar, it should appear after you `wait`{:class="blockcontrol"} for `5-10`{:class="blockoperators"} seconds. \--- /hint \--- \--- hint \--- `When the flag is clicked`{:class="blockcontrol"}, the `Bat` sprite should `forever`{:class="blockcontrol"}

+ `wait`{:class="blockcontrol"} for a `random`{:class="blockoperators"} time between `5-10`{:class="blockoperators"} seconds
+ `create a clone`{:class="blockcontrol"} of the `Orange` sprite \--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of [Orange v]
end
```

\--- /hint \--- \--- /hints \---

+ Click on your `Orange` sprite and add some code to make each `Orange` sprite clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

\--- hints \--- \--- hint \--- This code you want is almost the same as the code inside the `Lightning` sprite, except that the `Orange` sprite should `go to`{:class="blockmotion"} the `Bat` sprite's position, and it should use the `change y by`{:class="blockcontrol"} block to move downwards instead of upwards. \--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
    when flag clicked
    hide

    when I start as a clone
    go to [Bat1 v]
    show
    repeat until <touching [edge v]?
        change y by (-4)
    end
    delete this clone

```

\--- /hint \--- \--- /hints \---

+ Add some more code to the `Orange` sprite so that when the `Spaceship` sprite is hit, it also disappears to give the player a chance to reset:

```blocks
    when I receive [hit v]
    delete this clone
```

+ You'll also need to modify the code in your `Spaceship` sprite so that it is hit when it touches a `Hippo` sprite or an `Orange` sprite:

```blocks
    wait until < <touching [Hippo1 v]?> or <touching [Orange v]?>>
```

+ Przetestuj swoją grę. Co się stanie, jeśli uderzy cię spadająca pomarańcza?