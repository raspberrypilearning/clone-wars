## Crea una navicella spaziale

Creiamo una navicella spaziale che difenderà la Terra!

\--- task \---

Apri il progetto per principianti 'Clone wars'.

**Online:** open the starter project at [rpf.io/clone-wars-on](https://rpf.io/clone-wars-on){:target="_blank"}.

Se hai un account su Scratch, puoi farne una copia cliccando su **Remix**.

**Offline:** download the starter project from [rpf.io/p/en/clone-wars-go](https://rpf.io/p/en/clone-wars-go), and then open it using the offline editor.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![progetto per principianti](images/starter-project.png)

\--- task \---

Aggiuhngi questo codice allo sprite della navicella per far si che si muova verso sinistra quando la freccetta <kbd>sinistra</kbd> viene premuta:

![sprite razzo](images/rocket-sprite.png)

```blocks3
    quando si clicca sulla bandiera
    per sempre
        se <key (left arrow v) pressed?> allora
            cambiare x a (-4)
        end
    end
```

L'asse x va da sinistra verso destra nella scena. Questo significa che la navicella si muoverà a sinistra quando si sottrarrà dal valore dello sprite della navicella il valore della posizione `x`. Quindi questo blocco di codice è la parte che permetterà alla navicella di spostarsi verso sinistra:

```blocks3
cambiare x a (-4)
```

\--- /task \---

\--- task \---

Aggiungi ancora altro codice nel blocco `forever`{:class="block3control"} per far si che la navicella si muova a destra quando la freccetta <kbd>destra</kbd> verrà premuta.

\--- hint \---

\--- hint \---

Sottraendo `4` dalla posizione `x` della navicella questa si muoverà verso sinistra, invece come puoi far si che si muova a destra di `4`?

\--- /hint \---

\--- hint \---

Hai bisogno dello stesso blocco di codice, solo che dovrai cambiare numero:

```blocks3
cambia x a ( )
```

\--- /hint \---

\--- hint \---

Qui c'è il codice che dovrai inserire sotto l'altro codice nel blocco `sempre`{:class="block3control"}:

![sprite razzo](images/rocket-sprite.png)

```blocks3
se <key (right arrow v) pressed?> allora
    cambia x a (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Prova il tuo progetto facendo clic sulla bandierina verde. Riesci a muovere la navicella prememndo le frecce a sinistra e a destra?

\--- /task \---