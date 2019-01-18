## Space-hippos

Now you're going to add lots of flying hippos that try to destroy your spaceship.

\--- task \---

Create a new sprite with the 'Hippo1' image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![zrzut ekranu](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Set the `Hippo` sprite's rotation style to **left-right**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Dodaj kod, aby ukryć duszka `Hipcio` kiedy gra się zaczyna.

![hippo sprite](images/hippo-sprite.png)

![blocks_1546522869_3620155](images/blocks_1546522869_3620155.png) \--- /task \---

\--- task \---

Add some code to the Stage to create a new `Hippo` clone every few seconds.

\--- wskazówka \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} and then `create a clone of the Hippo sprite`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Here are the blocks you need:

![blocks_1546522870_9668188](images/blocks_1546522870_9668188.png)

\--- /wskazówka \---

\--- hint \---

This is what your code should look like:

![stage sprite](images/stage-sprite.png)

![blocks_1546522872_610604](images/blocks_1546522872_610604.png)

\--- /wskazówka \---

\--- /wskazówka \---

\--- /task \---

Each new hippo clone should appear at a random `x` position, and every clone should have a random speed.

\--- task \---

Create a new variable called `speed`{:class="block3variables"} that is for the `Hippo` sprite only.

[[[generic-scratch3-add-variable]]]

When you've done this correctly, the variable has the name of the sprite next to it, like this:

![zrzut ekranu](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

![blocks_1546522874_2438061](images/blocks_1546522874_2438061.png)

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

![blocks_1546522875_874299](images/blocks_1546522875_874299.png)

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![zrzut ekranu](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---