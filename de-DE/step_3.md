## Baue ein Raumschiff

Bauen wir ein Raumschiff, das die Erde verteidigen wird!

+ Starte ein neues Scratch-Projekt und lösche das Katzen-Sprite.

[[[generic-scratch-new-project]]]

+ Füge den ` Sterne Hintergrund ` hinzu und das ` Raumschiff `-Sprite zu deinem Projekt hinzu.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Verwende das **Schrumpf-** Werkzeug, um dein ` Raumschiff` Sprite ein bisschen kleiner zu machen, und positioniere es am unteren Rand des Bildschirms.

+ Wenn die **linke** Pfeiltaste gedrückt ist, soll das Raumschiff sich anch links bewegen. Füge den folgenden Code hinzu um das Raumschiff nach links zu bewegen, wenn die **linke** Pfeiltaste gedrückt ist:

```blocks
    wenn grüne Fahne angeklickt
    wiederhole fortlaufend
        falls <key [left arrow v] pressed?> dann
            ändere x um (-4)
        end
    end
```

Die x-Achse geht von links nach rechts auf der Bühne, so dasssich das Schiff, wenn man die X-Position des Raumschiffs durch Subtraktion verkleinert wird, weiter nach links bewegt. Dieser Code ist der Teil, der das Raumschiff nach links bewegt:

```blocks
ändere x um (-4)
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