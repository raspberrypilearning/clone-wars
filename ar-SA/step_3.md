## إنشاء سفينة فضاء

لننشئ سفينة فضاء تدافع عن كوكب الأرض!

+ Start a new Scratch project, and delete the cat sprite.

[[[generic-scratch-new-project]]]

+ Add the `stars` backdrop and the `Spaceship` sprite to your project.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Use the **shrink** tool to make your `Spaceship` sprite a bit smaller, and position it near the bottom of the screen.

+ When the **left** arrow key is pressed, the spaceship should move to the left. Add this code to make your spaceship move left when the **left** arrow is pressed:

```blocks
    when flag clicked
    forever
        if <key [left arrow v] pressed?> then
            change x by (-4)
        end
    end
```

The x-axis goes from left to right on the Stage, so if you make the the spaceship's x-position smaller by substracting from it, it will move further to the left. This code is the part which makes your spaceship move left:

```blocks
change x by (-4)
```

+ Add some more code inside the `forever`{:class="blockcontrol"} block to make your spaceship move to the right when the **right** arrow key is pressed.

\--- hints \--- \--- hint \--- If subtracting `4` from the spaceship's position made it move left, how could you make it move right by `4` instead? \--- /hint \--- \--- hint \--- You will need to use the same block, but with a different number:

```blocks
change x by ( )
```

\--- /hint \--- \--- hint \--- Here is the code you will need to add below the other code inside your `forever`{:class="blockcontrol"} block:

```blocks
if <key [right arrow v] pressed?> then
    change x by (4)
end
```

\--- /hint \--- \--- /hints \---

+ Test your project by clicking the green flag. Can you make your spaceship move left and right with the arrow keys?