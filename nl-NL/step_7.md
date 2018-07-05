## Verdwijnende nijlpaarden

Wanneer het ruimteschip wordt geraakt, moeten alle nijlpaarden verdwijnen om de speler een kans te geven om te herstellen.

+ Voeg een blok toe aan je code voor een` zend signaal ` "geraakt" bericht wanneer het ruimteschip een nijlpaard raakt.

[[[generic-scratch-broadcast-message]]]

\--- hints \--- \--- hint \--- Maak een ` -zend signaal 'geraakt'` blok door het blok uit de ** gebeurtenissen ** tab te slepen en klik vervolgens op het pijltje ernaast en selecteer ** nieuw bericht... **. \--- / hint \--- \--- hint \--- Hier is hoe je blok eruit zou moeten zien:

```blocks
zend signaal [geraakt v]
```

\--- / hint \--- \--- hint \--- Hier is hoe je blok eruit zou moeten zien:

```blocks
wanneer groene vlag wordt aangeklikt
verander uiterlijk naar [normaal v] 
wacht tot <touching [Hippo1 v]>? 
verander uiterlijk naar [geraakt v]
```

\--- /hint \--- \--- /hints \---

Alle ` Hippo ` sprite-klonen zullen dit bericht horen, zodat je ze nu kunt instrueren om te verdwijnen wanneer het ruimteschip wordt geraakt.

+ Voeg deze code toe aan de ` Hippo ` sprite:

```blocks
wanneer ik signaal [geraakt v] ontvang, 
verwijder deze kloon
```

+ Test deze code door een nieuw spel te starten en opzettelijk in botsing te komen met een nijlpaard.

![screenshot](images/invaders-hippo-collide.png)

Nadat je bent geraakt, verschijnen de nijlpaarden weer, maar het ruimteschip is nog steeds geëxplodeerd! Laten we het mogelijk maken dat het ruimteschip zichzelf reset na geraakt te zijn.

+ Voeg een `herhaal ` {: class="blockcontrol"} blok toe rondom al je code om het proces te laten herhalen, en een ` wacht ` {: class="blockcontrol"} blok aan het einde toe om een ​​kleine pauze in te voegen voordat nijlpaarden weer verschijnen.

```blocks
wanneer groene vlag wordt aangeklikt
verander uiterlijk naar [normaal v] 
wacht tot <touching [Hippo1 v]>? 
verander uiterlijk naar [geraakt v]
zend signaal [geraakt]
wacht (1) sec
```

\--- challenge \---

### Challenge: levens en score

Op dit moment heeft de speler een oneindig aantal levens. Kun je ` levens ` {: class="blockdata"}, een ` score ` {: class="blockdata"}, of zelfs een ` highscore ` {: class="blockdata"} toevoegen aan je spel?

[[[generic-scratch-high-score]]] \--- /challenge \---