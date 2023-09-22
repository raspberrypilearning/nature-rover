
--- question ---

---
legend: Ερώτηση 3 από 3
---

Αυτό το script είναι μια συνάρτηση που χρησιμοποιείται για να κάνει μια γάτα να χορέψει:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Ποιο από τα παρακάτω scripts θα χρησιμοποιούσε το παραπάνω `cat animation`{:class='block3myblocks'} για να κάνει τη γάτα να χορεύει όταν γίνεται κλικ στο Αντικείμενο;

--- choices ---

- ( )

```blocks3
when this sprite clicked
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

  --- feedback ---

  Αυτό θα έκανε τη γάτα να χορέψει, αλλά δεν χρησιμοποιεί το μπλοκ `cat animation `{:class='block3myblocks'} που έχει δημιουργηθεί.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  Αυτό καλεί ένα μπλοκ `cat dance`{:class='block3myblocks'}, αλλά όχι το μπλοκ `cat 
 animation`{:class='block3myblocks'}.

  --- /feedback ---

- ( )

```blocks3
when I receive [cat animation v]
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

  --- feedback ---

  Αυτό θα έκανε τη γάτα να χορέψει, αλλά όχι όταν γίνει κλικ στο αντικείμενο. Επίσης, δεν χρησιμοποιεί το μπλοκ `cat animation`{:class='block3myblocks'}.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Ναι, σε αυτή την απάντηση, χρησιμοποιείται το μπλοκ `cat animation`{:class='block3myblocks'} όταν γίνει κλικ στο αντικείμενο, προκαλώντας τον χορό της γάτας.

  --- /feedback ---

--- /choices ---

--- /question ---
