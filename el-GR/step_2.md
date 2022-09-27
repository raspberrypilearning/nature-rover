## Έλεγχος του ρομποτικού όχηματος

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Σε αυτό το βήμα, θα χρησιμοποιήσεις ένα χειριστήριο στην οθόνη ή το πληκτρολόγιο για να μετακινήσεις το ρομποτικό σου όχημα πάνω και κάτω.
</div>
<div>
![](images/step-2.gif){:width="300px"}
</div>
</div>

--- task ---

Άνοιξε το αρχικό έργο στο διαδίκτυο στη διεύθυνση [rpf.io/nature-rover-starter](https://rpf.io/nature-rover-starter){:target="_blank"}.

--- collapse ---
---
title: Εργασία εκτός σύνδεσης
---

Εάν εργάζεσαι εκτός σύνδεσης, μπορείς να βρείς το αρχικό έργο στη διεύθυνση [rpf.io/p/en/nature-rover-go](https://rpf.io/p/en/nature-rover-go)

--- /collapse ---


--- /task ---

Θα πρέπει να δεις μια σκηνή με ένα ρομποτικό όχημα, ένα φόντο με λόφους και ένα χειριστήριο στην κάτω, αριστερή γωνία.

![Το φόντο που πρωταγωνιστεί δείχνει λόφους, έναν σωρό λάσπης και ένα ρομπότ.](images/starter-background.png)

Θα χρησιμοποιήσεις το χειριστήριο στην οθόνη ή τα βελάκια του πληκτρολογίου για να κάνεις το ρομποτικό όχημα να φαίνεται σα να κινείται προς ή μακριά από το θεατή.

--- task ---

Κοίτα την καρτέλα **Κώδικας** για καθένα από τα κουμπιά. Ο κώδικας θα μοιάζει κάπως έτσι:

![Το αντικείμενο up.](images/up-sprite.png)

```blocks3
when this sprite clicked
broadcast (up v)

when I receive [start v]
forever
go to [front v] layer
go to x:(-190) y: (-121)
end
```

Αυτό διατηρεί τα κουμπιά στη σωστή θέση και μεταδίδει τις κατευθύνσεις τους όταν γίνεται κλικ.

--- /task ---

Το **ρομποτικό όχημα** θα ελέγχει την έναρξη του παιχνιδιού για όλα τα άλλα αντικείμενα. Έτσι, όταν κάνεις κλικ στην πράσινη σημαία, το αντικείμενο **rover** πρέπει να μεταδώσει ένα μήνυμα `start`{:class='block3events'}.

--- task ---

Πρόσθεσε τη μετάδοση σε ένα μπλοκ `όταν γίνει κλικ σε πράσινη σημαία`{:class='block3events'}.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when flag clicked
broadcast [start v]
```

--- /task ---

--- task ---

Εάν εργάζεσαι σε υπολογιστή, μπορεί να είναι πιο εύκολο να χρησιμοποιήσεις τα βελάκια του πληκτρολογίου, αντί να χρησιμοποιήσεις τα κουμπιά. Τα βελάκια πληκτρολογίου μπορούν να προστεθούν στο αντικείμενο **rover**.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when [up arrow v] key pressed
broadcast [up v]

when [down arrow v] key pressed
broadcast [down v]

when [right arrow v] key pressed
broadcast [right v]

when [left arrow v] key pressed
broadcast [left v]
```

Εάν δεν θέλεις να χρησιμοποιήσεις το χειριστήριο, κάνε κλικ σε καθένα από τα αντικείμενα **button** και κάνε κλικ στο μπλοκ `εξαφανίσου`{:class='block3looks'} στο μενού `όψεις`{:class='block3looks'}.

```blocks3
hide
```

--- /task ---

Όταν κάνεις κλικ στο κουμπί **up** ή πατήσεις το <kbd>πάνω βελάκι</kbd>, το **rover** θα πρέπει να αλλάξει τη θέση του `y`{:class="block3motion"} κατά ένα μικρό ποσό. Η αύξηση του `y`{:class="block3motion"} θα κάνει το **rover** να ανέβει. Η μείωση του `y`{:class="block3motion"} θα κάνει το **rover** να μετακινηθεί προς τα κάτω.

--- task ---

Πρόσθεσε κώδικα ώστε το κουμπί **up** να κάνει το **rover** να κινηθεί προς τα πάνω.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)
```

--- /task ---

**Δεν χρειάζεται να ανησυχείς για την αριστερή και τη δεξιά κίνηση αυτή τη στιγμή. Η αριστερή και η δεξιά κίνηση θα προστεθούν στο επόμενο βήμα του έργου.**

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Η <span style="color: #0faeb0">**Προοπτική**</span> χρησιμοποιείται στα γραφικά υπολογιστή για να κάνει μια σκηνή πιο ρεαλιστική. Αντικείμενα που είναι πολύ μακριά συνήθως φαίνεται να είναι μικρότερα και υψηλότερα στην οθόνη. Τα αντικείμενα που βρίσκονται κοντά φαίνονται να είναι μεγαλύτερα και χαμηλότερα στην οθόνη.
</p>

--- task ---

Πρόσθεσε **προοπτική** στο **rover** σου κάνοντας το μικρότερο όταν κινείται προς τα πάνω και μεγαλύτερο όταν κινείται προς τα κάτω.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)
change size by (-1) //Smaller looks further away


when I receive [down v]
change y by (-10)
change size by (1) //Bigger looks closer
```

--- /task ---

--- task ---

Θα χρειαστεί να επαναφέρεις το μέγεθος του **rover** στην αρχή του παιχνιδιού.

```blocks3
when I receive [start v]
set size to (50) %
```

--- /task ---


--- task ---

**Δοκιμή:** Κάνε κλικ στα κουμπιά **up** και **down** για να επιβεβαιώσεις τον έλεγχο του **rover** ή χρησιμοποίησε τα πλήκτρα με τα βελάκια.

--- /task ---

--- task ---

Τώρα πρέπει να επαναφέρεις τη θέση του **rover** κάθε φορά που ξεκινά το παιχνίδι.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
+ go to x: (0) y: (-90)
```

--- /task ---

--- task ---

Προς το παρόν, το **rover** θα πρέπει να εμφανίζεται μπροστά από τα άλλα αντικείμενα. Μετακίνησε το **rover** στο προσκήνιο.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
+ go to [front v] layer
```

--- /task ---

--- task ---

**Δοκιμή**: Κάνε κλικ στην πράσινη σημαία για να ελέγξεις ότι το παιχνίδι σου κάνει επαναφορά στην αρχική θέση σωστά.

--- /task ---

--- save ---
