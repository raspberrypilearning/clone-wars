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
kiedy kliknięto zieloną flagę
ukryj
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
zawsze
end

utwórz klona z (Hipcio v)

(losuj liczbę od (2) do (4))

kiedy kliknięto zieloną flagę

czekaj () sekund
```

--- /hint ---

--- hint ---

Tak powinien wyglądać Twój kod:

![duszek sceny](images/stage-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
zawsze 
  czekaj (losuj liczbę od (2) do (4)) sekund
  utwórz klona z (Hipcio v)
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
gdy zaczynam jako klon
ustaw [prędkość v] na (losuj liczbę od (2) do (4))
Idź do x: (losuj liczbę od (-220) do (220)) y: (150)
pokaż
```

--- /task ---

--- task ---

Przetestuj swój kod. Czy nowy Hipcio pojawia się co kilka sekund?

--- /task ---

W tej chwili hipopotamy się nie ruszają.

--- task ---

Każdy hipopotam powinien poruszać się losowo, dopóki nie zostanie trafiony błyskawicą. Aby tak się stało, dołącz poniższy kod pod blokami, które są już w kodzie skryptu duszka `Hipcia`:

```blocks3
powtarzaj aż <dotyka (Błyskawica v) ?> 
  przesuń o (speed :: variables) kroków
  obróć w prawo o (losuj liczbę od (-10) do (10)) stopni
  jeżeli na brzegu, odbij się
end
usuń tego klona
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