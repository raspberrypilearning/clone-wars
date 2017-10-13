## Flying Space-hippos

Let's add lots of flying hippos that are trying to destroy your spaceship.



+ Create a new sprite from the 'Hippo1' image in the Scratch library.

	![screenshot](images/invaders-hippo.png)

+ Set its rotation style to be left-right only, and add the following code to hide the sprite when the game starts:

	```blocks
		when flag clicked
		hide
	```

+ Create a new variable called `speed`{:class="blockdata"}, that is for the hippo sprite only.

	![screenshot](images/invaders-var.png)

	You'll know if you've done this correctly because the variable will have the name of the sprite next to it, like this:

	![screenshot](images/invaders-var-test.png)

+ The following code will create a new hippo every few seconds. **The Stage** is a good place for this code to live:

	```blocks
		when flag clicked
		forever
			wait (pick random (2) to (4)) secs
			create clone of [Hippo1 v]
		end
	```

+ When each hippo clone starts, make it move around the stage (at a random speed) until it gets hit by the lightning. Add this code **to the hippo** sprite:

	```blocks
		when I start as a clone
		set [speed v] to (pick random (2) to (4))
		go to x: (pick random (-220) to (220)) y: (150)
		show
		repeat until <touching [lightning v] ?>
			move (speed) steps
			turn right (pick random (-10) to (10)) degrees
			if on edge, bounce
		end
		delete this clone
	```

+ Test out your hippo code. You should see a new hippo clone appear every few seconds, each moving at its own speed.

	![screenshot](images/invaders-hippo-test.png)

+ Test your laser cannon. If you hit a hippo, does it vanish?

+ When a hippo touches your spaceship, we need to make the spaceship explode! To do this, first make sure that your spaceship has 2 costumes called 'normal' and 'hit'.

	![screenshot](images/invaders-spaceship-costumes.png)

	The spaceship's 'hit' costume can be made by importing the 'Sun' image from the Scratch library, and using the 'Color a shape' tool to change its colour.

	![screenshot](images/invaders-sun.png)

+ Add this code to your spaceship so that it switches costume whenever it collides with a flying hippo:

	```blocks
		when flag clicked
		forever
			switch costume to [normal v]
			wait until <touching [Hippo1 v]>?
			switch costume to [hit v]
			broadcast [hit v]
			wait (1) secs
		end
	```

+ Did you notice that you have broadcast a 'hit' message in the code above? You can use this message to make all of the hippos disappear when the spaceship is hit.

	Add this code to your hippo:

	```blocks
		when I receive [hit v]
		delete this clone
	```

+ Test out this code by starting a new game and colliding with a hippo.

	![screenshot](images/invaders-hippo-collide.png)
