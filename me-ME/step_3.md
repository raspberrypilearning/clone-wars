## Izrada svemirskog broda

Napravimo svemirski brod koji će braniti Zemlju!

+ Započni novi Scratch projekat i obriši lik mačke.

[[[generic-scratch-new-project]]]

+ Dodaj u svoj projekat pozadinu (backdrop) `zvijezde` i lik (sprite) `Svemirskog broda`.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Koristi alat **shrink** (smanji) da malo smanjiš lik `Svemirskog broda` i postavi ga u donji dio ekrana.

+ Kada je pritisnut taster sa strelicom **ulijevo**, svemirski brod treba da se kreće ulijevo. Dodaj ovaj kôd, da napraviš da se tvoj svemirski brod kreće ulijevo kada je pritisnuta strelica **ulijevo** (when the left arrow is pressed):

```blocks
    when flag clicked
    forever
        if <key [left arrow v] pressed?> then
            change x by (-4)
        end
    end
```

Pošto osa x ide slijeva nadesno na Pozornici, ako umanjiš x-poziciju svemirskog broda oduzimanjem, brod će se kretati ulijevo. Ovaj kôd je dio koji će učiniti da se tvoj svemirski brod kreće ulijevo:

```blocks
change x by (-4)
```

+ Dodaj još kôda unutar bloka `forever`{:class="blockcontrol"} (ponavljaj) da napraviš da se tvoj svemirski brod kreće udesno kada je pritisnut taster sa strelicom **udesno**.

Ako smo oduzimanjem `4` od pozicije svemirskog broda napravili da se on kreće ulijevo, kako možeš da napraviš da se kreće udesno za `4`? --- /hint --- --- hint --- Treba da koristiš isti blok, samo sa drugim brojem:

```blocks
change x by ( )
```

--- /hint --- --- hint --- Ovdje je kôd koji treba da dodaš ispod prethodno dodatog kôda unutar bloka `forever`{:class="blockcontrol"} (ponavljaj):

```blocks
if <key [right arrow v] pressed?> then
    change x by (4)
end
```

--- /hint --- --- /hints ---

+ Klikni na zelenu zastavicu i isprobaj svoj projekat. Možeš li da pokrećeš svoj svemirski brod ulijevo i udesno koristeći tastere sa strelicama?