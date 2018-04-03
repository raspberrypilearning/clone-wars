## Blitze

Lass uns dem Raumschiff die Fähigkeit verleihen, Blitze abzufeuern!

+ Füge das 'Lightning' (Blitze) Sprite von der Scratch Bibliothek hinzu.  Wenn das Spiel beginnt, sollten die Blitze erstmal versteckt bleiben bis das Raumschiff seine Laser-Kanonen feuert. Das Sprite muss viel kleiner und kopfüber sein. Füge den folgenden Code zum 'Lightning' (Blitze) Sprite hinzu.

	```blocks
		Wenn die grüne Flagge angeklickt
		verstecke dich
		setze Größe auf (25)%
		setze Richtung auf (-90 v)	
	```


+ Füge den folgenden Code **to the Spaceship** (zum Raumschiff hinzu), um einen neuen Blitz zu erzeugen, wannimmer die Leertaste gedrückt wird.


	```blocks
		Wenn die grüne Flagge angeklickt
		wiederhole fortlaufend
   			falls <Taste [Leertaste v] gedrückt?> dann
      			erzeuge Klon von [Lightning v]
   		Ende
	Ende
	```

+ Wannimmer ein neuer Klon erstellt wird, sollte er am gleichen Ort wie das Raumschiff beginnen und dann das Stadium hoch gehen bis er die Kante berührt. Füge den folgenden Code **to the Lightning sprite** (zum Blitze-Sprite hinzu):

	```blocks
		Wenn ich als Klon entstehe
		gehe zu [Spaceship v]
		zeige dich
		wiederhole bis <wird [Rand v] berührt?>
   			ändere y um (10)
		Ende
		lösche diesen Klon
	```

Hinweis: Wir bewegen den neuen Klon zum Raumschiff hin, während es immer noch versteckt ist, ehe wir es dann zeigen. Das sieht schöner aus.

+ Teste deine Blitze, indem du die Leertaste drückst.

--- challenge ---

## Aufgabe: Die Blitze ausbessern 
Was passiert, wenn du die Leertaste gedrückt hältst? Kannst du einen `wait`{:class="blockcontrol"} Block einschieben, um dies zu beheben?

--- /challenge ---
