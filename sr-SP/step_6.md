## Експлозија свемирског брода

Када нилски коњ додирне твој свемирски брод, свемирски брод би требао да експлодира!

\--- task \---

Select the `Spaceship` sprite and rename its costume 'normal'.

\--- /task \---

\--- task \---

Draw another costume of an exploding spaceship, and call the new costume 'hit'.

![снимак екрана](images/invaders-spaceship-costumes.png)

If you don't want to draw the explosion, you can select the 'Sun' costume from the Scratch library, and then use the **Color a shape** tool to change the costume's colour and face.

![снимак екрана](images/invaders-sun.png)

\--- /task \---

\--- task \---

Add some code to your `Spaceship` sprite so that it displays the 'normal' costume when the game starts, and switches to the 'hit' costume when it touches a hippo:

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
замени костим са (нормалан v)
чекај док не <touching (Hippo1 v)>?
замени костим са (ударац v)
```

\--- /task \---

\--- task \---

Test your code. Make the spaceship collide with a hippo. Does the spaceship change to the 'hit' costume?

\--- /task \---