## Exploding spaceship

When a hippo touches your spaceship, we need to make the spaceship explode! 

+ First make sure that your spaceship has 2 costumes called 'normal' and 'hit'.

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
