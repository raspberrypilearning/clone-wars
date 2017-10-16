## Fruit Bat

To make the game a bit harder, let's make a fruit bat which throws oranges at the spaceship.

+ Add a bat sprite to the game and set its rotation style to **left-right** only.

+ Make the bat sprite `move`{:class="blockmotion"} from side to side across the top of the stage `forever`{:class="blockcontrol"}. Remember to test out your code.

![screenshot](images/invaders-bat.png)

--- hints ---
--- hint ---
When the flag is clicked, the bat should forever
- move 10 steps
- if it reaches the edge, bounce
--- /hint ---
--- hint ---
Here is the code you will need:

```blocks
when flag clicked
forever
    move (10) steps
    if on edge, bounce
end
```
--- /hint ---
--- /hints ---

If you look at the bat's costumes, you'll see that it already has 2:

![screenshot](images/invaders-bat-costume.png)

+ Use the `next costume`{:class="blocklooks"} block to make the bat flap its wings as it moves.

--- hints ---
--- hint ---
After the bat has moved, it should show the `next costume`{:class="blocklooks"} and then `wait`{:class="blockcontrol"} for a short time.
--- /hint ---
--- hint ---
Here is the code you will need:

```blocks
next costume
wait (0.3) secs
```
--- /hint ---
--- hint ---
Here is the full code with the new code added:

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

Now let's make the bat throw oranges.

+ Create a new 'Orange' sprite from the Scratch library

![screenshot](images/invaders-orange.png)


+ Add code to your bat, so that when the flag is clicked, it waits for a random time between 5-10 seconds and then creates a clone of the orange sprite.

--- hints ---
--- hint ---
Look at the code you wrote when you created the lightning bolt. This code is very similar, except instead of an orange appearing when you press the space bar, it appears after you `wait`{:class="blockcontrol"} for `5-10`{:class="blockoperators"} seconds.
--- /hint ---
--- hint ---
`When the flag is clicked`{:class="blockcontrol"}, the bat should
`forever`{:class="blockcontrol"}
- `wait`{:class="blockcontrol"} for a `random`{:class="blockoperators"} time between 5-10 seconds
- `create a clone`{:class="blockcontrol"} of the orange sprite
--- /hint ---
--- hint ---
Here is the code you will need:

```blocks
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of [Orange v]
end
```
--- /hint ---
--- /hints ---

+ Click on your orange sprite and add some code to make each orange clone drop, starting from the bat and falling towards the bottom of the stage.

--- hints ---
--- hint ---
This code is almost the same as the code inside the lightning bolt, except that the orange should `go to`{:class="blockmotion"} the bat and it should move **down** the screen instead of up, but still using the `change y by`{:class="blockcontrol"} block.
--- /hint ---
--- hint ---
Here is the code you will need:

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
--- /hint ---
--- /hints ---


+ Add some more code to the orange so that when the spaceship is hit, it also disappears to give the player a chance to reset:

```blocks
	when I receive [hit v]
	delete this clone
```

+ In your spaceship sprite, you'll also need to modify the code so that you are hit if you touch a hippo or an orange:

```blocks
	wait until < <touching [Hippo1 v]?> or <touching [Orange v]?>>
```

+ Test your game. What happens if you get hit by a falling orange?
