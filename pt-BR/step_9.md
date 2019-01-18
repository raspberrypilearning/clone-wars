## Space-bat

To make your game a bit harder, you are going to create a bat that throws oranges at the spaceship.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

\--- task \---

Add a `Bat` sprite and set its rotation style to **left–right**.

\--- /task \---

\--- task \---

Make the `Bat` sprite `move`{:class="block3motion"} from left to right at the top of the Stage `forever`{:class="block3control"}.

![bat sprite](images/bat-sprite.png)

![blocks_1546522883_9902587](images/blocks_1546522883_9902587.png)

Remember to test your code.

\--- /task \---

If you look at the bat's costumes, you can see that it has four different ones:

![captura de tela](images/invaders-bat-costume.png)

\--- task \---

Use the `next costume`{:class="block3looks"} block to make the bat flap its wings as it moves.

\--- dica \---

\--- hint \---

After the bat has moved, it should show the `next costume`{:class="block3looks"} and then `wait`{:class="block3control"} for a short time.

\--- /hint \---

\--- hint \---

You need to add these blocks to you code:

![blocks_1546522885_6359174](images/blocks_1546522885_6359174.png) \--- /hint \---

\--- hint \--- You code should look like this:

![blocks_1546522887_2722294](images/blocks_1546522887_2722294.png) \--- /hint \---

\--- /hints \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![captura de tela](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

![blocks_1546522888_8938003](images/blocks_1546522888_8938003.png)

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

![blocks_1546522890_544698](images/blocks_1546522890_544698.png)

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

![blocks_1546522892_2124374](images/blocks_1546522892_2124374.png)

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

![blocks_1546522893_821553](images/blocks_1546522893_821553.png)

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---