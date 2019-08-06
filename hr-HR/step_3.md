## Munje

Sada ćete dati svemirskom brodu mogućnost pucanja munja!

\--- task \---

Dodajte lik ` Munja ` iz Scratch biblioteke.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Kada se igra pokrene, munja bi trebala biti skrivena sve dok svemirski brod ne ispali laserske topove.

Dodaj ovaj kôd liku `Munja`:

![lightning sprite](images/lightning-sprite.png)

```blocks3
Kada je kliknuta zelena zastava
sakrij
```

\--- /task \---

Trenutno je munja puno veća u odnosu na svemirski brod!

\--- task \---

Ispod kôda koji je lik ` Munja ` već ima, dodajte nekoliko blokova kako bi lik bio manji i okrenite ga naopako.

![lightning sprite](images/lightning-sprite.png)

```blocks3
postavi veličinu na (25) %
okreni se u smjeru (-90)
```

Sada se ispaljuje šiljati kraj prvi iz svemirskog broda.

\--- /task \---

\--- task \---

Dodajte novi kôd liku ` Svemirski brod ` da bi ste stvorili novi klon munje ako je tipka <kbd> razmaknica</kbd> pritisnuta.

\--- pomoć \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- /pomoć \---

\--- hint \---

Ovdje su blokovi koji vam trebaju:

```blocks3
ako <> onda
kraj

pnovaljaj
kraj

kloniraj (Munja v)

kada je tipka (razmaknica) pritisnuta

kada je zelena zastava kliknuta
```

\--- /pomoć \---

\--- hint \---

Evo kako bi vaš novi kôd trebao izgledati:

![rocket sprite](images/rocket-sprite.png)

```blocks3
kada je kliknuta zelena zastava 
ponavljaj
    ako <tipka razmaknica pritisnuta?> onda
        kloniraj (Munja v)
    kraj
kraj
```

\--- /pomoć \---

\--- /pomoć \---

\--- /task \---

\--- task \---

Kad god igra stvori klon lika ` Munja `, klon bi se trebao pojaviti, a zatim pomaknuti prema gore sve dok ne dosegne vrh pozornice. Tada bi klon trebao nestati.

Dodajte ovaj kôd u lik ` Munja `, tako da se njegovi klonovi kreću prema gore sve dok ne dodirnu rub pozornice, a zatim se izbrišu.

![lightning sprite](images/lightning-sprite.png)

```blocks3
    kada krećem kao klon
    idi do (Svemirski brod v)
    prikaži
    ponavljaj dok nije <dodiruje (rub)?>
        promijeni y za (10)
    kraj
    izbriši klona
```

\--- /task \---

\--- task \---

Pokreni projekt i testiraj munje držeći pritisnutu razmaknicu.

\--- /task \---