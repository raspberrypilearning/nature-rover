## Συλλογή δείγματος

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Σε αυτό το βήμα, θα αλλάξεις την εμφάνιση ενός αντικειμένου και του rover για να εμφανίσεις το ρομποτικό όχημα να συλλέγει δείγματα.
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

Δες τις ενδυμασίες του αντικειμένου **rover**. Υπάρχουν έξι διαθέσιμα κινούμενα σχέδια. Το **rover** μπορεί:
- Να εκτείνει τον βραχίονα του

![Τρεις ενδυμασίες που δείχνουν τον βραχίονα του ρόβερ να εκτείνεται.](images/arm-animation.png)

- Να τρυπήσει στο έδαφος
- Να ρουφήξει αέρα
- Να επεκτείνει ένα ηλιακό πάνελ
- Να τραβήξει μια φωτογραφία
- Να μαζέψει κάτι

--- /task ---

Όταν θέλεις να οργανώσεις πολύ κώδικα στο Scratch, όπως πολλές αλλαγές ενδυμασιών, είναι χρήσιμο να χρησιμοποιήσεις το μενού `Οι Εντολές μου`{:class="block3myblocks"}. Αυτό σου επιτρέπει να δημιουργήσεις τα δικά σου προσαρμοσμένα μπλοκ.

Το αντικείμενό σου **rover** θα έχει μια συνάρτηση στο μενού `Οι Εντολές μου`{:class="block3myblocks"} για κάθε κινούμενη εικόνα.

--- task ---

Κάνε κλικ στο μενού `Οι Εντολές μου`{: class = "block3myblocks"} και έπειτα στο **Δημιουργία Εντολής** και ονόμασε αυτό το νέο μπλοκ `δείγμα φρούτου`{: class = "block3myblocks"}.

--- /task ---

Ένα νέο μπλοκ θα εμφανιστεί στο script σου. Θα μοιάζει έτσι:

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

Κάτω από αυτό το μπλοκ, επισύναψε μερικά μπλοκ `άλλαξε ενδυμασία`{:class="block3looks"} και μπλοκ `περίμενε`{:class="block3control"}, για να δώσεις κίνηση στο ρομπότ.

**Συμβουλή:** Είναι πιο γρήγορο να δημιουργήσεις το πρώτο μπλοκ `άλλαξε ενδυμασία`{:class='block3looks'} και μπλοκ `περίμενε`{:class='block3control'}, στη συνέχεια να τις αντιγράψεις και να αλλάξεις την ενδυμασία που χρησιμοποιείται.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

Add a block so that the **rover** sprite plays a sound when it collects the fruit sample. You can find the **Collect** sound in the Sound gallery.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ start sound (Collect v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---


--- task ---

Μπορείς να κάνεις κλικ στο μπλοκ `ορισμός δείγματος φρούτου`{:class="block3myblocks"} για να δεις την κινούμενη εικόνα. Εάν βρίσκεσαι σε μια μικρή οθόνη, ίσως χρειαστεί να κοιτάξεις προσεκτικά.

Ωστόσο, η κινούμενη εικόνα δεν θα εκτελείται όταν κάνεις κλικ στην πράσινη σημαία, καθώς δεν έχεις χρησιμοποιήσει ακόμη το νέο `μπλόκ δείγμα φρούτου`{:class='block3myblocks'} στο έργο σου.

--- /task ---

--- task ---

Για να χρησιμοποιήσεις το νέο σου μπλοκ, μπορείς να το επισυνάψεις σε ένα μπλοκ `συμβάντος`{:class="block3events"}. Στο μενού `Οι Εντολές μου`{:class="block3myblocks"}, θα πρέπει να δεις το μπλοκ που δημιούργησες. Χρησιμοποίησε το στο παρακάτω script.

![Το αντικείμενο rover.](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

Κάνε κλικ στο αντικείμενο **rover** και θα δεις το κινούμενο σχέδιο.

--- /task ---

Τώρα πρέπει να κάνεις το rover να συλλέξει πραγματικά ένα δείγμα. Σε αυτό το παράδειγμα, το rover θα συλλέξει έναν καρπό από ένα δέντρο.

--- task ---

The **tree** sprite needs two costumes, one without fruit on (`tree without fruit`{:class="block3looks"}), and one with fruit (`tree with fruit`{:class="block3looks"}). Add another costume to the **tree**, change the names and draw some fruit on the **with fruit** one.

![The 'tree with fruit' costume, with 5 light red circles on it to represent fruit](images/tree-with-fruit.png)

--- /task ---

--- task ---

On the **tree** sprite, add blocks to set the costume of the **tree** at the start of the project, and the costume it should switch to when it receives a `sample fruit`{:class="block3events"} broadcast.

![The tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [sample fruit v]
+ switch costume to (tree without fruit v)
```

--- /task ---

--- task ---

On the **rover** sprite, you can use the new `broadcast`{:class="block3events"} to trigger the costume change. Add this new `broadcast`{:class="block3events"} into your `define sample fruit`{:class="block3myblocks"} function.

![The rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
start sound (Collect v)
wait (0.3) seconds
+ broadcast (sample fruit v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

**Test:** To check that your code is working, click on the flag, and then click on your **rover** sprite. Its arm should extend, and the **tree** sprite should change costumes.

**Tip:** Switch to full screen mode and you will be able to see the animation more easily.

--- /task ---

The rover should only be able to collect the fruit, if it is touching it.

--- task ---

On the **rover** sprite, change the `when this sprite clicked`{:class="block3events"} set of blocks, so that the `sample fruit`{:class="block3myblocks"} function is only called if the **rover** sprite is touching the colour of your fruit.

**Tip:** Your costume change from testing might mean that the fruit is not visible. Just click on the costumes tab for the **tree** sprite, and switch to the costume with the visible fruit.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

Now that the **tree** sprite changes when a fruit is sampled, you need to reset the sprite to its first costume when it goes off the screen.

![The tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (tree with fruit v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (tree with fruit v)
end
end
```

--- /task ---

--- task ---

**Test:** Move the **rover** sprite so that it is touching the fruit, then click on the **rover** sprite and watch it collect the fruit from the tree.

--- /task ---


--- save ---
