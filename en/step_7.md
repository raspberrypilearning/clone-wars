## Disappearing hippos

When the spaceship is hit, all the hippos should disappear to give the player a chance to recover.

--- task ---

Add the code to spaceship so it `broadcasts`{:class="blockevents"} the message "hit" when the `spaceship touches a hippo`{:class="blocksensing"}.

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

All of the `Hippo` sprite clones will hear the "hit" message, so you can instruct them to disappear when the spaceship is hit by adding this code:

![hippo sprite](images/hippo-sprite.png)

```blocks
when I receive [hit v]
delete this clone
```

--- /task ---

--- task ---

Test out this code by starting a new game and deliberately colliding with a hippo.

![screenshot](images/invaders-hippo-collide.png)

--- /task ---

After you get hit, hippos start reappearing but the spaceship has still exploded! Let's make it possible for the spaceship to reset itself after being hit.

--- task ---

Add a `forever`{:class="blockcontrol"} block around all of your code to make the process repeat, and a `wait`{:class="blockcontrol"} block at the end to add a small pause before hippos begin appearing again.

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

