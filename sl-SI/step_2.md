## Ustvari raketo

Najprej ustvari raketo, ki bo branila Zemljo!

\--- task \---

Odpri začetni projekt imenovan 'Vojna klonov'.

**Spletno:** Odpri začetni projekt na [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){: target = "_ blank"}.

Če imaš Scratch uporabniški račun, lahko ustvariš kopijo s klikom na **Predelaj**.

** Brez povezave: ** prenesi začetni projekt iz [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go) {: target = "_ blank"} in ga nato odpri s pomočjo namiznega urejevalnika.

Če želiš prenesti in namestiti Namizni Scratch, ga lahko najdeš na [rpf.io/scratchoff](https://rpf.io/scratchoff){: target = "_ blank"}.

\--- /task \---

![začetni projekt](images/starter-project.png)

\--- task \---

Dodaj to kodo figuri rakete, da se bo raketa premikala v levo, če je pritisnjena <kbd>leva</kbd> smerna tipka:

![figura rakete](images/rocket-sprite.png)

```blocks3
    ko kliknemo na zastavico
  ponavljaj
    če <je pritisnjena tipka [puščica v levo v]?> potem
      spremeni x za (-4)
    konec
  konec
```

X-os poteka od leve do desne strani odra. To pomeni, da se raketa premika v levo, kadar odštevaš od vrednosti `x` pozicije, ki jo ima raketa. Ta blok je torej tisti del kode, ki premika tvojo raketo v levo:

```blocks3
spremeni x za (-4)
```

\--- /task \---

\--- task \---

Dodaj še nekaj kode v blok `ponavljaj`{:class="block3control"}, da se bo tvoja raketa pomikala v desno, če je pritisnjena <kbd>desna</kbd> smerna tipka.

\--- hints \---

\--- hint \---

Če si od `x` pozicije rakete odšteval `4`, se je ta premikala v levo. Kako bi lahko dosegel, da bi se raketa namesto tega pomikala za `4` v desno?

\--- /hint \---

\--- hint \---

Potrebuješ enako kodo, le število mora biti drugačno:

```blocks3
spremeni x za ( )
```

\--- /hint \---

\--- hint \---

To je koda, ki jo je potrebno dodati ostali kodi v bloku `ponavljaj`{:class="block3control"}:

![figura rakete](images/rocket-sprite.png)

```blocks3
če <key (right arrow v) pressed?> potem
    spremeni x za (4)
konec
```

\--- /hint \---

\--- /namigi \---

\--- /task \---

\--- task \---

Preizkusi svoj projekt s klikom na zeleno zastavico. Ali se ob pritiskanju na smerni tipki raketa premika levo ali desno?

\--- /task \---