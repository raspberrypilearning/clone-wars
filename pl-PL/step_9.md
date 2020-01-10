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
kiedy kliknięto zieloną flagę
ustaw rozmiar na (50) %
zawsze 
  przesuń o (10) kroków
  jeżeli na brzegu, odbij się
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
czekaj (0.3) sekund

następny kostium
```

--- /hint ---

--- hint --- Twój kod powinien wyglądać tak:

```blocks3
kiedy kliknięto zieloną flagę
ustaw rozmiar na (50) %
zawsze 
przesuń o (10) kroków
jeżeli na brzegu, odbij się
+ następny kostium
+ czekaj (0.3) sekund
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
kiedy kliknięto zieloną flagę
zawsze 
  czekaj (losuj liczbę od (5) do (10)) sekund
  utwórz klona z (Pomarańcza v)
end
```

--- /task ---

--- task ---

Dodaj kod do `Pomarańczy` aby każdy z jego klonów spadał, zaczynając od duszka `Nietoperza` i spada w dół do dolnej części sceny.

![duszek pomarańczy](images/orange-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
  ukryj

  gdy zaczynam jako klon
  idź do (Nietoperz v)
  pokaż
  powtarzaj aż <dotyka (krawędź v)?
    zmień y o (-4)
  end
  usuń tego klona
```

--- /task ---

--- task ---

Dodaj jeszcze kod do duszka `Pomarańczy` aby kiedy klon `Pomarańczy` trafi duszka `statku kosmicznego`, klon również znikał, aby dać szanse graczowi na zresetowanie:

![duszek pomarańczy](images/orange-sprite.png)

```blocks3
    kiedy otrzymam [trafienie v]
usuń tego klona
```

--- /task ---

--- task ---

Zmodyfikuj kod swojego duszka `statku kosmicznego`, aby zmieniał kostium na "trafiony", gdy dotknie duszka `Hipcia` lub duszka `Pomarańczy`:

![duszek rakiety](images/rocket-sprite.png)

```blocks3
    czekaj aż <<dotyka (Hipcia v) ?> lub <dotyka (Pomarańczy v) ?>>
```

--- /task ---

--- task ---

Przetestuj swoją grę. Co się stanie, jeśli statek kosmiczny zostanie uderzony spadającą pomarańczą?

--- /task ---