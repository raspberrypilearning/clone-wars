## Fruit vleermuis

Om het spel een beetje moeilijker te maken, laten we een fruitvleermuis maken die sinaasappels naar het ruimteschip gooit.

+ Voeg een `Bat (vleermuis)` sprite toe en zet de draaistijl naar **links-rechts**.

+ Zorg ervoor dat de `vleermuis` sprite zich van links naar rechts aan de bovenkant van het speelveld `verplaatst` {: klasse = "blockmotion"} door middel van een `herhaal` {: class = "blockcontrol"} blok. Vergeet je code niet te testen.

![screenshot](images/invaders-bat.png)

\--- hints \--- \--- hint \--- Wanneer op de groene vlag wordt geklikt, zou de ` -vleermuis ` Sprite steeds

+ verplaats 10 stappen
+ als het de rand bereikt, omkeren \--- / hint \--- \--- hint \--- Dit is de code die je nodig hebt:

```blocks
wanneer de vlag wordt aangeklikt
herhaal
   neem (10) stappen 
   keer om aan de rand
einde
```

\--- /hint \--- \--- /hints \---

Als je naar de uiterlijken van de vleermuis kijkt, zie je dat het al twee verschillende uiterlijken heeft:

![screenshot](images/invaders-bat-costume.png)

+ Gebruik het ` volgende uiterlijk` {: class = "blocklooks"} blok om de vleermuis met zijn vleugels te laten klapperen als hij beweegt.

\--- hints \--- \--- hint \--- Nadat de vleermuis is verplaatst, wordt het ` volgend uiterlijk ` {: class = "blocklooks"} weergegeven en ` wacht ` {: class = "blockcontrol"} vervolgens een korte tijd. \--- / hint \--- \--- hint \--- Hier is de code die je nodig hebt:

```blocks
volgend uiterlijk
wacht (0,3) sec
```

\--- / hint \--- \--- hint \--- Hier is de complete code met de nieuwe code toegevoegd:

```blocks
wanneer de groene vlag wordt aangeklikt
herhaal
   neem (10) stappen
   keer om aan de rand
   volgend uiterlijk
   wacht (0,3) sec
einde
```

\--- /hint \--- \--- /hints \---

Nu laten we de vleermuis sinaasappels gooien.

+ Voeg een nieuwe ` Orange (sinaasappel) ` sprite toe uit de Scratch-bibliotheek.

![screenshot](images/invaders-orange.png)

+ Voeg code aan je vleermuis toe, zodat wanneer op de groene vlag wordt geklikt, het een willekeurige tijd tussen 5 en 10 seconden wacht en dan een clone van de `oranje`-sprite maakt.

\--- / hint \--- \--- hint \--- Hier is de code die je moet toevoegen aan de ` Lightning ` sprite. De code die je nu nodig hebt, lijkt veel op die van de lightning sprite, in plaats van dat er bliksemschicht verschijnt als je op de ** spatiebalk ** drukt, zou er na een ` wacht ` {: class="blockcontrol"} tussen de ` 5-10 ` {: class="blockoperators"} seconden een sinaasappel moeten verschijnen. \--- / hint \--- \--- hint \--- ` Wanneer de groene vlag wordt aangeklikt ` {: class="blockcontrol"}, zou de ` vleermuis ` sprite via een ` herhaal ` {: class ="blockcontrol"} blok steeds na een wachttijd tussen 5 - 10 sec een sinaasappel clone moeten gooien

+ ` wacht ` {: class="blockcontrol"} een `willekeurige getal tussen `{: class="blockoperators"} ` 5 en 10 ` {: class="blockoperators"} sec
+ ` maak kloon van` {: class="blockcontrol"} ` Orange ` sprite \--- / hint \--- \--- hint \--- Hier is de code die je nodig hebt:

```blocks
wanneer groene vlag wordt aangeklikt
herhaal
   wacht (willekeurig getal tussen (5) en (10)) sec.
   maak kloon van [Orange v]
einde
```

\--- /hint \--- \--- /hints \---

+ Klik op je ` Orange ` sprite en voeg een code toe om elke ` Orange ` kloon sprite te laten verschijnen, beginnend bij de ` Bat ` sprite en naar de onderkant van het speelveld valt.

\--- hints \--- \--- hint \--- De code die je zoekt is bijna hetzelfde als de code in de ` Lightning ` sprite, behalve dat de ` Orange ` sprite moet ` gaan naar ` {: class="blockmotion"} de ` Bats ` sprite's positie, en het zou het ` verander y met ` {: class="blockcontrol"} blok moeten gebruiken om naar beneden in plaats van naar boven te gaan. \--- / hint \--- \--- hint \--- Hier is de code die je nodig hebt:

```blocks
    wanneer de groene vlag wordt aangeklikt
   verdwijn

   wanneer ik als kloon start
   ga naar [Bat1 v] 
   verschijn
   herhaal tot <raak ik [rand v]
      verander y met (-4)
   eind
   verwijder deze kloon

```

\--- /hint \--- \--- /hints \---

+ Voeg wat meer code toe aan de ` Orange ` sprite zodat wanneer de ` ruimteschip ` sprite is geraakt, de sinaasappel sprite ook verdwijnt om de speler een kans te geven om te herstellen:

```blocks
    wanneer ik signaal [geraakt] ontvang, 
   verwijder deze kloon
```

+ Je moet ook de code van je ` Spaceship` sprite wijzigen zodat het wordt geraakt wanneer het een ` Hippo ` sprite of een ` sinaasappel ` sprite aanraakt:

```blocks
    wacht tot < <touching [Hippo1 v]?> of <touching [Orange v]?>>
```

+ Test je spel. Wat gebeurt er als je wordt geraakt door een vallende sinaasappel?