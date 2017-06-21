## Game over

Let's add a 'game over' message at the end of the game.

+ If you haven't already, create a new variable called `lives` {.blockdata}. Your spaceship should start with 3 lives and lose a life whenever it collides with an enemy. Your game should also stop when you run out of lives. If you need help, you can use the 'Catch the Dots' project to help you.

+ Draw a new sprite called 'Game Over', using the text tool.

	![screenshot](images/invaders-game-over.png)

+ On your stage, broadcast a `game over` {.blockevents} message just before the game ends.

	```blocks
		broadcast [game over v] and wait
	```

+ Add this code to your 'Game Over' sprite, so that the message shows at the end of the game:

	```blocks
		when flag clicked
		hide

		when I receive [game over v]
		show
	```

	Because you've used a `broadcast [game over] and wait` {.blockevents} block on your stage, it will wait for the 'Game Over' sprite to be displayed before ending the game.

+ Test your game. How many points can you score? Can you think of ways to improve your game if it is too easy or too hard?
