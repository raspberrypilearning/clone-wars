## Kosmiczne hipopotamy

Teraz dodasz mnóstwo latających hipopotamów, które będą próbować zniszczyć Twój statek kosmiczny.

--- task ---

Utwórz nowego duszka z obrazem "Hippo1" w bibliotece Scratch. Użyj narzędzia **pomniejsz** aby zmienić rozmiar duszka `Hipcio` do rozmiarów duszka `Statku kosmicznego`.

![zrzut ekranu](images/invaders-hippo.png)

--- /task ---

--- task ---

Ustaw styl obrotów duszka `Hipcio` na tylko **lewo-prawo**.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

Dodaj kod, aby ukryć duszka `Hipcio` kiedy gra się zaczyna.

![duszek hipopotama](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

Dodaj trochę kodu do sceny, aby tworzyć nowego klona duszka `Hipcio` co kilka sekund.

--- hints ---


--- hint ---

Kiedy `kliknięto zieloną flagę`{:class="block3events"}, `wielokrotnie`{:class="block3control"} `czekaj`{:class="block3control"} `pomiędzy 2 a 4 sekundy`{:class="block3operators"} i później `utwórz klona duszka Hipcio`{:class="block3control"}.

--- /hint ---

--- hint ---

Oto bloki, których potrzebujesz:

```blocks3
forever
end

create clone of (Hipcio v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

Tak powinien wyglądać Twój kod:

![duszek sceny](images/stage-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (2) to (4)) secs
	create clone of (Hipcio v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

Każdy nowy hipopotam powinien pojawić się w przypadkowym położeniu `x` i każdy klon powinien mieć losową prędkość.

--- task ---

Utwórz nową zmienną o nazwie `prędkość`{:class="block3variables"}, która jest tylko dla duszka `Hipcio`.

[[[generic-scratch3-add-variable]]]

Jeśli zrobisz to poprawnie, zmienna będzie mieć obok siebie nazwę duszka, tak jak poniżej:

![zrzut ekranu](images/invaders-var-test.png)

--- /task ---

--- task ---

Kiedy każdy klon `Hipcia` zaczyna, losuje prędkość i położenie zanim pojawi się na ekranie.

```blocks3
when I start as a clone
set [prędkość v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

Przetestuj swój kod. Czy nowy Hipcio pojawia się co kilka sekund?

--- /task ---

W tej chwili hipopotamy się nie ruszają.

--- task ---

Każdy hipopotam powinien poruszać się losowo, dopóki nie zostanie trafiony błyskawicą. Aby tak się stało, dołącz poniższy kod pod blokami, które są już w kodzie skryptu duszka `Hipcia`:

```blocks3
repeat until <touching (Błyskawica v) ?> 
	move (speed :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```	

--- /task ---

--- task ---

Sprawdź swój kod ponownie. Powinieneś zobaczyć nowego klona hipopotama co kilka sekund, a każdy klon powinien poruszać się z inną prędkością.

--- no-print ---

![zrzut ekranu](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

Teraz przetestuj działo laserowe statku kosmicznego. Jeśli błyskawica trafi w hipopotama, to czy hipopotam zniknie?

--- /task ---