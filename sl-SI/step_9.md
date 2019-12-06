## Vesoljski netopir

Da narediš svojo igor nekoliko bolj težavno, boš ustvaril še netopirja, ki na raketo meče pomaranče.

![netopir, ki meče pomarančo na raketo](images/bat-oranges.png)

\--- task \---

Dodaj figuro `netopir` in določi njegov slog vrtenja na **levo-desno**.

\--- /task \---

\--- task \---

Naredi, da se bo figura `netopir` `premikala`{:class="block3motion"} iz leve v desno na vrhu odra in da se bo to `ponavljalo`{:class="block3control"}.

![figura netopirja](images/bat-sprite.png)

```blocks3
ko kliknemo na zastavo
nastavi velikost na (50)%
ponavljaj
  pojdi (10) korakov
  odbij se, če si na robu
konec
```

Ne pozabi preizkusiti svoje kode.

\--- /task \---

Če si ogledaš videze netopirja, boš videl, da so štirje različni:

![posnetek zaslona](images/invaders-bat-costume.png)

\--- task \---

Uporabi blok `naslednji videz`{:class="block3looks"}, da bo netopir mahal s krili, medtem ko se bo premikal.

\--- hints \---

\--- hint \---

Po tem, ko se premakne, bi moral pokazati `naslednji videz`{:class="block3looks"} in `počakati`{:class="block3control"} kratek čas.

\--- /hint \---

\--- hint \---

Svoji kodi moraš dodati te bloke:

```blocks3
počakaj (0.3) sekund

naslednji videz
```

\--- /hint \---

\--- hint \--- Tvoja koda bi morala izgledati tako:

```blocks3
ko kliknemo na zastavo
nastavi velikost na (50)%
ponavljaj
pojdi (10) korakov
odbij se, če si na robu

+ naslednji videz
+ počakaj (0.3) sekund
konec
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Zdaj pa poskrbi, da bodo netopirji metali pomaranče!

\--- task \---

Odaj figuro `Orange` iz Scratch knjižnice in jo preimenuj v 'pomaranča'.

![posnetek zaslona](images/invaders-orange.png)

\--- /task \---

\--- task \---

Netopirju dodaj kodo, da bo `ko kliknemo na zastavo`{:class="block3events"}, figura `netopir` `ponavljala`{:class="block3control"} `počakaj`{:class="block3control"} `naključno`{:class="block3operators"} časa `med 5 in 10`{:class="block3operators"} sekundami in `ustvarila dvojnika`{:class="block3control"} figure `pomaranča`.

![figura netopirja](images/bat-sprite.png)

```blocks3
ko kliknemo na zastavo
pomavljaj
  počakaj (naključno število med (5) in (10)) sekund
  ustvari dvojnika (pomaranča v)
konec
```

\--- /task \---

\--- task \---

`Pomaranči` dodaj kodo, da bo vsak njen dvojnik padal, začenši od figure `netopirja`, proti dnu odra.

![figura pomaranče](images/orange-sprite.png)

```blocks3
    ko kliknemo na zastavo
  skrij

  ko začnem kot dvojnik
  pojdi na (netopir v)
  pokaži
  ponavljaj do <se dotika (roba v)?>
    spremeni za (-4)
konec
zbriši tega dvojnika
```

\--- /task \---

\--- task \---

Dodaj še nekaj kode v figuro `pomaranča`, da ko dvojnik `pomaranče` zadene figuro ` rakete`, izgine tudi dvojnik, da omogočimo namestitev nove rakete za igralca:

![figura pomaranče](images/orange-sprite.png)

```blocks3
    ko prejmem [zadetek v]
   zbriši tega dvojnika
```

\--- /task \---

\--- task \---

Spremeni kodo figure `raketa`, da bo figura "zadeta", kadat se dotakne figure `povodni` konje ali figure `pomaranča`:

![figura rakete](images/rocket-sprite.png)

```blocks3
    počakaj dokler ni <<se dotika (povodni v)>? ali <se dotika (pomaranča v)>?>
```

\--- /task \---

\--- task \---

Preizkusite svojo igro. Kaj se zgodi, če raketo zadene padajoča pomaranča?

\--- /task \---