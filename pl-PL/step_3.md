## Stwórz statek kosmiczny

Stwórzmy statek kosmiczny, który będzie bronił Ziemi!

+ Rozpocznij nowy projekt Scratch i usuń duszek kota.

[[[generic-scratch-new-project]]]

+ Dodaj tło z `gwiazdek` i duszka `statku kosmicznego` do twojego projektu.
    
    ![zrzut ekranu](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Użyj narzędzia **zmniejsz** żeby trochę pomniejszyć twój ` statek kosmiczny ` i ustaw go w dolnej części ekranu.

+ Kiedy klawisz strzałki ** w lewo ** jest wciśnięty, statek kosmiczny powinien przesunąć się w lewo. Dodaj ten kod, aby twój statek kosmiczny przesuwał się w lewo, gdy strzałka ** w lewo ** jest wciśnięta:

```blocks
    kiedy kliknięto zieloną flagę
     zawsze 
       jeżeli <klawisz [strzałka w lewo v] naciśnięty?> to 
         zmień x o (-4)
     end
    end
```

W scenie, oś x przebiega od lewej do prawej, więc jeśli zmniejszysz pozycję x statku kosmicznego, odejmując od niej, przesunie się dalej w lewo. Ten kod sprawia, że ​​twój statek kosmiczny przesuwa się w lewo:

```blocks
zmień x o (-4)
```

+ Dodaj więcej kodu wewnątrz bloku ` zawsze`, aby twój statek kosmiczny przesuwał się w prawo, gdy strzałka** w prawo ** jest wciśnięta.

\--- hints \--- \--- hint \--- Jeśli odjęcie` 4 `od pozycji x statku kosmicznego spowodowało, że przesunął się w lewo, w jaki sposób można go przesunąć o ` 4 ` w prawo? \--- /hint \--- \--- hint \--- Będziesz musiał użyć tego samego bloku, ale z inną liczbą:

```blocks
zmień x o ()
```

\--- /hint \--- \--- hint \--- Oto kod, który będziesz musiał dodać wewnątrz poprzednio stworzonego bloku `zawsze` pod kodem który już tam jest:

```blocks
jeżeli <klawisz [strzałka w prawo v] naciśnięty?> to 
  zmień x o (4)
end
```

\--- /hint \--- \--- /hints \---

+ Przetestuj swój projekt, klikając zieloną flagę. Czy potrafisz sprawić, by twój statek kosmiczny poruszał się w lewo i prawo za pomocą klawiszy strzałek?