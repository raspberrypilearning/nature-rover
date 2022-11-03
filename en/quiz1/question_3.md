
--- question ---

---
legend: Question 3 of 3
---

This script is a function that is used to get a cat to dance:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Which of the following scripts would use the `cat animation`{:class='block3myblocks'} above to make the cat dance when the Sprite is clicked?

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

  This would make the cat dance, but does not use the `cat animation`{:class='block3myblocks'} block that has been made.

  --- /feedback ---

- ( ) 

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  This is calling a `cat dance`{:class='block3myblocks'} block, but not the cat `cat animation`{:class='block3myblocks'} block.

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

  This would make the cat dance, but not when the sprite is clicked. It also does not use the `cat animation`{:class='block3myblocks'} block.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Yes, in this answer, the `cat animation`{:class='block3myblocks'} block is used when the sprite is clicked, causing the cat to dance.

  --- /feedback ---

--- /choices ---

--- /question ---
