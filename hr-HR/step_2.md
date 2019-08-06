## Napravite svemirski brod

Prvo napravite svemirski brod koji može obraniti Zemlju!

\--- task \---

Otvorite početni projekt 'Clone wars' Scratch.

** Online: ** otvorite početni projekt na [ rpf.io/clone-wars-on ](http://rpf.io/clone-wars-on) {: Target = "_ blank"}.

Ako imate Scratch račun, možete napraviti kopiju klikom na ** Remix **.

** Offline: ** preuzmite početni projekt iz [ rpf.io/p/en/clone-wars-go ](http://rpf.io/p/en/clone-wars-go), a zatim ga otvorite pomoću izvanmrežnog editora.

Ako trebate preuzeti i instalirati izvanmrežni Scratch editor, možete ga pronaći na [ rpf.io/scratchoff ](https://rpf.io/scratchoff) {: Target = "_ blank"}.

\--- /task \---

![početni projekt](images/starter-project.png)

\--- task \---

Dodajte ovaj kôd svemirskom brodu da bi se svemirski brod pomaknuo lijevo ako je <kbd> lijevo </kbd> strelica je pritisnuta:

![lik rakete](images/rocket-sprite.png)

```blocks3
    kada je kliknuta zastava
    ponavljaj
        ako <tipka (strelica lijevo) pritisnuta?> onda
            promijeni x za (-4)
        end
    end
```

Os x ide s lijeve prema desnoj strani prozora. To znači da se svemirski brod pomiče ulijevo kada se oduzme vrijednost od ` x ` položaja svemirskog broda. Dakle, ovaj blok kôda je dio koji pomiče vaš svemirski brod lijevo:

```blocks3
promijeni x za (-4)
```

\--- /task \---

\--- task \---

Dodajte još naredbi unutar `forever`{:class="block3control"} bloka kako bi se svemirski brod kretao udesno ako je pritisnuta <kbd>right</kbd> tipka sa strelicom.

\--- hints \---

\--- hint \---

Oduzimanje `4` od položaja svemirskog broda `x` ga pomiče ulijevo, pa kako bi ste napravili da se svemirski brod pomakne udesno za `4`?

\--- /hint \---

\--- hint \---

Potreban vam je isti blok koda, ali s drugim brojem:

```blocks3
promijeni x za ( )
```

\--- /hint \---

\--- hint \---

Ovdje je kôd koji trebate dodati ispod drugog koda unutar ` ponavljaj ` {: class = "block3control"} bloka:

![sprite rakete](images/rocket-sprite.png)

```blocks3
ako <key (right arrow v) pressed?> onda
    promijeni za (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Testirajte svoj projekt klikom na zelenu zastavu. Možete li pritisnuti tipke sa strelicama kako bi se vaš svemirski brod pomaknuo lijevo i desno?

\--- /task \---