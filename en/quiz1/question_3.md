
--- question ---

---
legend: Question 3 of 3
---

is used  This script is a function that is used to get a cat to dance:

```blocks3
define cat animation
change costume to [costume 1 v]
wait (0.1) seconds
change costume to [costume 2 v]
wait (0.1) seconds
change costume to [costume 3 v]
wait (0.1) seconds
change costume to [costume 4 v]
wait (0.1) seconds
```

Which of the following scripts would call the function above to make the cat dance when the Sprite is clicked?

--- choices ---

- ( ) 

```blocks3
when this sprite clicked
change costume to [costume 1 v]
wait (0.1) seconds
change costume to [costume 2 v]
wait (0.1) seconds
change costume to [costume 3 v]
wait (0.1) seconds
change costume to [costume 4 v]
wait (0.1) seconds
```

  --- feedback ---

  This would make the cat dance, but does not call the function that has been made.

  --- /feedback ---

- ( ) 

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  This is calling a function called cat dance, but not the cat animation function.

  --- /feedback ---

- ( ) 

```blocks3
when I receive [cat animation v]
change costume to [costume 1 v]
wait (0.1) seconds
change costume to [costume 2 v]
wait (0.1) seconds
change costume to [costume 3 v]
wait (0.1) seconds
change costume to [costume 4 v]
wait (0.1) seconds
```

  --- feedback ---

  This would make the cat dance, but not when the sprite is clicked. It also does not call the cat animation function.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Yes, in this answer, the function is called when the sprite is clicked, causing the cat to dance.

  --- /feedback ---

--- /choices ---

--- /question ---
