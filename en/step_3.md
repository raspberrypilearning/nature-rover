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

Click on the Tree sprite in your starter project, and then set its starting position.

![The Tree sprite](images/tree-sprite.png)]

```blocks3
when flag clicked
go to x:(-90) y:(-80)
```

--- /task ---

The tree sprite should move in the **opposite** direction as the broadcast. So if the broadcast is `left`{:class="block3events"} then the `x`{:class="block3motion"} position will increase. If the broadcast is `right`{:class="block3events"} then the `x`{:class="block3motion"} of the tree will decrease.

![add GIF of tree moving gif showing dragging tree around (x coordinate changes)]

--- task ---

To get this moving effect, change the x values when the `left`{:class="block3events"} and `right`{:class="block3events"} broadcasts are recieved.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

--- /task ---

--- task ---

**Test:** your left and right buttons now. It should appear as if the rover moves towards and away from the tree.

**Test:** What happens if you go as far away from the tree as you can?

--- /task ---

Did you notice that the tree almost disappears, then it starts following the rover? To make the scene more realistic, the tree should stay in one place. 

--- task ---

Add to your scrolling effect and make the tree disappear when it gets far away enough from the rover.

--- /task ---


easy way to reset animation/game/scene


--- save ---
