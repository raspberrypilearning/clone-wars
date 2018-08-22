## Nilski konji koji nestaju

Kada je svemirski brod udaren, svi nilski konji treba da nestanu kako bi igraču dali mogućnost da se oporavi.

+ Dodaj blok svom kôdu da `pošalje` (broadcast) poruku ''udaren'' kada svemirski brod dodirne nilskog konja.

[[[generic-scratch-broadcast-message]]]

--- hints --- --- hint --- Napravi blok `broadcast` 'udaren' tako što ćeš prevući blok sa kartice **Events** (Događaji), a zatim kliknuti na padajući meni i izabrati **new message** (nova poruka). --- /hint --- --- hint --- Ovako treba da izgleda tvoj blok:

```blocks
broadcast [udaren v]
```

--- /hint --- --- hint --- Ovako treba da izgleda tvoj kôd:

```blocks
when flag clicked
switch costume to [normalan v]
wait until <touching [Hippo1 v]>?
switch costume to [udaren v]
broadcast [udaren v]
```

--- /hint --- --- /hints ---

Svi klonovi lika `Nilskog konja` će čuti ovu poruku, tako da sada možeš da im daš naredbu da nestanu kada je svemirski brod udaren.

+ Dodaj ovaj kôd liku `Nilskog konja`:

```blocks
when I receive [udaren v]
delete this clone
```

+ Isprobaj ovaj kôd tako što ćeš započeti novu igru i namjerno se sudariti sa nilskim konjem.

![screenshot](images/invaders-hippo-collide.png)

Nakon sudara, nilski konji počinju ponovo da se pojavljuju, a svemirski brod još uvijek eksplodira! Napravimo da svemirski brod može da se vrati u početno stanje nakon što je udaren.

+ Dodaj blok `forever`{:class="blockcontrol"} (ponavljaj) oko cijelog svog kôda da napraviš da se proces ponavlja, i blok `wait`{:class="blockcontrol"} (čekaj) na kraju, da dodaš malu pauzu prije nego što nilski konji počnu ponovo da se pojavljuju.

```blocks
when flag clicked
forever
    switch costume to [normalan v]
    wait until <touching [Hippo1 v]>?
    switch costume to [udaren v]
    broadcast [udaren v]
    wait (1) secs
end
```

--- challenge ---

### Izazov: životi i rezultat

Trenutno igrač ima neograničen broj života. Da li možeš u svoju igru da dodaš `živote`{:class="blockdata"}, `rezultat`{:class="blockdata"}, pa čak i `najbolji rezultat`{:class="blockdata"}?

[[[generic-scratch-high-score]]] --- /challenge ---