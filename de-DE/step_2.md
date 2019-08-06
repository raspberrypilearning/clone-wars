## Baue ein Raumschiff

Baue zuerst ein Raumschiff, das die Erde verteidigen kann!

\--- task \---

Öffnen Sie das Scratch-Startprojekt "Clone Wars".

**Online:** Öffnen Sie das Startprojekt unter [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){: target = "_ blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch Klick auf **Remix** eine Kopie anlegen.

**Offline:** Laden Sie das Startprojekt von [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go)herunter und öffnen Sie es mit dem Offline-Editor.

Wenn du den Scratch-Offline-Editor herunterladen und installieren möchtest, findest du diesen unter [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![Startprojekt](images/starter-project.png)

\--- task \---

Fügen Sie diesen Code zum Raumschiffsprite hinzu, damit sich das Raumschiff nach links bewegt, wenn der Pfeil <kbd>links</kbd> gedrückt wird:

![Raketen-Sprite](images/rocket-sprite.png)

```blocks3
    wenn grüne Fahne angeklickt
    wiederhole fortlaufend
        falls <key (left arrow v) pressed?> dann
            ändere x um (-4)
        end
    end
```

Die x-Achse verläuft von der linken Seite der Bühne zur rechten Seite. Dies bedeutet, dass sich das Raumschiff nach links bewegt, wenn Sie vom Wert der `x` Position des Raumschiff-Sprites subtrahieren. Dieser Codeblock ist also der Teil, der Ihr Raumschiff nach links bewegt:

```blocks3
ändere x um (-4)
```

\--- /task \---

\--- task \---

Fügen Sie weiteren Code in den Block `für immer`{: class = "block3control"} ein, damit sich Ihr Raumschiff nach rechts bewegt, wenn die Pfeiltaste <kbd>rechts und</kbd> gedrückt wird.

\--- hints \---

\--- hint \---

Wenn Sie `4` von der `x` Position des Raumschiffs subtrahieren, wurde es nach links verschoben. Wie können Sie das Raumschiff stattdessen um `4` nach rechts verschieben?

\--- /hint \---

\--- hint \---

Sie benötigen denselben Codeblock, jedoch mit einer anderen Nummer:

```blocks3
ändere x um ( )
```

\--- /hint \---

\--- hint \---

Hier ist der Code, den Sie unterhalb des anderen Codes im Block `forever`{: class = "block3control"} hinzufügen müssen:

![Raketen-Sprite](images/rocket-sprite.png)

```blocks3
falls <key (right arrow v) pressed?> dann
  ändere x um (4)
end
```

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Testen Sie Ihr Projekt, indem Sie auf die grüne Flagge klicken. Kannst du die Pfeiltasten drücken, um dein Raumschiff nach links und rechts zu bewegen?

\--- /task \---