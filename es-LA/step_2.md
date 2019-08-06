## Make a spaceship

First make a spaceship that can defend the Earth!

\--- función \---

Open the 'Clone wars' Scratch starter project.

** Online **: abra un nuevo proyecto Scratch en línea en [ rpf.io/clone-wars-on ](http://rpf.io/clone-wars-on)"}.

Si tienes una cuenta Scratch puedes hacer una copia haciendo clic en **Remix**.

**Offline:** download the starter project from [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), and then open it using the offline editor.

Si necesitas descargar e instalar el editor offline de Scratch, puedes encontrarlo en [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- / tarea \---

![starter project](images/starter-project.png)

\--- tarea \---

Add this code to the spaceship sprite to make the spaceship move left if the <kbd>left</kbd> arrow is pressed:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

The x-axis goes from the left side of the Stage to the right side. This means that the spaceship moves to the left when you subtract from the value of the spaceship sprite's `x` position. So this code block is the part that makes your spaceship move left:

```blocks3
change x by (-4)
```

\--- /task \---

\--- tarea \---

Add some more code inside the `forever`{:class="block3control"} block to make your spaceship move to the right if the <kbd>right</kbd> arrow key is pressed.

\--- hints \---

\--- hint \---

Subtracting `4` from the spaceship's `x` position made it move left, so how could you make the spaceship move right by `4` instead?

\--- /hint \---

\--- hint \---

You need the same code block, but with a different number:

```blocks3
change x by ( )
```

\--- /hint \---

\--- hint \---

Here is the code you need to add below the other code inside the `forever`{:class="block3control"} block:

![rocket sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- /hint \---

\--- / consejos \---

\--- / tarea \---

\--- tarea \---

Test your project by clicking the green flag. Can you press the arrow keys to make your spaceship move left and right?

\--- / tarea \---