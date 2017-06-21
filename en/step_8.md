## Fruit Bats!

Let's make a fruit bat that throws oranges at your spaceship.

+ Firstly, make a new bat sprite that will `move` {.blockmotion} across the top of the stage `forever` {.blockcontrol}. Remember to test out your code.

	![screenshot](images/invaders-bat.png)

+ If you look at the bat's costumes, you'll see that it already has 2:

	![screenshot](images/invaders-bat-costume.png)

	Use the `next costume` {.blocklooks} block to make the bat flap its wings as it moves.

+ Create a new 'Orange' sprite from the Scratch library

	![screenshot](images/invaders-orange.png)

+ Add code to your bat, so that it creates a new orange clone every few seconds.

	```blocks
		when flag clicked
		forever
			wait (pick random (5) to (10)) secs
			create clone of [Orange v]
		end
	```

+ Click on your orange sprite and add this code to make each orange clone drop down the stage from the bat towards the spaceship:

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

		when I receive [hit v]
		delete this clone
	```

+ In your spaceship sprite, you'll need to modify your code so that you are hit if you touch a hippo or an orange:

	```blocks
		wait until < <touching [Hippo1 v]?> or <touching [Orange v]?>>
	```

+ Test your game. What happens if you get hit by a falling orange?
