## Baue ein Raumschiff

Bauen wir ein Raumschiff, das die Erde verteidigen wird!

+ Starte ein neues Scratch-Projekt und lösche das Katzen-Sprite.

[[[generic-scratch-new-project]]]

+ Füge den ` Sterne Hintergrund ` hinzu und das ` Raumschiff `-Sprite zu deinem Projekt hinzu.
    
    ![Bildschirmfoto](images/invaders-sprites.png)

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

+ Füge nun weiteren Code innerhalb des `Wiederhole fortlaufend`{:class='blockcontrol'} Blocks hinzu, um das Raumschiff nach rechts zu bewegen, wenn die **rechte** Pfeiltaste gedrückt wird.

\--- Hinweise \--- \--- Hinweis \--- Wenn sich das Raumschiff nach links bewegt wenn man von seiner Position `4` abzieht, wie schafft man es dann, dass es sich stattdessen um `4` nach rechts bewegt? \--- / Hinweis \--- \--- Hinweis \--- Sie müssen den gleichen Block verwenden, aber mit einer anderen Ziffer:

```blocks
ändere x um ( )
```

\--- / Hinweis \--- \--- Hinweis \--- Hier ist der Code, der unter dem anderen Code innerhalb des `Wiederhole fortlaufent`{: class = "blockcontrol"} Blocks hinzugefügt werden muss:

```blocks
falls <key [right arrow v] pressed?> dann
  ändere x um (4)
end
```

\--- / Hinweis \--- \--- / Hinweise \---

+ Testen Sie Ihr Projekt, indem Sie auf die grüne Flagge klicken. Kannst du dein Raumschiff mit den Pfeiltasten nach links und rechts bewegen?