## Fruit bat

To make the game a bit harder, let's make a fruit bat which throws oranges at the spaceship.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

--- task ---

Add a `Bat` sprite and set its rotation style to **left–right** only.

--- /task ---

--- task ---

Make the `Bat` sprite `move`{:class="blockmotion"} from side to side across the top of the Stage `forever`{:class="blockcontrol"}. 

![screenshot](images/invaders-bat.png)

![bat sprite](images/bat-sprite.png)

```blocks
when flag clicked
forever
    move (10) steps
    if on edge, bounce
end
```

Remember to test out your code.

--- /task ---

If you look at the bat's costumes, you'll see that it already has two different ones:

![screenshot](images/invaders-bat-costume.png)

--- task ---

Use the `next costume`{:class="blocklooks"} block to make the bat flap its wings as it moves.

--- hints ---

--- hint ---

After the bat has moved, it should show the `next costume`{:class="blocklooks"} and then `wait`{:class="blockcontrol"} for a short time.

--- /hint ---

--- hint ---

You will need to add these blocks to you code

```blocks
wait (0.3) secs

next costume
```
--- /hint ---

--- hint ---
You code should look like this:

```blocks
when flag clicked
forever
    move (10) steps
    if on edge, bounce
    next costume
    wait (0.3) secs
end
```
--- /hint ---

--- /hints ---

--- /task ---


Now let's make the bat throw oranges.

--- task ---

Add a new `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

--- /task ---

--- task ---

Add code to your bat so that `When the flag is clicked`{:class="blockevent"}, the `Bat` sprite will `forever`{:class="blockcontrol"} `wait`{:class="blockcontrol"} for a `random`{:class="blockoperators"} time between `5-10`{:class="blockoperators"} seconds and then `create a clone`{:class="blockcontrol"} of the `Orange` sprite

![bat sprite](images/bat-sprite.png)

```blocks
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of [Orange v]
end
```

--- /task ---

--- task ---

Add the code to make each `Orange` sprite clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

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
```

--- /task ---

--- task ---

Add some more code to the `Orange` sprite so that when the `Spaceship` sprite is hit, it also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks
	when I receive [hit v]
	delete this clone
```

--- /task ---

--- task ---

You'll also need to modify the code in your `Spaceship` sprite so that it is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

```blocks
	wait until < <touching [Hippo1 v]?> or <touching [Orange v]?>>
```

--- /task ---

--- task ---

Test your game. What happens if you get hit by a falling orange?

--- /task ---

