## Błyskawice

Teraz, dodasz statkowi możliwość strzelania błyskawicami!

--- task ---

Dodaj duszka `Lightning` z biblioteki Scratch i nazwijmy go "Błyskawica".

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Gdy gra się rozpocznie, duszek `Błyskawica` powinien być ukryty, dopóki statek kosmiczny nie wystrzeli z dział laserowych.

Dodaj ten kod do duszka `Błyskawicy`:

![duszek błyskawicy](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

W tej chwili błyskawica jest naprawdę duża w porównaniu do statku kosmicznego!

--- task ---

Poniżej kodu jaki ma już duszek `Błyskawica` dodaj kilka bloków, aby zmniejszyć duszka i obrócić go do góry nogami.

![duszek błyskawicy](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Teraz wygląda na to, że je wystrzeliwuje ze statku kosmicznego spiczastym końcem do przodu.

--- /task ---

--- task ---

Dodaj trochę nowego kodu do duszka `Statku kosmicznego` aby stworzyć nowego klona błyskawicy, jeżeli wciśnięty jest przycisk <kbd>spacja</kbd>.

--- hints ---


--- hint ---

`Kiedy kliknięto zieloną flagę`{:class="block3events"}, sprawdzaj `zawsze`{:class="block3control"} `jeżeli`{:class="block3control"} `klawisz spacji jest wciśnięty`{:class="block3sensing"}, w takim przypadku `stwórz klona Błyskawicy`{:class="block3control"}.

--- /hint ---

--- hint ---

Oto bloki, których potrzebujesz:

```blocks3
if <> then
end

forever
end

create clone of (Błyskawica v)

<key (spacja v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

Tak powinien wyglądać Twój kod:

![duszek rakiety](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (spacja v) then
		create clone of (Błyskawica v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Za każdym razem, gdy gra tworzy klona duszka `Błyskawica`, klon powinien pojawić się i przesuwać w górę, aż osiągnie górną granicę sceny. Następnie klon powinien zniknąć.

Dodaj ten kod do duszka `Błyskawica` tak, aby jego klony poruszały się w górę, aż dotkną krawędzi sceny, a następnie zostaną usunięte.

![duszek błyskawicy](images/lightning-sprite.png)

```blocks3
	when I start as a clone
	go to (Statek kosmiczny v)
    show
	repeat until <touching (krawędź v) ?> 
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

Naciśnij klawisz <kbd>spacji</kbd> aby sprawdzić czy twoje błyskawice poprawnie się poruszają.

--- /task ---