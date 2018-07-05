## Game over

Laten we aan het einde van het spel een 'game-over'-bericht toevoegen.

+ Maak, als je dat nog niet gedaan hebt, een nieuwe variabele met de naam ` levens ` {: Class="blockdata"}aan.

Je ruimteschip moet beginnen met drie levens en een leven verliezen wanneer het een nijlpaard of een sinaasappel raakt. Je game zou ook moeten stoppen als je geen levens meer hebt. Als je hulp nodig hebt, kun je het[ Catch the dots ](https://codeclubprojects.org/en-GB/scratch/catch-the-dots/) project gebruiken om je te helpen.

+ Teken een nieuwe sprite genaamd ` Game Over ` met behulp van de ** tekst ** tool.

![screenshot](images/invaders-game-over.png)

+ Verspreid een ` game over ` {: class="blockevents"} bericht vlak voordat het spel eindigt.

```blocks
zend signaal [game over v] en wacht
```

+ Voeg deze code toe aan je ` Game over` sprite, zodat aan het einde van het spel het bericht verschijnt:

```blocks
wanneer op de vlag wordt geklikt
verdwijn

wanneer ik signaal [game over v] ontvang
verschijn
```

Omdat je een ` zend signaal [game over] en wacht ` {: class="blockevents"} hebt gebruikt, zal het wachten op de ` game-over ` sprite voordat het spel wordt beëindigd.

+ Test je spel. Hoeveel punten kun je scoren? Als het te gemakkelijk of te moeilijk is, kun je dan manieren bedenken om je spel te verbeteren?