## Vesoljski povodni konji

Sedaj boš dodal veliko letečih povodnih konjev, ki bodo skušali uničiti tvojo raketo.

\--- task \---

Izberi figuro Hippo1' iz Scratch knjižnice in jo preimenuj v 'povodni'. Uporabi orodje za **manjšanje**, da bo figura `povodni` podobne velikosti, kot je figura `raketa`.

![posnetek zaslona](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Za figuro `povodni` konj nastavi stil vrtenja na **levo-desno**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Dodaj kodo, ki bo skrila figuro `povodnega` konja, ko se igra začne.

![figura povodnega konja](images/hippo-sprite.png)

```blocks3
ko kliknemo na zastavo
skrij
```

\--- /task \---

\--- task \---

Odru dodaj kodo, ki bo an vsakih nekaj sekund ustvarila dvojnika `povodnega` konja.

\--- hints \---

\--- hint \---

`Ko kliknemo na zastavo`{:class="block3events"}, `ponavljaj`{:class="block3control"} `čakanje`{:class="block3control"} `med 2 in 4 sekundami`{:class="block3operators"}, nato pa `ustvari dvojnika figure povodni`{:class="block3control"}.

\--- /hint \---

\--- hint \---

To so bloki, ki jih potrebuješ:

```blocks3
ponavljaj
konec

ustvari dvojnika (povodni v)

(naključno število med (2) in (4))

ko kliknemo na zastavo

počakaj () sekund
```

\--- /hint \---

\--- hint \---

Tvoja koda mora izgledati tako:

![figura odra](images/stage-sprite.png)

```blocks3
ko kliknemo na zastavo
ponavljaj
  počakaj (naključno število med (2) in (4)) sekund
  ustvari dvojnika (povodni v)
konec
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Vsak novi dvojnik povodnega konja se mora pojaviti na naključnem `x` položaju in vsak bi moral imeti naključno hitrost.

\--- task \---

Ustvari novo spremenljivko z imenom `hitrost`{:class="block3variables"}, ki bo narejena le za figuro `povodnega konja`.

[[[generic-scratch3-add-variable]]]

Če si to pravilno naredil, stoji poleg spremenljivke tudi ime figure, na tak način:

![posnetek zaslona](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Za vsakega dvojnika `povodnega konja` izberi naključno hitrost in položaj, kjer naj se pojavi. Potem naj se dvojnik pokaže na zaslonu.

```blocks3
ko začnem kot dvojnik
nastavi [hitrost v] na (naključno število med (2) in (4))
pojdi na x: (naključno število med (-220) in (220)) y:(150)
pokaži
```

\--- /task \---

\--- task \---

Preizkusi kodo. Ali se na vsakih nekaj sekund pojavi nov povodni konj?

\--- /task \---

Trenutno se povodni konji ne premikajo.

\--- task \---

Vsak povodni konj naj se giblje naključno, dokler ga ne zadene strela. V ta namen dodaj to kodo pod bloke, ki se že nahajajo v skripti figure `povodni` konj:

```blocks3
ponavljaj do <se dotika (blisk v) ?>
  pojdi (hitrost::Spremenljivka) korakov
  obrni se za (naključno število med (-10) in (10)) stopinj v desno
  odbij se, če si na robu
konec
zbriši tega dvojnika
```

\--- /task \---

\--- task \---

Ponovno preizkusi svojo kodo. Na vsakih nekaj sekund bi se moral pojaviti nov dvojnik povodnega konja, vsak dvojnik pa bi se moral premikati z drugačno hitrostjo.

\--- no-print \---

![posnetek zaslona](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Zdaj preizkusite laserski top rakete. Če strela zadene v povodnega konja, ali ta izgine?

\--- /task \---