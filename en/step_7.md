## Disappearing hippos

When the spaceship is hit, all the hippos should disappear to give the player a chance to recover.

+ Add a block to your code to broadcast the message "hit" when the spaceship is touching a hippo.

[[[generic-scratch-broadcast-message]]]

--- hints ---
--- hint ---
Create a broadcast 'hit' block by dragging the block from the 'Events' tab and then clicking on the drop down and selecting "new message".
--- /hint ---
--- hint ---
Here is what your block should look like:
```blocks
broadcast [hit v]
```
--- /hint ---
--- hint ---
Here is what your code should look like:

```blocks
when flag clicked
switch costume to [normal v]
wait until <touching [Hippo1 v]>?
switch costume to [hit v]
broadcast [hit v]
```
--- /hint ---
--- /hints ---

All of the hippo sprites will hear this message, so you can now instruct them to disappear when the spaceship is hit.

+ Add this code to the hippo sprite:

```blocks
when I receive [hit v]
delete this clone
```

+ Test out this code by starting a new game and deliberately colliding with a hippo.

![screenshot](images/invaders-hippo-collide.png)

After you get hit, hippos start reappearing but the spaceship has still exploded! Let's make it possible for the spaceship reset itself after being hit.

+ Add a `forever`{:class="blockcontrol"} block around all of your code to make the process repeat, and a `wait`{:class="blockcontrol"} at the end to add a small pause before hippos begin appearing again.

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

--- challenge ---
### Challenge: lives and score

At the moment, the player has infinite lives. Can you add a `lives`{:class="blockdata"}, `score`{:class="blockdata"} or even a `highscore`{:class="blockdata"} to your game?

[[[generic-scratch-high-score]]]

You can also use the 'Catch the Dots' project to help you.
--- /challenge ---
