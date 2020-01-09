## Stwórz statek kosmiczny

Najpierw utwórz statek kosmiczny, który może bronić Ziemi!

--- task ---

Otwórz projekt startowy Scratch "Wojny klonów".

**Online:** otwórz nowy projekt startowy na stronie [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Jeśli masz konto Scratch, możesz wykonać kopię klikając **Remiks**.

**Offline:** pobierz projekt początkowy z [rpf.io/p/pl-PL/clone-wars-go](http://rpf.io/p/pl-PL/clone-wars-go) i otwórz w programie Scratch Desktop.

Jeśli chcesz pobrać i zainstalować edytor Scratch, znajdziesz go na stronie [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![startowy projekt](images/starter-project.png)

--- task ---

Dodaj ten kod do duszka statku kosmicznego, aby skłonić statek kosmiczny poruszał się w lewo, jeśli strzałka <kbd>w lewo</kbd> jest wciśnięta:

![duszek rakiety](images/rocket-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
zawsze 
  jeżeli <key (strzałka w lewo v) pressed?> to 
    zmień x o (-4)
  end
end
```

Oś x przechodzi od lewej strony Sceny do prawej. Oznacza to, że statek kosmiczny porusza się w lewo po odjęciu od wartości `x` pozycji duszka statku kosmicznego. Ten blok kodu to część, która sprawia, że twój statek kosmiczny porusza się w lewo:

```blocks3
zmień x o (-4)
```

--- /task ---

--- task ---

Dodaj więcej kodu wewnątrz bloku `zawsze`{:class="block3control"}, aby twój statek kosmiczny przesuwał się w prawo, gdy strzałka <kbd>w prawo</kbd> jest wciśnięta.

--- hints ---


--- hint ---

Odjęcie`4` od pozycji `x` sprawiło, że statek kosmiczny porusza się w lewo, więc jak zamiast tego sprawić, żeby przesunął się w prawo o `4`?

--- /hint ---

--- hint ---

Potrzebujesz tego samego bloku kodu, ale z innym numerem:

```blocks3
zmień x o ( )
```

--- /hint ---

--- hint ---

Oto kod, który musisz dodać pod innym kodem wewnątrz bloku `zawsze`{:class="block3control"}:

![duszek rakiety](images/rocket-sprite.png)

```blocks3
jeżeli <key (strzałka w prawo v) pressed?> to 
  zmień x o (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Przetestuj swój projekt, klikając zieloną flagę. Czy możesz nacisnąć klawisze strzałek, aby twój statek kosmiczny poruszał się w lewo i w prawo?

--- /task ---