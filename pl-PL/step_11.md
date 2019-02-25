## Wyzwanie: udoskonal swoją grę

Jakie udoskonalenia możesz wprowadzić w swojej grze?

Oto kilka pomysłów:

+ Dodaj pakiety zdrowia, które możesz zebrać, aby zyskać dodatkowe życia.

![zrzut ekranu](images/invaders-aid.png)

+ Dodaj pływające skały, których twój statek kosmiczny musi unikać.

![zrzut ekranu](images/invaders-rocks.png)

+ Zwiększ liczbę wrogów pokazujących się, gdy twój wynik osiągnie poziom `100`.

```blocks3
    wait until <(score :: variables) = [100]>
```