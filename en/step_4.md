## Lightning bolts

Let's give the spaceship the ability to fire lightning bolts!

+ Add the 'Lightning' sprite from the Scratch library.  

+ When the game is started, the lightning should be hidden until the spaceship fires its laser cannons, so add this code to the lightning sprite:

```blocks
when green flag clicked
hide
```

At the moment you have a pretty gigantic lightning bolt for the spaceship to fire!

+ Attach some more code underneath the code you just added to make the lightning smaller and turn it upside down so that it fires pointy end first out of the spaceship.

```blocks
set size to (25) %
point in direction (-90 v)
```

+ Switch to the **spaceship** sprite by clicking on it in the 'Sprites' panel underneath the stage.

+ Add some new code to make the spaceship create a new lightning bolt whenever the space key is pressed.

```blocks
when flag clicked
forever
	if <key [space v] pressed?> then
		create clone of [Lightning v]
	end
end
```

+ Switch back to the **lightning** sprite.

+ Whenever a lightning bolt is created it should appear and then move upwards until it reaches the top of the screen, when it should disappear. Add this code to the lightning sprite:

```blocks
	when I start as a clone
    show
	repeat until <touching [edge v] ?>
		change y by (10)
	end
	delete this clone
```

+ Test your lightning by clicking the green flag and then pressing the space bar. Does lightning appear when you press space and move up the screen? What problem can you spot?

--- collapse ---
---
title: Answer
---
Oops - at the moment the lightning always fires from the same place, regardless of where the spaceship is!

Add this block just before the `show`{:class="blocklooks"} block to make the lightning bolt move to the spaceship's position before it appears, so that it looks like the lightning bolt is firing out of the spaceship.

```blocks
go to [Spaceship v]
```

--- /collapse ---

+ Test your lightning bolt now fires correctly by pressing the space key.

--- challenge ---
### Challenge: Fixing the lightning
What happens if you keep the space key held down? Can you use a `wait`{:class="blockcontrol"} block to fix this?

--- /challenge ---
