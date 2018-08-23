## Błyskawice

Dodajmy statkowi kosmicznemu zdolność strzelania błyskawicami!

+ Dodaj duszek `Błyskawicy` z biblioteki Scratch.

+ Na początku gry, dopóki statek kosmiczny nie wystrzeli ze swoich dział laserowych, `Błyskawica` powinna być ukryta. Dodaj ten kod do duszka `Błyskawicy`:

```blocks
kiedy kliknięto zieloną flagę
ukryj
```

W tej chwili masz dość gigantyczną błyskawicę do wystrzelenia ze statku!

+ Dołącz ten kod poniżej bloków, które właśnie dodałeś, aby pomniejszyć `Błyskawicę` i odwrócić ją do góry nogami. Wtedy będzie wyglądać jak wystrzeliwuje spiczasty koniec ze statku kosmicznego.

```blocks
ustaw rozmiar na (25) %
ustaw kierunek na (-90 v)
```

+ Przejdź do duszka ` statku koszmicznego ` klikając na niego w panelu Duszki poniżej Sceny.

+ Dodaj nowy kod, aby sprawić że ` statek kosmiczny ` stworzy nową błyskawicę za każdym razem, gdy klawisz ** spacji ** zostanie wciśnięty.

\--- hints \--- \--- hint \--- Oto trochę pseudokodu dla ciebie:

When the green flag is clicked Keep checking forever If the **space** key was pressed, create a clone of the `Lightning` sprite \--- /hint \--- \--- hint \--- Here are the blocks you will need:

![Wskazówka](images/hint-lightning.png) \--- /hint \--- \--- hint \--- To jest kod, którego będziesz potrzebować:

```blocks
when flag clicked
forever
    if <key [space v] pressed?> then
        create clone of [Lightning v]
    end
end
```

\--- /hint \--- \--- /hints \---

+ Wróć do duszka `Błyskawica`.

+ Ilekroć tworzona jest błyskawica, powinna pojawić się, a następnie przesuwać się w górę, aż osiągnie górną część ekranu. Wtedy powinna zniknąć.

\--- hint \--- \--- /hints \---

Kiedy pojawia się nowy klon duszka `Błyskawica`:

+ Wyświetl to
+ Repeatedly move it up by `10` until it is touching the edge of the screen
+ Then delete the clone \--- /hint \--- \--- hint \--- Here are the blocks you will need:

![Move lightning](images/move-hint-lightning.png) \--- /hint \--- \--- hint \--- To jest kod, którego potrzebujesz, żeby dodać duszka `Błyskawica`:

```blocks
    kiedy zaczynam jako klon
    pokaż
    powtórz, aż <touching [edge v] ?>
        zmień y przez (10)
    koniec
    usuń ten klon
```

\--- /hint \--- \--- /hints \---

+ Sprawdź swojego duszka `Błyskawica` klikając zieloną flagę, a następnie wciskając klawisz **spacja**. When you press **space**, does lightning appear and move up the screen? Jaki problem możesz zauważyć?

## \--- collapse \---

## title: Answer

Ups - w tej chwili błyskawica zawsze strzela z tego samego miejsca, niezależnie od tego, gdzie znajduje się statek kosmiczny!

Add this block just before the `show`{:class="blocklooks"} block to make the clone of the `Lightning` sprite move to the `Spaceship` sprite's position before it appears. To spowoduje odpalenie błyskawicy że statku kosmicznego.

```blocks
idź do [Spaceship v]
```

\--- /collapse \---

+ Press the **space** key to test whether your lightning bolt now fires correctly.

\--- challenge \---

### Wyzwanie: naprawienie błyskawicy

What happens if you hold down the **space** key? Can you use a `wait`{:class="blockcontrol"} block to fix this?

\--- /challenge \---