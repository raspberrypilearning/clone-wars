## Αστραπές

Ας δώσουμε στο διαστημόπλοιο τη δυνατότητα να ρίχνει αστραπές!

--- task ---

Πρόσθεσε το χαρακτήρα `Lightning` από τη βιβλιοθήκη του Scratch.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Όταν ξεκινήσει το παιχνίδι, ο χαρακτήρας `Lightning` θα πρέπει να είναι κρυμμένος μέχρι το διαστημόπλοιο να πυροδοτήσει τα κανόνια λέιζερ του.

Πρόσθεσε αυτόν τον κώδικα στο χαρακτήρα `Lightning`:

![χαρακτήρας αστραπής](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

Προς το παρόν, η αστραπή είναι πολύ μεγάλη σε σύγκριση με το διαστημόπλοιο!

--- task ---

Κάτω από τον κώδικα που έχει ήδη ο χαρακτήρας `Lightning`, πρόσθεσε μερικά μπλοκ για να κάνεις το χαρακτήρα μικρότερο και να τον γυρίσεις ανάποδα.

![χαρακτήρας αστραπής](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Τώρα μοιάζει σαν να πυροβολεί από τη μύτη του διαστημόπλοιου.

--- /task ---

--- task ---

Πρόσθεσε νέο κώδικα στο χαρακτήρα `Spaceship` για να δημιουργήσεις ένα νέο χαρακτήρα αστραπής όταν πατηθεί το πλήκτρο <kbd>space</kbd>.

--- hints ---


--- hint ---

`Εάν πατηθεί η πράσινη σημαία`{:class="block3events"}, συνέχισε να ελέγχεις `για πάντα`{:class="block3control"} `εάν`{:class="block3control"} το `κενό πλήκτρο πατηθεί`{:class="block3sensing"}, και σε αυτή την περίπτωση `δημιούργησε έναν κλώνο του χαρακτήρα της Αστραπής`{:class="block3control"}.

--- /hint ---

--- hint ---

Εδώ είναι τα μπλοκ που χρειάζεσαι:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (διάστημα v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

Έτσι πρέπει να φαίνεται ο νέος σου κώδικας:

![χαρακτήρας πύραυλου](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (διάστημα v) pressed?> then
		create clone of (Lightning v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Κάθε φορά που το παιχνίδι δημιουργεί έναν χαρακτήρα κλώνο `Lightning`, ο κλώνος θα πρέπει να εμφανιστεί και στη συνέχεια να κινηθεί προς τα πάνω μέχρι να φτάσει στην κορυφή του σκηνικού. Τότε ο κλώνος θα πρέπει να εξαφανιστεί.

Πρόσθεσε αυτόν τον κώδικα στο χαρακτήρα `Lightning` έτσι ώστε οι κλώνοι του να κινούνται προς τα πάνω μέχρι να αγγίξουν την άκρη του σκηνικού και μετά να διαγραφούν.

![χαρακτήρας αστραπής](images/lightning-sprite.png)

```blocks3
	when I start as a clone
	go to (Spaceship v)
    show
	repeat until <touching (όριο v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

Πάτησε το πλήκτρο <kbd>space</kbd> για να ελέγξεις αν οι αστραπές πλέον λειτουργούν όπως πρέπει.

--- /task ---