## Нилски коњи који нестају

When the spaceship explodes, all the hippos should disappear so that players of the game can recover.

\--- task \---

Add code to the spaceship sprite to make it `broadcast`{:class="block3events"} the message "hit" when the `spaceship touches a hippo`{:class="block3sensing"}.

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
замени костим са (нормалан v)
чекај док не <touching (Hippo1 v)>?
замени костим са (ударац v)

+ разгласи (hit v)
```

\--- /task \---

\--- task \---

All of the `Hippo` sprite clones will receive the "hit" message, and you can instruct them to disappear when the spaceship is hit by adding this code to the `Hippo` sprite:

![лик нилског коња](images/hippo-sprite.png)

```blocks3
када примим [ударац v]
обриши овај умножак
```

\--- /task \---

\--- task \---

To check whether the new code works, click the green flag and make the spaceship collide with a hippo.

![снимак екрана](images/invaders-hippo-collide.png)

\--- /task \---

After the spaceship explodes, new `Hippo` clones appear, but the spaceship is still exploded! The spaceship needs to reset itself after being hit.

\--- task \---

Add a `wait`{:class="block3control"} block at the end of the `Spaceship` sprite's code to create a small pause before hippos begin appearing again. Then add a `forever`{:class="block3control"} block around all of your code to make the code run repeatedly.

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
понављај заувек 
  замени костим са (нормалан v)
  чекај док не <touching (Hippo1 v)>?
  замени костим са (ударац v)
  разгласи (ударац v)

+ чекај (1) секунду
end
```

\--- /task \---