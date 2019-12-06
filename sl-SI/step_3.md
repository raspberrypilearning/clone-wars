## Strele

Sedaj boš raketi dodal-a sposobnost, da strelja strele!

\--- task \---

Dodaj figuro `Lightning` iz Scratch knjižnice in jo preimenuj v 'strela'.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Ko se igra začne mora biti figura `strela` skrita, dokler raketa ne sproži svojega laserskega topa.

Figuri `strela` dodaj to kodo:

![figura strele](images/lightning-sprite.png)

```blocks3
ko kliknemo na zastavo
skrij
```

\--- /task \---

Trenutno je strela v primerjavi z raketo zelo velika!

\--- task \---

Pod kodo, ki jo figura `strela` že vsebuje, dodaj še nekaj blokov, ki bodo figuro zmanjšale in jo obrnile na glavo.

![figura strele](images/lightning-sprite.png)

```blocks3
nastavi velikost na (25) %
obrni se v smer (-90)
```

Zdaj je videti, kot da strela iz rakete izstopi s konico naprej.

\--- /task \---

\--- task \---

Dodaj še nekaj kode figuri `rakete`, ki ustvari nov dvojnik strele, če je pritisnjena tipka <kbd>presledek</kbd>.

\--- hints \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- /hint \---

\--- hint \---

To so bloki, ki jih potrebuješ:

```blocks3
če <> potem
konec

ponavljaj
konec

ustvari dvojnika (strela v)

<key (space v) pressed?>

ko kliknemo na zastavo
```

\--- /hint \---

\--- hint \---

Tvoja koda naj bi izgledala tako:

![figura rakete](images/rocket-sprite.png)

```blocks3
ko kliknemo na zastavo
ponavljaj
  če &ltje pritisnjena tipka (presledek v)&gt potem
    ustvari dvojnika (strela v)
   konec
konec
```

\--- /hint \---

\--- /namigi \---

\--- /task \---

\--- task \---

Kadarkoli igra ustvari dvojnika figure `strela`, bi se dvojnik moral pojaviti in potem premikati navzgor, dokler ne doseže vrha odra. Nato bi moral dvojnik izginiti.

Dodaj to kodo figuri `strela`, da se dvojnik premika navzgor, dokler ne doseže roba odra, nato pa je zbrisan.

![figura strele](images/lightning-sprite.png)

```blocks3
    ko začnem kot dvojnik
  pojdi na (raketa v)
  pokaži
  ponavljaj do <se dotika (roba)>
    spremeni y za (10)
  zbriši tega dvojnika
```

\--- /task \---

\--- task \---

Pritisni tipko <kbd>presledek</kbd>, da preizkusiš ali se strela pravilno premika.

\--- /task \---