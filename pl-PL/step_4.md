## Błyskawice

Dodajmy statkowi kosmicznemu moc strzelania błyskawicami!

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

![Hint](images/hint-lightning.png) \--- /hint \--- \--- hint \--- Here is the code you will need:

```blocks
when flag clicked
forever
    if <key [space v] pressed?> then
        create clone of [Lightning v]
    end
end
```

\--- /hint \--- \--- /hints \---

+ Switch back to the `Lightning` sprite.

+ Whenever a lightning bolt is created, it should appear and then move upwards until it reaches the top of the screen. Then it should disappear.

\--- hints \--- \--- hint \---

When a new `Lightning` sprite clone appears:

+ Display it
+ Repeatedly move it up by `10` until it is touching the edge of the screen
+ Then delete the clone \--- /hint \--- \--- hint \--- Here are the blocks you will need:

![Move lightning](images/move-hint-lightning.png) \--- /hint \--- \--- hint \--- Here is the code you will need to add to the `Lightning` sprite:

```blocks
    when I start as a clone
    show
    repeat until <touching [edge v] ?>
        change y by (10)
    end
    delete this clone
```

\--- /hint \--- \--- /hints \---

+ Test your `Lightning` sprite by clicking the green flag and then pressing the **space** bar. When you press **space**, does lightning appear and move up the screen? What problem can you spot?

## \--- collapse \---

## title: Answer

Oops — at the moment the lightning always fires from the same place, regardless of where the spaceship is!

Add this block just before the `show`{:class="blocklooks"} block to make the clone of the `Lightning` sprite move to the `Spaceship` sprite's position before it appears. This will make it look like the lightning bolt is firing out of the spaceship.

```blocks
go to [Spaceship v]
```

\--- /collapse \---

+ Press the **space** key to test whether your lightning bolt now fires correctly.

\--- challenge \---

### Challenge: fixing the lightning

What happens if you hold down the **space** key? Can you use a `wait`{:class="blockcontrol"} block to fix this?

\--- /challenge \---