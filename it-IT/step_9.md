## Pipistrelli spaziali

Per rendere il tuo gioco un po' più difficile, creerai un pipistrello che lancia arance sulla navicella.

![un pipistrello che lancia un'arancia all'astronave](images/bat-oranges.png)

\--- task \---

Aggiungi uno sprite `Pipistrello` e imposta la sua rotazione su **sinistra-destra**.

\--- /task \---

\--- task \---

Rendi lo sprite `Pipistrello` `movimentato`{:class="block3motion"} da sinistra a destra nella parte superiore dello Stage `per sempre`{:class="block3control"}.

![sprite pipistrello](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Ricorda di provare il tuo codice.

\--- /task \---

Se guardi i costumi del pipistrello, puoi vedere che ne ha quattro diversi:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

Usa il blocco `prossimo costumee`{:class="block3looks"} per far si che batti le ali quando si muove.

\--- hint \---

\--- hint \---

Dopo che il pipistrello è stato spostato, dovrebbe mostrare il `costume successivo`{:class="block3look"} e poi `attendere`{:class="block3control"} per un breve periodo.

\--- /hint \---

\--- hint \---

Devi aggiungere questi blocchi al tuo codice:

```blocks3
wait (0.3) seconds

next costume
```

\--- /hint \---

\--- hint \---

You code should look like this:

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
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---