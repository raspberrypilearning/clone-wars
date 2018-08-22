## Munje

Dajmo svemirskom brodu moć da ispaljuje munje!

+ Dodaj lik `Lightning` (Munja) iz Scratch biblioteke (library).

+ Kada igra započne, lik `Munje` treba da bude sakriven sve dok svemirski brod ne počne da puca svojim laserskim topovima. Da to napraviš, dodaj ovaj kôd liku `Munje`:

```blocks
when green flag clicked
hide
```

Trenutno imaš ogromnu munju koju svemirski brod treba da ispali!

+ Dodaj kôd ispod prethodno dodatih blokova da smanjiš lik `Munje` i da ga okreneš obratno. Tako će izgledati da svemirski brod ispaljuje munju sa njenim oštrim vrhom naprijed.

```blocks
set size to (25) %
point in direction (-90 v)
```

+ Pređi na lik `Svemirskog broda` tako što ćeš kliknuti na njega u panelu Sprites (Likovi) ispod pozornice.

+ Dodaj novi kôd da napraviš da lik `Svemirskog broda` stvori novu munju svaki put kada se pritisne taster za **razmak**.

--- hints --- --- hint --- Ovdje je jedan pseudokôd za tebe:

Kada je kliknuto na zelenu zastavicu (when the green flag is clicked) Neprestano (forever) provjeravaj Ako je pritisnut taster za ** razmak** (if the space key was pressed), kreiraj klona (create a clone) lika `munje` --- /hint --- --- hint --- Ovdje su blokovi koji će ti biti potrebni:

![Hint](images/hint-lightning.png) --- /hint --- --- hint --- Ovdje je kôd koji će ti biti potreban:

```blocks
when flag clicked
forever
    if <key [space v] pressed?> then
        create clone of [Munja v]
    end
end
```

--- /hint --- --- /hints ---

+ Vrati se na lik `Munje`.

+ Svaki put kada je kreirana, munja treba da se pojavi, a zatim da se kreće nagore dok ne dođe do vrha ekrana. Tada treba da nestane.

--- hints --- --- hint ---

Kada se pojavi novi klon lika `Munje`:

+ Prikaži ga
+ Pomjeraj ga u više navrata nagore za `10`, dok ne dodirne vrh ekrana
+ Zatim izbriši klona --- /hint --- --- hint --- Ovdje su blokovi koji će ti biti potrebni:

![Pomjeraj munju](images/move-hint-lightning.png) Ovdje je kôd koji treba da dodaš liku `Munje`:

```blocks
    when I start as a clone
    show
    repeat until <touching [edge v] ?>
        change y by (10)
    end
    delete this clone
```

--- /hint --- --- /hints ---

+ Isprobaj lik `Munje` tako što ćeš kliknuti na zelenu zastavicu, a zatim pritisnuti taster za **razmak**. Kada pritisneš **razmak**, da li se munja pojavi i kreće prema vrhu ekrana? Koji problem možeš da primijetiš?

--- collapse ---
---
title: Odgovor
---
Uh — trenutno se munja uvijek ispaljuje sa istog mjesta, bez obzira na to gdje se nalazi svemirski brod!

Dodaj ovaj blok prije bloka `show`{:class="blocklooks"} (prikaži), da napraviš da se klon lika `Munje` pomjeri na poziciju lika `Svemirskog broda` prije nego što se pojavi. Tako će izgledati kao da svemirski brod ispaljuje munju.

```blocks
go to [Svemirski brod v]
```

--- /collapse ---

+ Pritisni taster za **razmak** da isprobaš da li se tvoja munja sada pravilno ispaljuje.

--- challenge ---

### Izazov: popravljanje munje

Šta se dešava ako držiš pritisnut taster za **razmak**? Da li možeš da upotrijebiš blok `wait`{:class="blockcontrol"} (čekaj) da to popraviš?

--- /challenge ---