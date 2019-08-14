## Hipopotami-spațiali

Acum vei adăuga o mulțime de hipopotami zburători care încearcă să îți distrugă nava spațială.

--- task ---

Creează un nou personaj folosind imaginea „Hippo1” din biblioteca Scratch. Folosește unealta **de micșorare** pentru a face personajul `Hippo` o dimensiune similară cu personajul `Navă Spațială`.

![captură de ecran](images/invaders-hippo.png)

--- /task ---

--- task ---

Setează stilul de rotație al personajului `Hippo` să fie **stânga-dreapta**.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

Adaugă cod pentru a ascunde personajul `Hippo` când începe jocul.

![personaj hipopotam](images/hippo-sprite.png)

```blocks3
când se dă click pe stegulețul verde
ascunde
```

--- /task ---

--- task ---

Adaugă cod Scenei pentru a crea o nouă clonă a `Hippo` la fiecare câteva secunde.

--- hints ---


--- hint ---

Când `se face click pe stegulețul verde`{:class="block3events"}, `în mod repetat`{:class="block3control"} `așteaptă`{:class="block3control"} `între 2 și 4 secunde`{:class="block3operators"} și apoi `creează o clonă a personajului Hippo`{:class="block3control"}.

--- /hint ---

--- hint ---

Iată care sunt blocurile de care ai nevoie:

```blocks3
la infinit
end

creează o clonă a (Hippo1 v)

(alege aleator între (2) și (4))

când se dă click pe stegulețul verde

așteaptă () secunde
```

--- /hint ---

--- hint ---

Iată cum ar trebui să arate noul tău cod:

![personaj scena](images/stage-sprite.png)

```blocks3
când se face click pe stegulețul verde
la infinit 
  așteaptă (alege aleator între (2) și (4)) secunde
  creează o clonă a (Hippo1 v)
```

--- /hint ---

--- /hints ---

--- /task ---

Fiecare nouă clonă a hipopotamului ar trebui să apară la o poziție `x` aleatorie și fiecare clonă ar trebui să aibă o viteză aleatorie.

--- task ---

Creează o nouă variabilă numită `viteză`{:class="block3variables"} doar pentru personajul `Hippo`.

[[[generic-scratch3-add-variable]]]

Când ai făcut acest lucru corect, variabila va avea numele personajului alături, astfel:

![captură de ecran](images/invaders-var-test.png)

--- /task ---

--- task ---

Când fiecare clonă `Hippo` apare, alege o viteză aleatorie și locul de pornire pentru ea. Apoi, afișează clona pe ecran.

```blocks3
când încep ca și clonă
setează [viteză v] la (alege aleator între (2) și (4))
mergi la x (alege aleator între (-220) și (220)) y: (150)
arată
```

--- /task ---

--- task ---

Testează-ți codul. Apare un hipopotam nou la fiecare câteva secunde?

--- /task ---

Momentan hipopotamii nu se mișcă.

--- task ---

Fiecare hipopotam ar trebui să se miște la întâmplare până când este lovit de un fulger. Pentru a face acest lucru, atașează acest cod sub blocurile care sunt deja în script pentru personajul `Hippo`:

```blocks3
repetă până când <atinge (Fulger v) ?> 
  mergi (viteză :: variables) pași
  rotește la dreapta (alege aleator între (-10) și (10)) grade
  dacă atinge marginea, ricoșează
end
șterge această clonă
```

--- /task ---

--- task ---

Testează-ți din nou codul. Ar trebui să vezi o nouă clonă a hipopotamului ce apare la fiecare câteva secunde și fiecare clonă ar trebui să se miște cu o viteză diferită.

--- no-print ---

![captură de ecran](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

Acum testează tunul laser al navei spațiale. Dacă un fulger lovește un hipopotam, dispare hipopotamul?

--- /task ---