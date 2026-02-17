## Kosmiczny nietoperz

Aby twoja gra była nieco trudniejsza, stworzysz nietoperza, który zrzuca pomarańcze na statek kosmiczny.

![nietoperz zrzucający pomarańczę na statek kosmiczny](images/bat-oranges.png)

--- task ---

Dodaj duszka `Bat`, zmień jego nazwę na Nietoperz i ustaw styl obrotu na **lewo-prawo**.

--- /task ---

--- task ---

Zrób aby duszek `Nietoperz` wykonywał ruch `przesuń się`{:class="block3motion"} z lewej strony na prawą, na górze Sceny `zawsze`{:class="block3control"}.

![duszek nietoperza](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Pamiętaj, aby przetestować swój kod.

--- /task ---

Jeśli spojrzysz na kostiumy nietoperza, to zobaczysz, że ma cztery różne:

![zrzut ekranu](images/invaders-bat-costume.png)

--- task ---

Użyj bloku `następny kostium`{:class="block3looks"} aby sprawić, żeby nietoperz machał skrzydłami w czasie ruchu.

--- hints ---


--- hint ---

Po przesunięciu, nietoperz powinien wyświetlić `następny kostium`{:class="block3looks"}, a następnie `czekać`{:class="block3control"} przez krótki czas.

--- /hint ---

--- hint ---

Musisz dodać te bloki do swojego kodu:

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

Twój kod powinien wyglądać tak:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce
+ next costume
+ wait (0.3) seconds
end
```

--- /hint ---

--- /hints ---

--- /task ---

Teraz spraw, aby nietoperz zrzucał pomarańcze!

--- task ---

Dodaj nowego duszka `Orange` z biblioteki Scratch. Tym razem zmieńmy nazwę tego duszka na Pomarańcza.

![zrzut ekranu](images/invaders-orange.png)

--- /task ---

--- task ---

Dodaj kod do swojego nietoperza, taki że `kiedy flaga jest kliknięta`{:class="block3events"}, duszek `Nietoperza` `zawsze`{:class="block3control"} `czeka`{:class="block3control"} przez `losowy`{:class="block3operators"} okres czasu, z przedziału między `5 a 10`{:class="block3operators"} sekund, a następnie `tworzy klona`{:class="block3control"} duszka `Pomarańczy`.

![duszek nietoperza](images/bat-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of (Pomarańcza v)
end
```

--- /task ---

--- task ---

Dodaj kod do `Pomarańczy` aby każdy z jego klonów spadał, zaczynając od duszka `Nietoperza` i spada w dół do dolnej części sceny.

![duszek pomarańczy](images/orange-sprite.png)

```blocks3
	when flag clicked
	hide

	when I start as a clone
	go to (Nietoperz v)
	show
	repeat until <touching (krawędź v)?
		change y by (-4)
	end
	delete this clone
```

--- /task ---

--- task ---

Dodaj jeszcze kod do duszka `Pomarańczy` aby kiedy klon `Pomarańczy` trafi duszka `statku kosmicznego`, klon również znikał, aby dać szanse graczowi na zresetowanie:

![duszek pomarańczy](images/orange-sprite.png)

```blocks3
	when I receive [trafienie v]
	delete this clone
```

--- /task ---

--- task ---

Zmodyfikuj kod swojego duszka `statku kosmicznego`, aby zmieniał kostium na "trafiony", gdy dotknie duszka `Hipcia` lub duszka `Pomarańczy`:

![duszek rakiety](images/rocket-sprite.png)

```blocks3
	wait until < <touching (Hipcia v)?> or <touching (Pomarańczy v)?>>
```

--- /task ---

--- task ---

Przetestuj swoją grę. Co się stanie, jeśli statek kosmiczny zostanie uderzony spadającą pomarańczą?

--- /task ---