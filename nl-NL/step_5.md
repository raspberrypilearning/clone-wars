## Vliegende ruimte-nijlpaarden

Laten we heel veel vliegende nijlpaarden toevoegen die proberen je ruimteschip te vernietigen.

+ Maak een nieuwe sprite met de `Hippo1` afbeelding uit de Scratch-bibliotheek. Gebruik het **Kleiner maken ** hulpmiddel om de `Hippo` Sprite net zo klein te maken als de `Spaceship` sprite.

![screenshot](images/invaders-hippo.png)

+ Stel de `Hippo` sprite in de draaistijl zodat deze alleen links-rechts draait.

[[[generic-scratch-sprite-rotation-style]]]

+ Voeg code toe om als het spel begint de `Hippo` Sprite te verbergen.

--- hints --- --- hint --- De code hiervoor is precies hetzelfde als de code die je hebt gebruikt om de `Lightning` Sprite aan het begin van het spel te verbergen. --- / hint --- --- hint --- Dit is de code die je nodig hebt:

```blocks
wanneer groene vlag wordt aangeklikt 
 verdwijn
```

--- /hint --- --- /hints ---

+ Ga naar de stars achtergrond door te klikken op de achtergrond links onder.

+ Voeg wat code toe aan de achtergrond om elke paar seconden een nieuw nijlpaard te maken.

--- hints --- --- hint --- Wanneer op de groene vlag wordt geklikt: herhaal...

+ Wacht tussen 2 en 4 seconden
+ Maak een kloon van de hippo-sprite

--- / hint --- --- hint --- Hier is de code die je nodig hebt: ![Clone hippo hint](images/clone-hippo-hint.png)

--- / hint --- --- hint --- Hier is de code die je nodig hebt:

```blocks
wanneer de groene vlag wordt aangeklikt 
herhaal
   wacht (willekeurig getal tussen (2) tot (4)) sec.
   maak kloon van [Hippo1 v] 
einde
```

--- /hint --- --- /hints ---

+ Schakel terug naar de `Hippo` sprite.

Elke nieuw nijlpaard moet op een willekeurige x-positie verschijnen en moet een willekeurige snelheid hebben.

+ Maak een nieuwe variabele met de naam `snelheid` {:class="blockdata"} deze is alleen voor de `Hippo` sprite.

[[[generic-scratch-add-variable]]]

Je hebt dit goed gedaan als je de variabele naam van de sprite ernaast ziet staan, zoals hier:

![screenshot](images/invaders-var-test.png)

+ Bij elke nijlpaardenkloon, kies je een willekeurige snelheid en startplaats voordat je deze op het scherm laat zien.

```blocks
wanneer ik als kloon start
maak [snelheid v] (willekeurig getal tussen (2) tot (4)) 
ga naar x: (kies willekeurig (-220) tot (220)) y: (150) 
verschijn
```

+ Test je code door op de groene vlag te klikken. Verschijnt er om de paar seconden een nieuwe nijlpaard? Op dit moment bewegen je nijlpaarden niet.

+ De nijlpaard moet willekeurig rondvliegen totdat hij wordt geraakt door een bliksemflits. Om dit mogelijk te maken, plak je deze code onder de blokken die je zojuist hebt toegevoegd:

```blocks
herhaal tot <touching [lightning v] ?> 
   neem (snelheid) stappen
   draai naar rechts (willekeurig getal (-10) tot (10)) graden
   keer om aan de rand
einde
deze kloon verwijderen
```

+ Test je hippocode. Je zou elke paar seconden een nieuwe nijlpaardkloon moeten zien verschijnen, elk met zijn eigen snelheid.
    
    ![screenshot](images/hippo-clones.gif)

+ Test je laserkanon. Als je een nijlpaard raakt, verdwijnt die dan?