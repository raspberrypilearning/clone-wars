## Creează o navă spațială

Mai întâi creează o navă spațială care să poată apăra Pământul!

--- task ---

Deschide proiectul Scratch de început „Războiul clonelor”.

**Online:** deschide proiectul de început la [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Dacă ai un cont Scratch, poți să creezi o copie dând click pe **Remix**.

**Offline:** descarcă proiectul de început de la [rpf.io/p/ro-RO/clone-wars-go](http://rpf.io/p/ro-RO/clone-wars-go){:target="_blank"}, iar apoi deschide-l folosind editorul offline.

Dacă trebuie să descarci și să instalezi editorul Scratch offline, îl poți găsi la [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![proiect de început](images/starter-project.png)

--- task ---

Adaugă acest cod la personajul navei spațiale pentru a face ca nava spațială să se deplaseze la stânga dacă tasta <kbd>stânga</kbd> este apăsată:

![personaj rachetă](images/rocket-sprite.png)

```blocks3
    când se dă click pe stegulețul verde
    la infinit
        dacă <tasta (săgeată stânga v) apăsată?>  atunci 
            modifică x cu (-4)
        end
    end
```

Axa x începe din partea stângă a scenei și continuă spre partea dreaptă. Asta înseamnă că nava spațială se deplasează la stânga atunci când vei scadea din valoarea `x` a personajului navei spațiale. Deci, acest cod este partea care face ca nava ta spațială să se deplaseze la stânga:

```blocks3
modifică x cu (-4)
```

--- /task ---

--- task ---

Adaugă mai mult cod in blocul `forever`{:class="block3control"} pentru a face ca nava ta spațială să se deplaseze la dreapta dacă tasta <kbd>dreapta</kbd> este apăsată.

--- hints ---


--- hint ---

Scăzând `4` din poziția `x` a navei spațiale a făcut-o să se deplaseze la stânga, deci cum poți face ca nava spațială să se deplaseze spre dreapta folosind `4`?

--- /hint ---

--- hint ---

Ai nevoie de același cod, dar cu un număr diferit:

```blocks3
modifică x cu ( )
```

--- /hint ---

--- hint ---

Iată codul pe care trebuie să îl adaugi sub celălalt cod în interiorul blocului `la infinit`{:class="block3control"}:

![personaj rachetă](images/rocket-sprite.png)

```blocks3
dacă <tasta (săgeată dreapta v) apăsată> atunci 
    modifică x cu (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Testează-ți proiectul dând click pe steagul verde. Poți apăsa săgețile pentru a face nava spațială să se deplaseze la stânga și la dreapta?

--- /task ---