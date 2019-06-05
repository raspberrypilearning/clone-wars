## Maak een ruimteschip

Maak eerst een ruimteschip dat de aarde kan verdedigen!

\--- task \---

Open het 'Kloon wars' Scratch starter project.

**Online**: open het starter project op [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_ blank"}.

Als je een Scratch-account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline:** download het starter project op [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), en open het vervolgens met behulp van de Scratch offline editor.

Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![starter project](images/starter-project.png)

\--- task \---

Voeg deze code toe aan de spaceship sprite om het ruimteschip te verplaatsen als de <kbd>links</kbd> pijl wordt ingedrukt:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wanneer groene vlag wordt aangeklikt
  herhaal
    als <key (left arrow v) pressed?> dan
      verander x met (-4)
    einde
  einde
```

De x-as gaat van de linkerkant van het speelveld naar de rechterkant. Dit betekent dat het ruimteschip naar links gaat wanneer je de waarde van de `x` positie aftrekt. Dit code blok is dus het onderdeel dat je spaceship naar links verplaatst:

```blocks3
verander x met (-4)
```

\--- /task \---

\--- task \---

Voeg wat meer code toe aan het `herhaal`{:class="block3control"} blok om je spaceship naar rechts te verplaatsen als de <kbd>rechts</kbd> pijl toets wordt ingedrukt.

\--- hints \---

\--- hint \---

Subtracting `4` from the spaceship's `x` position made it move left, so how could you make the spaceship move right by `4` instead?

\--- /hint \---

\--- hint \---

You need the same code block, but with a different number:

```blocks3
verander x met ( )
```

\--- /hint \---

\--- hint \---

Here is the code you need to add below the other code inside the `forever`{:class="block3control"} block:

![rocket sprite](images/rocket-sprite.png)

```blocks3
als <key (right arrow v) pressed?> dan
   verander x met (4)
einde
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test your project by clicking the green flag. Can you press the arrow keys to make your spaceship move left and right?

\--- /task \---