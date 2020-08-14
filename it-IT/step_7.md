## Ippopotami che scompaiono

Quando la navicella esplode, tutti gli ippopotami dovrebbero scomparire così che il giocatore possa riprendersi.

--- task ---

Aggiungi del codice allo sprite dell'astronave affinché `trasmetta`{:class="block3events"} il messaggio "colpito" quando `l'astronave tocca un ippopotamo`{:class="block3sensing"}.

![sprite razzo](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normale v)
wait until <touching (Ippopotamo v)>?
switch costume to (colpito v)
+ broadcast (colpito v)
```

--- /task ---

--- task ---

Tutti gli sprite dei cloni degli `Ippopotami` riceveranno il messaggio "colpito", e puoi far si che scompaiano quando la navicella viene colpita aggiungendo questo codice allo sprite dell'`Ippopotamo`:

![sprite ippopotamo](images/hippo-sprite.png)

```blocks3
when I receive [colpito v]
delete this clone
```

--- /task ---

--- task ---

Per verificare se il nuovo codice funziona, premi la bandierina verde e fai si che la navicella si scontri con un ippopotamo.

![schermata](images/invaders-hippo-collide.png)

--- /task ---

Dopo che l'astronave esplode, appaiono dei nuovi cloni di `Ippopotamo`, ma l'astronave è ancora esplosa! L'astronave deve resettarsi dopo esser stata colpita.

--- task ---

Aggiungi un blocco `attendere`{:class="block3control"} alla fine del codice dello sprite della `Navicella` per creare una piccola pausa prima che gli ippopotami inizino a comparire di nuovo. Poi aggiungi un blocco `per sempre`{:class="block3control"} attorno a tutto il codice per far si che si ripeta continuamente.

![sprite razzo](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normale v)
wait until <touching (Ippopotamo v)>?
switch costume to (colpito v)
broadcast (colpito v)
+ wait (1) seconds
end
```

--- /task ---