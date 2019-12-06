## Weltraum-Fledermaus

Um Dein Spiel etwas schwieriger zu machen, wirst Du eine Fledermaus erschaffen, die Orangen auf das Raumschiff wirft.

![eine Fledermaus wirft eine Orange auf das Raumschiff](images/bat-oranges.png)

--- task ---

Füge eine `Bat` (englisch für Fledermaus) Figur hinzu und setze ihren Rotationsstil auf **Links/Rechts**.

--- /task ---

--- task ---

Lass die `"Bat"`-Figur `fortlaufend`{:class="block3control"} am oberen Rand der Bühne von Links nach Rechts `gehen`{:class="block3motion"}.

![Fledermaus Figur](images/bat-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
setze Größe auf (50)
wiederhole fortlaufend 
  gehe (10) er Schritt
  pralle vom Rand ab
end
```

Denke daran, Deinen Code zu testen.

--- /task ---

Wenn Du dir die Kostüme der Fledermaus (also der "Bat"-Figur) ansiehst, siehst Du, dass es vier verschiedene gibt:

![screenshot](images/invaders-bat-costume.png)

--- task ---

Verwende den `nächstes Kostüm`{:class=„block3looks“}-Block um die Fledermaus ihre Flügel schlagen zu lassen, wenn sie sich bewegt.

--- hints ---


--- hint ---

Nachdem sich die Fledermaus bewegt hat, sollte sie zum `nächsten Kostüm wechseln`{:class="block3looks"} und dann für eine kurze Zeit `warten`{:class="block3control"}.

--- /hint ---

--- hint ---

Du musst diese Blöcke zu deinem Code hinzufügen:

```blocks3
warte (0.3) Sekunden

wechsle zum nächsten Kostüm
```

--- /hint ---

--- hint --- Dein Code sollte so aussehen:

```blocks3
Wenn die grüne Flagge angeklickt
setze Größe auf (50)
wiederhole fortlaufend 
gehe (10) er Schritt
pralle vom Rand ab
  
+ wechsle zum nächsten Kostüm
+ warte (0.3) Sekunden
end
```

--- /hint ---

--- /hints ---

--- /task ---

Jetzt lass die Fledermaus Orangen werfen!

--- task ---

Füge einr `Orange` Figur aus der Scratch-Bibliothek hinzu.

![Screenshot](images/invaders-orange.png)

--- /task ---

--- task ---

Füge Code zu deiner Fledermaus hinzu, sodass `wenn die Flagge angeklickt wird`{:class="block3events"}, die `Bat`-Figur `fortlaufend`{:class="block3control"} für eine `zufällige`{:class="block3operators"} Zeit, zwischen `5 und 10`{:class="block3operators"} Sekunden, `wartet`{:class="block3control"} und dann von der `Orange`-Figur `einen Klon erstellt`{:class="block3control"}.

![Fledermaus Figur](images/bat-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
wiederhole fortlaufend 
  warte (Zufallszahl von (5) bis (10)) Sekunden
  erzeuge Klon von (Orange v)
end
```

--- /task ---

--- task ---

Füge den Code zur `Orange` hinzu, damit jeder ihrer Klone von der `Bat`-Figur nach unten Richtung Boden der Bühne fällt.

![Orange Figur](images/orange-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt
    verstecke dich

    Wenn ich als Klon entstehe
    gehe zu (Bat v)
    zeige dich
    wiederhole bis <wird (Rand v) berührt?> 
        ändere y um (-4)
    end
    lösche diesen Klon
```

--- /task ---

--- task ---

Füge zu der `Orange`-Figur etwas mehr zum Code hinzu, sodass ein `Orange`-Klon auch verschwindet, wenn er die `Raumschiff`-Figur trifft, um dem Spieler die Möglichkeit zum zurückzusetzen zu geben:

![Orange Figur](images/orange-sprite.png)

```blocks3
    Wenn ich [getroffen v] empfange
    lösche diesen Klon
```

--- /task ---

--- task ---

Ändere den Code deiner `Raumschiff`-Figur so, dass die Figur "getroffen" wird, wenn sie eine `Hippo` Figur oder eine `Orange` Figur berührt:

![raumschiff-Figur](images/rocket-sprite.png)

```blocks3
    warte bis <<wird (Hippo1 v) berührt?> oder <wird (Orange v) berührt?>>
```

--- /task ---

--- task ---

Teste dein Spiel. Was passiert, wenn das Raumschiff von einer fallenden Orange getroffen wird?

--- /task ---