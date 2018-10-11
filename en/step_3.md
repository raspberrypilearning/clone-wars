## Lightning bolts

Let's give the spaceship the ability to fire lightning bolts!

--- task ---

Add the `Lightning` sprite from the Scratch library.  

[[[generic-scratch-sprite-from-library]]]

--- /task ---

--- task ---

When the game is started, the `Lightning` sprite should be hidden until the spaceship fires its laser cannons, so add this code to the `Lightning` sprite:

![lightning sprite](images/lightning-sprite.png)

```blocks
when green flag clicked
hide
```

At the moment you have a pretty gigantic lightning bolt for the spaceship to fire!

--- /task ---

--- task ---

Attach some code below the blocks you just added to make the `Lightning` sprite smaller and to turn it upside down. Then it will look like it fires pointy end–first out of the spaceship.

![lightning sprite](images/lightning-sprite.png)

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
if <> then
end

forever
end

create clone of [Lightning v]

<key [space v] pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

Here is the code you will need:

![rocket sprite](images/rocket-sprite.png)

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

--- task ---

Whenever a lightning bolt is created, it should appear and then move upwards until it reaches the top of the screen. Then it should disappear.

So add this code to the `Lightning` sprite so it moves up the screen until it is touching the edge.

```blocks
	when I start as a clone
	go to [Spaceship v]
    show
	repeat until <touching [edge v] ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

Press the **space** key to test whether your lightning bolt fires correctly.

--- /task ---

