## Maak een ruimteschip

Laten we een ruimteschip maken dat de aarde zal verdedigen!

+ Start een nieuw Scratch-project en verwijder de cat-sprite.

[[[generic-scratch-new-project]]]

+ Voeg de ` stars ` achtergrond en de ` spaceship ` sprite aan je project toe.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Gebruik het **kleiner maken ** hulpmiddel om je ` spaceship ` Sprite een beetje kleiner te maken en plaats deze onder aan het scherm.

+ Als de ** linker ** de pijltjestoets wordt ingedrukt, moet het ruimteschip naar links bewegen. Voeg deze code toe om je ruimteschip naar links te verplaatsen wanneer de **linker ** pijltjestoets wordt ingedrukt:

```blocks
    wanneer groene vlag wordt aangeklikt
  herhaal
    als <key [left arrow v] pressed?> dan
      verander x met (-4)
    einde
  einde
```

De x-as gaat van links naar rechts in het speelveld, dus als je de x-positie van het ruimteschip verandert door een getal ervan af te trekken, zal het ruimteschip naar links bewegen. Deze code is het deel dat je ruimteschip naar links verplaatst:

```blocks
verander x met (-4)
```

+ Voeg code toe in het ` herhaal ` {: class = "blockcontrol"} blok om je ruimteschip naar rechts te verplaatsen wanneer de **rechter ** pijltjestoets wordt ingedrukt.

\--- hints \--- \--- hint \--- Als je ` 4 ` van de positie van het ruimteschip aftrekt ging het naar links, hoe kun je in plaats daarvan het ruimteschip naar rechts laten bewegen met ` 4 `? \--- / hint \--- \--- hint \--- Je moet hetzelfde blok gebruiken, maar met een andere waarde:

```blocks
verander x met ( )
```

\--- / hint \--- \--- hint \--- Dit is de code die je nodig hebt om onder de andere code in het ` herhaal ` Blok {: class = "blockcontrol"} blok in te voegen:

```blocks
als <key [right arrow v] pressed?> dan
   verander x met (4)
einde
```

\--- /hint \--- \--- /hints \---

+ Test je project door op de groene vlag te klikken. Kun je je ruimteschip links en rechts laten bewegen met de pijltjestoetsen?