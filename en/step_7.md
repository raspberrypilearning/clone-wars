## Hippos that disappear

When the spaceship explodes, all the hippos should disappear so that players of the game can recover.

--- task ---

Add code to the spaceship sprite to make it `broadcast`{:class="blockevents"} the message "hit" when the `spaceship touches a hippo`{:class="blocksensing"}.

![rocket sprite](images/rocket-sprite.png)

```blocks
when flag clicked
switch costume to [normal v]
wait until <touching [Hippo1 v]>?
switch costume to [hit v]
+ broadcast [hit v]
```

--- /task ---

--- task ---

All of the `Hippo` sprite clones will receive the "hit" message, and you can instruct them to disappear when the spaceship is hit by adding this code to the `Hippo` sprite:

![hippo sprite](images/hippo-sprite.png)

```blocks
when I receive [hit v]
delete this clone
```

--- /task ---

--- task ---

To check whether the new code works, click the green flag and make the spaceship collide with a hippo.

![screenshot](images/invaders-hippo-collide.png)

--- /task ---

After the spaceship explodes, new `Hippo` clones appear, but the spaceship is still exploded! The spaceship needs to reset itself after being hit.

--- task ---

Add a `wait`{:class="blockcontrol"} block at the end of the `Spaceship` sprite's code to create a small pause before hippos begin appearing again. Then add a `forever`{:class="blockcontrol"} block around all of your code to make the code run repeatedly.

![rocket sprite](images/rocket-sprite.png)

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

--- /task ---

