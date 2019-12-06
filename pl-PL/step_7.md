## Hipopotamy, które znikają

Kiedy statek kosmiczny wybuchnie, wszystkie hipopotamy powinny zniknąć, aby dać graczowi szansę na wyleczenie.

\--- task \---

Dodaj kod do duszka statku kosmicznego, aby `nadać`{:class="block3events"} komunikat „trafienie”, gdy `Statek kosmiczny dotknie Hipcia`{:class="block3sensing"}.

![duszek rakiety](images/rocket-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
zmień kostium na (normalny v)
czekaj aż <touching (Hippo1 v)>?
zmień kostium na (trafiony v)
nadaj komunikat (trafienie v)
```

\--- /task \---

\--- task \---

Wszystkie klony duszka `Hipcio` otrzymają komunikat "trafienie" i możesz polecić im zniknąć, kiedy statek kosmiczny jest trafiony, poprzez dodanie tego kodu do duszka `Hipcia`:

![duszek hipopotama](images/hippo-sprite.png)

```blocks3
kiedy otrzymam [trafienie v]
usuń tego klona
```

\--- /task \---

\--- task \---

Aby sprawdzić, czy nowy kod działa, kliknij zieloną flagę i spraw, aby statek kosmiczny zderzył się z hipopotamem.

![zrzut ekranu](images/invaders-hippo-collide.png)

\--- /task \---

Po eksplozji statku kosmicznego pojawiają się nowe klony duszka `Hipcia`, ale statek kosmiczny wciąż eksploduje! Po trafieniu statek kosmiczny musi się zresetować.

\--- task \---

Dodaj blok `czekaj`{:class="block3control"} na końcu kodu duszka `Statek kosmiczny` aby utworzyć małą pauzę, zanim hipopotamy zaczną się ponownie pojawiać. Następnie dodaj blok `zawsze`{:class="block3control"} wokół całego kodu, aby kod był uruchamiany wielokrotnie.

![duszek rakiety](images/rocket-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
zawsze 
 zmień kostium na (normalny v)
 czekaj aż <touching (Hippo1 v)>?
 zmień kostium na (trafiony v)
 nadaj (trafienie v)
 
+ czekaj (1) s
end
```

\--- /task \---