## Lightning bolts

Let's give the spaceship the ability to fire lightning bolts!

--- task ---

Add the `Lightning` sprite from the Scratch library.  

[[[generic-scratch-sprite-from-library]]]

--- /task ---

--- task ---

When the game is started, the `Lightning` sprite should be hidden until the spaceship fires its laser cannons, so add this code to the `Lightning` sprite:

```blocks
when green flag clicked
hide
```

At the moment you have a pretty gigantic lightning bolt for the spaceship to fire!

--- /task ---

--- task ---

Attach some code below the blocks you just added to make the `Lightning` sprite smaller and to turn it upside down. Then it will look like it fires pointy end–first out of the spaceship.

```blocks
set size to (25) %
point in direction (-90 v)
```

--- /task ---

--- task ---

Add some new code to make the `Spaceship` sprite create a new lightning bolt whenever the **space** key is pressed.

--- hints ---

--- hint ---

`When the green flag is clicked`{:class="blockevents"} keep checking `forever`{:class="blockcontrol"} `if`{:class="blockcontrol"} the `**space** key was pressed`{:class="blocksensing"}, `create a clone of itself`{:class="blockcontrol"}.	

--- /hint ---

--- hint ---

Here are the blocks you will need:

```blocks
forever
end

<key [space v] pressed?>

if <> then
end

create clone of [Lightning v]

when flag clicked
```

![Hint](images/hint-lightning.png)

--- /hint ---

--- hint ---

Here is the code you will need:

```blocks
when flag clicked
forever
	if <key [space v] pressed?> then
		create clone of [Lightning v]
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---


+ 
+ 

+ 

+
+ Switch back to the `Lightning` sprite.

+ Whenever a lightning bolt is created, it should appear and then move upwards until it reaches the top of the screen. Then it should disappear.

--- hints ---
--- hint ---

When a new `Lightning` sprite clone appears:
- Display it
- Repeatedly move it up by `10` until it is touching the edge of the screen
- Then delete the clone
--- /hint ---
--- hint ---
Here are the blocks you will need:

![Move lightning](images/move-hint-lightning.png)
--- /hint ---
--- hint ---
Here is the code you will need to add to the `Lightning` sprite:

```blocks
	when I start as a clone
    show
	repeat until <touching [edge v] ?>
		change y by (10)
	end
	delete this clone
```
--- /hint ---
--- /hints ---



+ Test your `Lightning` sprite by clicking the green flag and then pressing the **space** bar. When you press **space**, does lightning appear and move up the screen? What problem can you spot?

--- collapse ---
---
title: Answer
---
Oops — at the moment the lightning always fires from the same place, regardless of where the spaceship is!

Add this block just before the `show`{:class="blocklooks"} block to make the clone of the `Lightning` sprite move to the `Spaceship` sprite's position before it appears. This will make it look like the lightning bolt is firing out of the spaceship.

```blocks
go to [Spaceship v]
```

--- /collapse ---

+ Press the **space** key to test whether your lightning bolt now fires correctly.

--- challenge ---
### Challenge: fixing the lightning
What happens if you hold down the **space** key? Can you use a `wait`{:class="blockcontrol"} block to fix this?

--- /challenge ---
