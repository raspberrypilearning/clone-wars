## Lightning bolts

Let's give the spaceship the ability to fire lightning bolts!

+ Add the 'Lightning' sprite from the Scratch library.  

+ When the game is started, the lightning should be hidden until the spaceship fires its laser cannons, so add this code to the lightning bolt sprite:

```blocks
when green flag clicked
hide
```

At the moment you have a pretty gigantic lightning bolt for the spaceship to fire! Let's make the lightning much smaller and turn it upside down so that it fires pointy end first out of the spaceship.

+ Add some more code underneath the code you just added to make it smaller

```blocks
set size to (25) %
point in direction (-90 v)
```

+ Swap to the **spaceship** sprite by clicking on it in the 'Sprites' panel underneath the stage.

+ Add some new code to make the spaceship create a new lightning bolt whenever the space key is pressed.

```blocks
when flag clicked
forever
	if <key [space v] pressed?> then
		create clone of [Lightning v]
	end
end
```

+ Whenever a new clone is created, it should start in the same place as the spaceship, and then move up the stage until it touches the edge. Add the following code **to the Lightning sprite**:

```blocks
	when I start as a clone
	go to [Spaceship v]
	show
	repeat until <touching [edge v] ?>
		change y by (10)
	end
	delete this clone
```

Note: We move the new clone to the spaceship while it is still hidden, before then showing it. This just looks nicer.

+ Test your lightning, by pressing the space key.
