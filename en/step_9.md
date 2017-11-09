## Game over

Let's add a 'game over' message at the end of the game.

+ If you haven't already, create a new variable called `lives`{:class="blockdata"}.

Your spaceship should start with three lives and lose a life whenever it touches a hippo or an orange. Your game should also stop when you run out of lives. If you need help, you can use the [Catch the dots](https://codeclubprojects.org/en-GB/scratch/catch-the-dots/) project to help you.

+ Draw a new sprite called `Game Over` using the **text** tool.

![screenshot](images/invaders-game-over.png)

+ On your **Stage**, broadcast a `game over`{:class="blockevents"} message just before the game ends.

```blocks
broadcast [game over v] and wait
```

+ Add this code to your `Game Over` sprite, so that the message shows at the end of the game:

```blocks
when flag clicked
hide

when I receive [game over v]
show
```

Because you've used a `broadcast [game over] and wait`{:class="blockevents"} block on your stage, it will wait for the `Game Over` sprite to be displayed before ending the game.

+ Test your game. How many points can you score? If it is too easy or too hard, can you think of ways to improve your game?
