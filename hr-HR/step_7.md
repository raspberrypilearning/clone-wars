## Nilski konji koji nestaju

Kad svemirski brod eksplodira, svi nilski konji trebali bi nestati tako da igrači mogu ponovno započeti igru.

\--- task \---

Add code to the spaceship sprite to make it `broadcast`{:class="block3events"} the message "hit" when the `spaceship touches a hippo`{:class="block3sensing"}.

![lik rakete](images/rocket-sprite.png)

```blocks3
kada je kliknuta zelena zastava
promijeni kostim u (normalan)
čekaj do <dodiruje (Hippo1 v)>
promijeni kostim u (pogođen)

+ pošalji (pogođen v)
```

\--- /task \---

\--- task \---

Svi klonovi lika `Nilski konj` primit će poruku "pogodak" i dodajući ove naredbe liku `Nilski konj` naređujete im da nestanu kada je svemirski brod pogođen:

![hippo sprite](images/hippo-sprite.png)

```blocks3
kada primim [pogodak v]
izbriši klona
```

\--- /task \---

\--- task \---

To check whether the new code works, click the green flag and make the spaceship collide with a hippo.

![screenshot](images/invaders-hippo-collide.png)

\--- /task \---

After the spaceship explodes, new `Hippo` clones appear, but the spaceship is still exploded! The spaceship needs to reset itself after being hit.

\--- task \---

Add a `wait`{:class="block3control"} block at the end of the `Spaceship` sprite's code to create a small pause before hippos begin appearing again. Then add a `forever`{:class="block3control"} block around all of your code to make the code run repeatedly.

![lik rakete](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
broadcast (hit v)

+ wait (1) seconds
end
```

\--- /task \---