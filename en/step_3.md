

## Making a Spaceship




Let's make a spaceship that will defend the Earth!



+ Start a new Scratch project and delete the cat sprite so that your project is empty. You can find the online Scratch editor at <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Add the 'stars' backdrop and the 'Spaceship' sprite to your project. Shrink the spaceship and move it near the bottom of the screen.

	![screenshot](images/invaders-sprites.png)

+ Add code to move your spaceship to the left when the left arrow key is pressed. You'll need to use these blocks:

	```blocks
		when flag clicked
		forever
			if <key [left arrow v] pressed?> then
				change x by (-4)
			end
		end
	```

+ Add code to move your spaceship to the right when the right arrow key is pressed.

+ Test your project to see whether you can control your spaceship with the arrow keys.




