## Add scrolling


<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
For the rover to move left and right, instead of the rover sprite moving, the foreground and background sprites move or 'scroll' to the left and right.
</div>
<div>
Add Gif showing how the scrolling works ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Add a tree sprite to your project, and then set its starting position.

```blocks3
when flag clicked
go to x:(-90) y:(-80)
```

--- /task ---

--- task ---

The tree sprite should move in the **opposite** direction as the broadcast. So if the broadcast is `left`{:class="block3events"} then the `x`{:class="block3motion"} position will increase. If the broadcast is `right`{:class="block3events"} then the `x`{:class="block3motion"} of the tree will decrease.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

--- /task ---

--- task ---

Test your left and right buttons now. It should appear as if the rover moves towards and away from the tree.

--- /task ---

sprites disappear when they reach a certain x/y (tree -290 290) 
gif showing dragging tree around (x coordinate changes)

easy way to reset animation/game/scene


--- save ---
