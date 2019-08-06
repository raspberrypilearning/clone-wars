## Svemirski nilski konji

Sada ćete dodati mnogo letećih nilskih konja koji pokušavaju uništiti vaš svemirski brod.

\--- task \---

Napravite novi lik sa slikom 'Hippo1' u Scratch biblioteci. Koristite **shrink** alat kako bi izradili `Hippo` lik slične veličine kao lik `svemirski brod`.

![screenshot](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Postavite stil rotacije lika `Hippo` na ** lijevo-desno **.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Dodajte naredbe kako bi sakrili lik `Hippo` kada igra započne.

![hippo sprite](images/hippo-sprite.png)

```blocks3
kada je kliknuta zelena zastava
sakrij
```

\--- /task \---

\--- task \---

Dodajte naredbe na pozornicu da biste stvorili novog `Hippo` klona svakih nekoliko sekundi.

\--- hints \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} and then `create a clone of the Hippo sprite`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Ovdje su blokovi koji vam trebaju:

```blocks3
ponavljaj
kraj

kloniraj (Hippo1 v)

(slučajni broj od (2) do (4))

kada je kliknuta zelena zastava

čekaj () sekundi
```

\--- /hint \---

\--- hint \---

Ovako bi trebao izgledati vaš kôd:

![stage sprite](images/stage-sprite.png)

```blocks3
kada je kliknuta zelena zastava
ponavljaj
    čekaj (slučajan broj od (2) do (4)) sekundi
    kloniraj (Hippo1 v)
kraj
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Svaki novi klon nilskog konja trebao bi se pojaviti nasumce </code>x</0> i svaki klon bi trebao imati slučajnu brzinu.

\--- task \---

Napravite novu varijablu koja se zove ` brzina ` {: class = "block3variables"} koja je samo za `Hippo` likove.

[[[generic-scratch3-add-variable]]]

Kada ste to napravili ispravno, varijabla ima pored sebe naziv lika, npr.:

![screenshot](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Kada je svaki `Hippo` klon počinje, odaberite mu slučajnu brzinu i ihsodište. Zatim pokažite klon na zaslonu.

```blocks3
kada krećem kao klon
postavi [brzina v] na (sličajan broj od (2) do (4))
idi na x: (slučajan broj od (-220) do (220)) y: (150)
prikaži
```

\--- /task \---

\--- task \---

Testirajte svoj kôd. Pojavljuje li se novi nilski konj svakih nekoliko sekundi?

\--- /task \---

Trenutno se nilski konji ne kreću.

\--- task \---

Svaki nilski konj bi se trebao kretati nasumično dok ga ne pogodi munja. Kako bi to bilo moguće, priložite ovaj kôd ispod blokova koji su već u skripti naredbi lika `Hippo-u`:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![screenshot](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---