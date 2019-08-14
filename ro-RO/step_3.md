## Fulgere

Acum vei face ca nava spațială să poată trage cu fulgere!

--- task ---

Adaugă personajul `Fulger` din biblioteca Scratch.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Când jocul începe, personajul `Fulger` trebuie ascuns până când nava spațială va folosi tunurile cu laser.

Adaugă acest cod la personajul `Fulger`:

![personaj fulger](images/lightning-sprite.png)

```blocks3
când se dă click pe stegulețul verde
ascunde
```

--- /task ---

În acest moment, fulgerul este foarte mare în comparație cu nava spațială!

--- task ---

Sub codul pe care personajul `Fulger` îl are deja, adaugă câteva blocuri pentru a face personajul mai mic și pentru a îl întoarce cu susul în jos.

![personaj fulger](images/lightning-sprite.png)

```blocks3
setează mărimea la (25) %
orientează-te in direcția (-90)
```

Acum arată ca și cum părăsește nava spațială cu vârful înainte.

--- /task ---

--- task ---

Adaugă ceva cod la personajul `Navă spațială` pentru a crea o nouă clonă a fulgerului dacă tasta <kbd>spațiu</kbd> este apăsată.

--- hints ---


--- hint ---

`când se face click pe stegulețul verde`{:class="block3events"}, continuă să verifici `la infinit`{:class="block3control"} `dacă`{:class="block3control"} `tasta spațiu este apăsată?`{:class="block3sensing"}, și în acest caz `creează o clonă a personajului Fulger`{:class="block3control"}.

--- /hint ---

--- hint ---

Iată care sunt blocurile de care ai nevoie:

```blocks3
dacă <> atunci
end

la infinit
end

creează o clonă a (Fulger v)

<tasta (spațiu v) apăsată?>

când se dă click pe stegulețul verde
```

--- /hint ---

--- hint ---

Iată cum ar trebui să arate noul tău cod:

![personaj rachetă](images/rocket-sprite.png)

```blocks3
când se dă click pe stegulețul verde
la infinit 
  dacă <tasta (spațiu v) apăsată?> atunci 
    creează o clonă a (Fulger v)
    end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Ori de câte ori jocul creează o clonă a personajului `Fulger`, clona ar trebui să apară și apoi să se deplaseze în sus până ajunge în partea de sus a Scenei. Atunci clona ar trebui să dispară.

Adaugă acest cod la personajul `Fulger` astfel încât clonele acestuia să se deplaseze în sus până când ating marginea Scenei, iar apoi sunt șterse.

![personaj fulger](images/lightning-sprite.png)

```blocks3
    când încep ca și clonă
mergi la (Navă Spațială v)
arată
repetă până când <atinge (marginea v) ?> 
  modifică y cu (10)
end
șterge această clonă
```

--- /task ---

--- task ---

Apasă tasta <kbd>spațiu</kbd> pentru a testa dacă fulgerul se mișcă corect.

--- /task ---