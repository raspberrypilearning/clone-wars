## Baue ein Raumschiff

Baue zuerst ein Raumschiff, das die Erde verteidigen kann!

\--- task \---

Öffne das "Klonkriege" Scratch Starter Projekt.

**Online:** Öffne das Basisprojekt auf [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch Klick auf **Remix** eine Kopie anlegen.

**Offline:** Lade das Basisprojekt von [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go){:target="_blank"} herunter und öffne es dann mit dem Scratch Offline-Editor.

Wenn du den Scratch-Offline-Editor herunterladen und installieren möchtest, findest du diesen unter [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![Startprojekt](images/starter-project.png)

\--- task \---

Füge diesen Code zur "Raumschiff"-Figur hinzu, damit sich das Raumschiff nach links bewegt, wenn der Pfeil <kbd>links</kbd> gedrückt wird:

![Raumschiff-Figur](images/rocket-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt
wiederhole fortlaufend 
  falls <Taste (Pfeil nach links v) gedrückt?> , dann 
    ändere x um (-4)
  end
end
```

Die x-Achse verläuft von der linken Seite der Bühne zur rechten Seite. Das bedeutet, dass sich das Raumschiff nach links bewegt, wenn Du vom Wert der `x` Position der Raumschiff-Figur etwas abziehst. Dieser Codeblock ist also der Teil, der dein Raumschiff nach links bewegt:

```blocks3
ändere x um (-4)
```

\--- /task \---

\--- task \---

Füge nun weiteren Code innerhalb des `Wiederhole fortlaufend`{:class="block3control"} Blocks hinzu, um das Raumschiff nach rechts zu bewegen, wenn die <kbd>rechte</kbd> Pfeiltaste gedrückt wird.

\--- hints \---

\--- hint \---

Wenn Du `4` von der `x` Position des Raumschiffs abziehst, wurde es nach links verschoben. Wie kannst Du das Raumschiff stattdessen um `4` nach rechts verschieben?

\--- /hint \---

\--- hint \---

Du benötigst denselben Code-Block, aber mit einer anderen Zahl:

```blocks3
ändere x um ( )
```

\--- /hint \---

\--- hint \---

Hier ist der Code, den Du unterhalb des anderen Codes im Block `Wiederhole fortlaufend`{:class="block3control"} hinzufügen musst:

![Raumschiff-Figur](images/rocket-sprite.png)

```blocks3
falls <Taste (Pfeil nach rechts v) gedrückt?> , dann 
  ändere x um (4)
end
```

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Teste dein Projekt, indem du auf die grüne Flagge klickst. Kannst du die Pfeiltasten drücken, um dein Raumschiff nach links und rechts zu bewegen?

\--- /task \---