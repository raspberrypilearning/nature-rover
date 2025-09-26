## Κύλιση περισσότερων αντικειμένων

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Όταν προσθέτεις περισσότερα αντικείμενα στη σκηνή σου, αυτά πρέπει επίσης να κάνουν κύλιση αριστερά και δεξιά.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

Τώρα μπορείς να προσθέσεις μερικά ακόμη αντικείμενα στη σκηνή σου και να τα μετακινήσεις με παρόμοιο τρόπο.

--- task ---

Πρόσθεσε ένα αντικείμενο **tree** στο έργο σου και στη συνέχεια, όρισε την αρχική του θέση.

![Το αντικείμενο tree.](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(0) y:(-80)
```

--- /task ---

Το αντικείμενο **tree** θα πρέπει επίσης να κινείται προς την **αντίθετη** κατεύθυνση από την μετάδοση.

![Κίνηση ενός δέντρου που κινείται δεξιά και αριστερά, που δείχνει τη συντεταγμένη x να αλλάζει.](images/scrolling-tree.gif)

Καθώς το δέντρο είναι πιο κοντά στον θεατή, θα πρέπει να φαίνεται ότι κινείται κατά μεγαλύτερη απόσταση από τους λόφους κάθε φορά που πατάς το κουμπί ή το πλήκτρο.

--- task ---

Για να αποκτήσεις αυτό το κινούμενο εφέ, άλλαξε τις τιμές `x`{:class='block3motion'} με τις οποίες κινείται το αντικείμενο **tree** όταν λαμβάνονται μεταδόσεις `left`{:class="block3events"} και `right`{:class=" block3events"}.

![Το αντικείμενο tree.](images/tree-sprite.png)

```blocks3
when I receive [left v]
change x by (10) //Use a bigger number than for the hills

when I receive [right v]
change x by (-10) //Use a bigger number than for the hills
```

--- /task ---

--- task ---

**Δοκιμή:** Κάνε κλικ στην πράσινη σημαία και έλεγξε τώρα το αριστερό και το δεξί κουμπί. Το δέντρο πρέπει να μετακινείται κάθε φορά που κάνεις κλικ στο χειριστήριο.

**Δοκιμή:** Τι συμβαίνει αν απομακρύνεσαι όσο πιο μακριά μπορείς από το δέντρο;

--- /task ---

Παρατήρησες ότι όταν το δέντρο φτάσει στην άκρη της οθόνης, σταματά να κινείται; Μπορείς να το διορθώσεις μετακινώντας το δέντρο στην άλλη πλευρά της οθόνης, όταν η συντεταγμένη `x`{:class='block3motion'} είναι πολύ μεγάλη ή πολύ μικρή.

--- task ---

Χρησιμοποιώντας έναν βρόχο `για πάντα`{:class='block3control'} και μπλοκ `εάν`{:class='block3control'}, έλεγξε τις συντεταγμένες `x`{:class='block3motion'} του δέντρου και μετακίνησέ το στην άλλη πλευρά της οθόνης όταν το `x`{:class='block3motion'} είναι μεγαλύτερο από `290` ή μικρότερο από `-290`.

![Το αντικείμενο tree.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ forever
if <(x position) > (290)> then //The tree is at the far right
set x to (-280) //Move the tree to the far left
end
if <(x position) < (-290)> then //The tree is at the far left
set x to (280) //Move the tree to the far right
end
end
```

--- /task ---

--- task ---

Τώρα μετακίνησε το αντικείμενο **rover** τριγύρω στην οθόνη. Όταν το δέντρο φτάσει στην άκρη, θα πρέπει να εξαφανιστεί στην άκρη της οθόνης και να εμφανιστεί ξανά στην άλλη πλευρά.

--- /task ---

--- task ---

Τέλος, κάνε το **rover** να στρίψει αριστερά και δεξιά, έτσι ώστε να βλέπει προς την κατεύθυνση προς την οποία κινείται και να επανέρχεται στην αρχή.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when flag clicked
go to [front v] layer
broadcast [start v]
+ set rotation style [left-right v]

when I receive [left v]
point in direction (-90)

when I receive [right v]
point in direction (90)

when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
go to [front v] layer
+ point in direction (90)
```

--- /task ---

--- task ---

**Δοκιμή:** Τρέξε το έργο σου και έλεγξέ το. Βεβαιώσου ότι το δέντρο φαίνεται να εξαφανίζεται από την άκρη της οθόνης και να εμφανίζεται στην άλλη πλευρά όταν το ρομποτικό όχημα κινείται.

--- /task ---
