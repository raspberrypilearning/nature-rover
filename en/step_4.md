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

Add a **Tree** sprite in to your project, and then set its starting position.

![The Tree sprite](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(0) y:(-80)
```

--- /task ---

The tree sprite should also move in the **opposite** direction as the broadcast as well.

![animation of tree moving right and left showing the x coordinate changing](images/scrolling-tree.gif)

As the **tree** is closer to the viewer, it should appear to move a greater distance than the **hills**.

--- task ---

To get this moving effect, change the x values when the `left`{:class="block3events"} and `right`{:class="block3events"} broadcasts are received.

![The Tree sprite](images/tree-sprite.png)
```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

--- /task ---

--- task ---

**Test:** your left and right buttons now. The tree should move each time you click on the controller.

**Test:** What happens if you go as far away from the tree as you can?

--- /task ---

Did you notice that when the tree reaches the very edge of the screen, it stops moving? You can fix this by moving the tree to the other side of the screen, when its `x`{:class='block3motion'} coordinate is too high or too low.

--- task ---

Using a `forever`{:class='block3control'} loop, and `if`{:class='block3control'} blocks, check the x coordinate of the tree, and move it to the other side of the screen when x is higher than `290` or lower than `-290`

![The Tree sprite](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ forever
if <(x position) > (290)> then //the tree is at the far right
set x to (-280) //move tree to far left
end
if <(x position) < (-290)> then //the tree is at the far left
set x to (280) //move tree to far right
end
end
```

--- /task ---

--- task ---

Now move your rover around the screen. When the tree reaches the edge, it should vanish off the edge of the screen and reappear on the other side.

--- /task ---

--- task ---

Lastly make the rover turn left and right so that if faces in the correct direction.

![rover sprite](images/rover-sprite.png)
```blocks3
when flag clicked
broadcast [start v]
+ set rotation style [left-right v]

when I receive [left v]
point in direction (-90)

when I receive [right v]
point in direction (90)
```

--- /task ---

--- task ---

**Test**: Run your project and test it. Make sure the tree appears to fall of the edge of the screen and appear on the other side when the rover moves.

--- /task ---