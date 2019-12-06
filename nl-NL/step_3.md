## Bliksemschichten

Nu ga je het ruimteschip de mogelijkheid geven om bliksemschichten af te vuren!

\--- task \---

Voeg de `Lightning ` sprite toe uit de Scratch-bibliotheek.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Wanneer het spel begint, moeten de `Lightning` sprites verborgen worden totdat het ruimteschip zijn laser kanon afschiet.

Voeg deze code toe aan de `Lightning` sprite:

![lightning sprite](images/lightning-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt 
 verdwijn
```

\--- /task \---

Op dit moment is de bliksemschicht echt groot in vergelijking met het ruimteschip!

\--- task \---

Onder de code die `Lightning` sprite al heeft, voeg je enkele blokken toe om de sprite kleiner te maken en om deze om te draaien.

![lightning sprite](images/lightning-sprite.png)

```blocks3
maak grootte (25) %
richt naar (-90) graden
```

Nu lijkt het als of de punt het eerst uit het ruimteschip wordt geschoten.

\--- /task \---

\--- task \---

Voeg nieuwe code toe om de `ruimteschip` sprite een nieuwe bliksemschicht te laten maken als op de <kbd>spatie</kbd> toets wordt gedrukt.

\--- hints \---

\--- hint \---

`Wanneer op de groene vlag wordt geklikt`{:class="block3events"}, controleer `voor altijd`{:class="block3control"} `als`{:class="block3control"} de `spatie toets wordt ingedrukt`{:class="block3sensing"}, en in dat geval `maak een kloon van de Lightning`{:class="block3control"} sprite.

\--- /hint \---

\--- hint \---

Dit zijn de blokken die je nodig hebt:

```blocks3
als <> dan
end

herhaal
end

maak een kloon van (Lightning v)

<wanneer (spatiebalk) is ingedrukt?>

wanneer groene vlag wordt aangeklikt
```

\--- /hint \---

\--- hint \---

Dit is hoe je code eruit zou moeten zien:

![ruimteschip sprite](images/rocket-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
herhaal 
  als < wanneer (spatiebalk v) ingedrukt?> dan 
    maak een kloon van (Lightning v)
  einde
einde
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Wanneer het spel een `Lightning` sprite kloont, moet de kloon verschijnen en vervolgens naar boven gaan totdat het de bovenkant van het speelveld bereikt. Dan moet de kloon verdwijnen.

Voeg deze code toe aan de `Lightning` sprite zodat klonen ervan naar boven bewegen totdat ze de rand van het speelveld raken, en vervolgens verwijderd worden.

![lightning sprite](images/lightning-sprite.png)

```blocks3
    wanneer ik als kloon start
ga naar (Ruimteschip v)
verschijn
herhaal tot <raak ik (rand v)> 
  verander y met (10)
einde
verwijder deze kloon
```

\--- /task \---

\--- task \---

Druk op de <kbd>spatietoets </kbd> om te testen of je bliksemschicht nu correct wordt afgevuurd.

\--- /task \---