## Aufgabe: Verbessere dein Spiel

Wenn das Raumschiff explodiert, sollten alle Flusspferde verschwinden, damit sich die Spieler des Spiels erholen können.

\--- task \---

Fügen Sie dem Raumschiffsprite Code hinzu, damit `Nachricht`{: class = "block3events"} "hit" sendet, wenn das Raumschiff `ein Flusspferd berührt`{: class = "block3sensing"}.

![Raketen-Sprite](images/rocket-sprite.png)

```blocks3
wenn Flagge geklickt
Kostüm wechseln zu (normal v)
warten bis <touching (Hippo1 v)>?
Kostüm wechseln zu (hit v)

+ Sendung (hit v)
```

\--- /task \---

\--- task \---

Alle `Hippo` Sprite-Klone erhalten die Nachricht "hit", und Sie können sie anweisen, zu verschwinden, wenn das Raumschiff getroffen wird, indem Sie dem `Hippo` Sprite diesen Code hinzufügen:

![Hippo Sprite](images/hippo-sprite.png)

```blocks3
Wenn ich [hit v]
erhalte, lösche diesen Klon
```

\--- /task \---

\--- task \---

Um zu überprüfen, ob der neue Code funktioniert, klicken Sie auf die grüne Flagge und lassen Sie das Raumschiff mit einem Flusspferd kollidieren.

![screenshot](images/invaders-hippo-collide.png)

\--- /task \---

Nachdem das Raumschiff explodiert ist, erscheinen neue `Hippo` Klone, aber das Raumschiff ist immer noch explodiert! Das Raumschiff muss sich nach einem Treffer selbst zurücksetzen.

\--- task \---

Fügen Sie am Ende des `Spaceship` Sprite-Codes einen `wait`{: class = "block3control"} -Block hinzu, um eine kleine Pause zu erstellen, bevor wieder Flusspferde angezeigt werden. Fügen Sie dann einen Block `für immer`{: class = "block3control"} um Ihren gesamten Code hinzu, damit der Code wiederholt ausgeführt wird.

![Raketen-Sprite](images/rocket-sprite.png)

```blocks3
als die Flagge für immer auf
geklickt hat
Kostüm wechseln zu (normal v)
Warten bis <touching (Hippo1 v)>?
Kostüm wechseln zu (v)
Senden (v)

+ Warten (1) Sekunden
Ende
```

\--- /task \---