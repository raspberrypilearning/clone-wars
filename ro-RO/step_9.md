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

\--- hint \---

You code should look like this:

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

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
când se dă click pe stegulețul verde
la infinit 
  așteaptă (alege aleator între (5) și (10)) secunde
  creează o clonă a (Portocală v)
end
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

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

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    când primesc [lovit v]
    șterge această clonă
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    așteaptă până când <<atinge (Hippo1 v)?> sau <atinge (Portocală v)?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---