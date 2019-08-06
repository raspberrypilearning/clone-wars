## Verdwijnende nijlpaarden

Wanneer het ruimteschip ontploft, moeten alle nijlpaarden verdwijnen zodat de speler het spel kan hervatten.

\--- task \---

Voeg code aan de ruimteschip sprite toe om het `zend signaal`{:class="block3events"} bericht "raak" te maken wanneer het `ruimteschip een nijlpaard raakt`{:class="block3sensing"}.

![ruimteschip sprite](images/rocket-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
verander uiterlijk naar (normaal v)
wacht tot <touching (Hippo1 v)>
verander uiterlijk naar (raak v)
zend signaal (raak v)
```

\--- /task \---

\--- task \---

Alle `nijlpaard` klonen ontvangen het "raak" bericht, en je kunt hen opdragen om te verdwijnen als het schip wordt getroffen door deze code toe te voegen aan `nijlpaard` sprite:

![nijlpaard sprite](images/hippo-sprite.png)

```blocks3
wanneer ik signaal [raak v] ontvang, 
verwijder deze kloon
```

\--- /task \---

\--- task \---

Om te controleren of de nieuwe code werkt, klik op de groene vlag en laat het ruimteschip een nijlpaard raken.

![screenshot](images/invaders-hippo-collide.png)

\--- /task \---

Nadat het ruimteschip ontploft is, verschijnen nieuwe `nijlpaard` klonen, maar het ruimteschip is nog steeds ontploft! Het schip moet zichzelf herstellen na geraakt te zijn.

\--- task \---

Voeg een `wacht`{:class="block3control"} blok toe aan het einde van de `ruimteschip` sprite code om een kleine pauze te maken voordat de nijlpaarden weer beginnen te verschijnen. Voeg vervolgens een `herhaal`{:class="block3control"} blok rond al je code toe om de code herhaaldelijk uit te laten voeren.

![ruimteschip sprite](images/rocket-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
herhaal 
 verander uiterlijk naar (normaal v)
 wacht tot <touching (Hippo1 v)>
 verander uiterlijk naar (raak v)
 zend signaal (raak v)
 wacht (1) sec.
end
```

\--- /task \---