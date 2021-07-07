## Reflection


--- question ---

---
legend: Question 2 of 3
---

Have a look at this project showing a rover exploring a mountain scene.

![animation showing rover with mountain moving in the background and a static cloud](images/mountain-animation.gif)

Here is the code for moving the mountain.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

Which code blocks would get the cloud to scroll slower than the mountain?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---
The cloud is scrolling slower than the mountain here, but this code makes the cloud difficult for the rover to reach because it moves in the same direction as the rover.
  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  With this code, the cloud will be moving up and down instead of left and right. How can you get the cloud to move left and right? Think about the stage as a coordinate grid.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  The cloud is scrolling in the right direction here, however it is scrolling much faster than the mountain, even though it is farther away from the rover than the mountain.

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

Great! the cloud moves right when the rover moves left, and left when the rover moves right.  The cloud scrolls slower than the mountain because x is changed in increments of 5.

  --- /feedback ---

--- /choices ---

--- /question ---
