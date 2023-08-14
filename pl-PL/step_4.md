## Scroll more sprites

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
When adding more sprites to your scene, these need to scroll left and right as well.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

Now you can add some more objects to your scene, and scroll them in a similar way.

--- task ---

Add a **tree** sprite to your project, and then set its starting position.

![The tree sprite.](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(0) y:(-80)
```

--- /task ---

The **tree** sprite should also move in the **opposite** direction to the broadcast as well.

![Animation of a tree moving right and left, showing the x coordinate changing.](images/scrolling-tree.gif)

As the tree is closer to the viewer, it should appear to move a greater distance than the hills each time the button or key is pressed.

--- task ---

To get this moving effect, change the `x`{:class='block3motion'} values that the **tree** sprite moves by when the `left`{:class="block3events"} and `right`{:class="block3events"} broadcasts are received.

![The tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [left v]
change x by (10) //Use a bigger number than for the hills

when I receive [right v]
change x by (-10) //Use a bigger number than for the hills
```

--- /task ---

--- task ---

**Test:** Click the green flag and check your left and right buttons now. The tree should move each time you click on the controller.

**Test:** What happens if you go as far away from the tree as you can?

--- /task ---

Did you notice that when the tree reaches the very edge of the screen, it stops moving? You can fix this by moving the tree to the other side of the screen, when its `x`{:class='block3motion'} coordinate is too high or too low.

--- task ---

Using a `forever`{:class='block3control'} loop, and `if`{:class='block3control'} blocks, check the `x`{:class='block3motion'} coordinate of the tree, and move it to the other side of the screen when `x`{:class='block3motion'} is higher than `290` or lower than `-290`.

![The tree sprite.](images/tree-sprite.png)

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

Now move your **rover** sprite around the screen. When the tree reaches the edge, it should vanish off the edge of the screen and reappear on the other side.

--- /task ---

--- task ---

Lastly, make the **rover** turn left and right so that it faces the direction it is moving in, and resets at the start.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when flag clicked
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

**Test**: Run your project and test it. Make sure the tree appears to fall off the edge of the screen and appears on the other side when the rover moves.

--- /task ---
