## Flying space-hippos

Let's add lots of flying hippos that will try to destroy your spaceship.

+ Create a new sprite with the `Hippo1` image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![screenshot](images/invaders-hippo.png)

+ Set the `Hippo` sprite's rotation style to be left-right only.

[[[generic-scratch-sprite-rotation-style]]]

+ Add some code to hide the `Hippo` sprite when the game starts.

\--- hints \--- \--- hint \--- The code for this is exactly the same as the code you used to hide the `Lightning` sprite when the game starts. \--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
when green flag clicked
hide
```

\--- /hint \--- \--- /hints \---

+ Switch to the Stage by clicking on it in the bottom panel.

+ Add some code to the Stage to create a new hippo every few seconds.

\--- hints \--- \--- hint \--- When the green flag is clicked: Repeatedly...

+ Wait between 2 and 4 seconds
+ Create a clone of the hippo sprite

\--- /hint \--- \--- hint \--- Here are the blocks you will need: ![Clone hippo hint](images/clone-hippo-hint.png)

\--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of [Hippo1 v]
end
```

\--- /hint \--- \--- /hints \---

+ Switch back to the `Hippo` sprite.

Each new hippo should appear at a random x-position, and each should have a random speed.

+ Create a new variable called `speed`{:class="blockdata"} that is for the `Hippo` sprite only.

[[[generic-scratch-add-variable]]]

You'll know you've done this correctly when you can see that the variable has the name of the sprite next to it, like this:

![screenshot](images/invaders-var-test.png)

+ When each hippo clone starts, pick a random speed and starting place before showing it on the screen.

```blocks
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

+ Test your code by clicking the green flag. Does a new hippo appear every few seconds? At the moment your hippos won't move.

+ The hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks you just added:

```blocks
repeat until <touching [lightning v] ?>
    move (speed) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

+ Test out your hippo code. You should see a new hippo clone appear every few seconds, each moving at its own speed.
    
    ![screenshot](images/hippo-clones.gif)

+ Test your laser cannon. If you hit a hippo, does it vanish?