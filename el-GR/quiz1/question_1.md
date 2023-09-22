## Γρήγορο κουίζ

Απάντησε στις τρεις ερωτήσεις. Υπάρχουν συμβουλές που θα σε καθοδηγήσουν στη σωστή απάντηση.

Όταν έχεις απαντήσει σε κάθε ερώτηση, κάνε κλικ στο **Έλεγξε την απάντησή μου**.

Διασκέδασέ το!


--- question ---

---
legend: Ερώτηση 1 από 3
---

Ακολουθεί ένα ελεγκτής που μεταδίδει το μήνυμα up όταν γίνει κλικ στο κουμπί up και down όταν γίνει κλικ στο κουμπί down:

![ελεγκτής τεσσάρων κουμπιών](images/controller.png)

Ποια από τα ακόλουθα μπλοκ κώδικα θα προσθέσεις στο **αντικείμενο rover** για να το κάνεις να κινηθεί πάνω και κάτω

--- choices ---

- ( )

```blocks3
when flag clicked
forever
if <touching [up button v]> then
change y by (10)
end
if <touching [down button v]> then
change y by (-10)

```


  --- feedback ---

  Αυτό θα μετακινούσε το rover όταν αγγίζει τα κουμπιά, αντί όταν πιέζονται τα κουμπιά.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  Αυτό θα μετακινούσε το rover όταν γίνει κλικ πάνω του, αντί όταν γίνεται κλικ στα κουμπιά.

  --- /feedback ---

- (x)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)

```

  --- feedback ---

  Ναι, αυτό το script λαμβάνει τις μεταδόσεις up και down από τα κουμπιά του ελεγκτή και κάνει το rover να κινείται πάνω και κάτω.

  --- /feedback ---

- ( )

```blocks3
define up
change y by (10)

define down
change y by (-10)

```


  --- feedback ---

  Αυτό δημιουργεί συναρτήσεις για κίνηση up και down, αλλά καθώς οι λειτουργίες δεν καλούνται, το rover δεν θα κινηθεί.

  --- /feedback ---

--- /choices ---

--- /question ---
