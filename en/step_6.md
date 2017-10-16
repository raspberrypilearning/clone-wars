## Exploding spaceship

When a hippo touches your spaceship it should explode!

+ Select the spaceship sprite and rename the costume to 'normal'.

+ Draw another costume of the spaceship exploding and call it 'hit'.

![screenshot](images/invaders-spaceship-costumes.png)

Or, if you don't want to draw the explosion you could choose the 'Sun' costume from the Scratch library, and use the 'Color a shape' tool to change its colour and remove the face.

![screenshot](images/invaders-sun.png)

+ Add some code to your spaceship so that it starts off displaying the spaceship costume, but when it touches a flying hippo it switches to the 'hit' costume:

```blocks
when flag clicked
switch costume to [normal v]
wait until <touching [Hippo1 v]>?
switch costume to [hit v]
```

+ Test your code by playing the game and colliding with a hippo. Does the spaceship change to the 'hit' costume?
