## Maak een ruimteschip

Maak eerst een ruimteschip dat de aarde kan verdedigen!

\--- task \---

Open het 'Clone wars' Scratch starter project.

**Online**: open het starter project op [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_ blank"}.

Als je een Scratch-account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline:** download het starter project op [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), en open het vervolgens met behulp van de Scratch offline editor.

Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![starter project](images/starter-project.png)

\--- task \---

Voeg deze code toe aan de spaceship sprite om het ruimteschip te verplaatsen als de <kbd>links</kbd> pijl wordt ingedrukt:

![ruimteschip sprite](images/rocket-sprite.png)

```blocks3
    wanneer groene vlag wordt aangeklikt
  herhaal
    als <key (left arrow v) pressed?> dan
      verander x met (-4)
    einde
  einde
```

De x-as gaat van de linkerkant van het speelveld naar de rechterkant. Dit betekent dat het ruimteschip naar links gaat wanneer je de waarde van de `x` positie aftrekt. Dit code blok is dus het onderdeel dat je ruimteschip naar links verplaatst:

```blocks3
verander x met (-4)
```

\--- /task \---

\--- task \---

Voeg wat meer code toe aan het `herhaal`{:class="block3control"} blok om je ruimteschip naar rechts te verplaatsen als de <kbd>rechts</kbd> pijl toets wordt ingedrukt.

\--- hints \---

\--- hint \---

Het aftrekken van `4` van de ruimteschip `x` positie verplaatst deze naar links, dus hoe kun je in plaats daarvan het ruimteschip `4` naar rechts verplaatsen?

\--- /hint \---

\--- hint \---

Je hebt hetzelfde code blok nodig, maar met een ander nummer:

```blocks3
verander x met ( )
```

\--- /hint \---

\--- hint \---

Hier is de code die je onder de andere code binnen het `herhaal`{:class="block3control"} blok moet toevoegen:

![ruimteschip sprite](images/rocket-sprite.png)

```blocks3
als <key (right arrow v) pressed?> dan
   verander x met (4)
einde
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test je project door op de groene vlag te klikken. Kun je op de pijltjes toetsen drukken om je ruimteschip naar links en rechts te laten bewegen?

\--- /task \---