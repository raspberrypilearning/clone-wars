## Liliac-spațial

Pentru a face jocul tău un pic mai greu, vei crea un liliac care aruncă portocale către nava spațială.

![un liliac aruncând o portocală către o nava spațială](images/bat-oranges.png)

\--- task \---

Adaugă un personaj `Liliac` și setează stilul lui de rotație să fie **stânga–dreapta**.

\--- /task \---

\--- task \---

Fă personajul `Liliac` să `meargă`{:class="block3motion"} de la stânga la dreapta în partea de sus a Scenei `la infinit`{:class="block3control"}.

![personaj liliac](images/bat-sprite.png)

```blocks3
când se dă click pe stegulețul verde
setează mărimea la (50) %
la infinit 
  mergi (10) pași
  dacă atinge marginea, ricoșează
end
```

Nu uita să îți testezi codul.

\--- /task \---

Dacă te uiți la costumele liliacului, poți vedea că are patru costume diferite:

![captură de ecran](images/invaders-bat-costume.png)

\--- task \---

Folosește blocul `costumul următor`{:class="block3looks"} pentru a face ca liliacul să își bată aripile în timp ce se mișcă.

\--- hints \---

\--- hint \---

După ce liliacul s-a mutat, ar trebui să arate `costumul următor`{:class="block3looks"} și apoi să `aștepte`{:class="block3control"} pentru o perioadă scurtă de timp.

\--- /hint \---

\--- hint \---

Trebuie să adaugi aceste blocuri la codul tău:

```blocks3
așteaptă (0.3) secunde

costumul următor
```

\--- /hint \---

\--- hint \--- Codul tău ar trebui să arate așa:

```blocks3
când se dă click pe stegulețul verde
setează mărimea la (50) %
la infinit 
mergi (10) pași
dacă atinge marginea, ricoșează

+ costumul următor
+ așteaptă (0.3) secunde
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Acum fă ca liliacul să arunce portocale!

\--- task \---

Adaugă un personaj `Portocală` din biblioteca Scratch.

![captură de ecran](images/invaders-orange.png)

\--- /task \---

\--- task \---

Adaugă cod liliacului tău, astfel încât `când se dă click pe stegulețul verde`{:class="block3events"}, personajul `Liliac` `la infinit`{:class="block3control"} `așteaptă`{:class="block3control"} pentru o perioadă `aleatorie`{:class="block3operators"} de timp între `5 și 10`{:class="block3operators"} secunde și apoi `creează o clonă`{:class="block3control"} a personajului `Portocală`.

![personaj liliac](images/bat-sprite.png)

```blocks3
când se dă click pe stegulețul verde
la infinit 
  așteaptă (alege aleator între (5) și (10)) secunde
  creează o clonă a (Portocală v)
end
```

\--- /task \---

\--- task \---

Adaugă cod personajului `Portocală` pentru a face ca fiecare dintre clonele sale să cadă, pornind de la personajul `Liliac` și căzând spre partea de jos a Scenei.

![personaj portocală](images/orange-sprite.png)

```blocks3
    când se dă click pe stegulețul verde
ascunde

când încep ca și clonă
mergi la (Liliac v)
arată
repetă până când <atinge (marginea v)?
  modifică y cu (-4)
end
șterge această clonă
```

\--- /task \---

\--- task \---

Adaugă cod personajului `Portocală` astfel încât atunci când o clonă `Portocală` lovește personajul `Navă Spațială`, clona dispare pentru a da jucătorului șansa de a reseta:

![personaj portocală](images/orange-sprite.png)

```blocks3
    când primesc [lovit v]
    șterge această clonă
```

\--- /task \---

\--- task \---

Modifică codul personajului tau `Navă Spațială`, astfel încât personajul devine „lovit” atunci când atinge un personaj `Hippo` sau un personaj `Portocală`:

![personaj rachetă](images/rocket-sprite.png)

```blocks3
    așteaptă până când <<atinge (Hippo1 v)?> sau <atinge (Portocală v)?>>
```

\--- /task \---

\--- task \---

Testează-ți jocul. Ce se întâmplă dacă nava spațială este lovită de o portocală în cădere?

\--- /task \---