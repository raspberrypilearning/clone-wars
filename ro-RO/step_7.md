## Hipopotami care dispar

Când nava spațială explodează, toți hipopotamii ar trebui să dispară, astfel încât jucătorii jocului să se poată recupera.

--- task ---

Adaugă cod custumului navei spațiale astfel încât să `difuzeze`{:class="block3events"} mesajul „lovit” când `nava spațială atinge un hipopotam`{:class="block3sensing"}.

![personaj rachetă](images/rocket-sprite.png)

```blocks3
când se dă click pe stegulețul verde
schimbă costumul la (normal v)
așteaptă până când <atinge (Hippo1 v) ?>
schimbă costumul la (lovit v)

+ difuzează (lovit v)
```

--- /task ---

--- task ---

Toate clonele personajului `Hippo` vor primi mesajul „lovit” și le poți instrui să dispară atunci când nava spațială este lovită adăugând acest cod personajului `Hippo`:

![personaj hipopotam](images/hippo-sprite.png)

```blocks3
când primesc [lovit v]
șterge această clonă
```

--- /task ---

--- task ---

Pentru a verifica dacă noul cod funcționează, dă click pe steagul verde și fă ca nava spațială să se ciocnească cu un hipopotam.

![captură de ecran](images/invaders-hippo-collide.png)

--- /task ---

După ce nava spațială explodează, noi clone `Hippo` apar, dar nava spațială este încă explodată! Nava spațială trebuie să se reseteze după ce a fost lovită.

--- task ---

Adaugă un bloc `așteaptă`{:class="block3control"} la sfârșitul codului personajului `Navă Spațială` pentru a crea o mică pauză înainte ca hipopotamii să înceapă să apară din nou. Apoi adaugă un bloc `la infinit`{:class="block3control"} în jurul întregului cod pentru a face codul să fie rulat în mod repetat.

![personaj rachetă](images/rocket-sprite.png)

```blocks3
când se dă click pe stegulețul verde
la infinit 
schimbă costumul la (normal v)
așteaptă până când <atinge (Hippo1 v)>?
schimbă costumul la (lovit v)
difuzează (lovit v)

+ așteaptă (1) secunde
end
```

--- /task ---