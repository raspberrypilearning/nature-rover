## Scroll the background

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
For the rover to look like it's moving left and right, instead of the **rover** sprite moving, the **background** sprite moves or scrolls to the left or right.
</div>
<div>
![](images/step-3.gif){:width="300px"}
</div>
</div>

--- task ---

Select the **hills** sprite. At the start of the game, you need to make sure that it is in the correct position and on the back layer.

![The hills sprite.](images/hills-sprite.png)
```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
```

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**Layers**</span> are like stacked sheets of clear plastic that you can draw images on. If an image on the top of the stack is covering the image below it, you will not be able to see the bottom image properly. Background images should be near the **back** layer. Images closer to the viewer should be near the **front** layer.
</p>

--- task ---

The **hills** sprite needs to make a copy of itself. These are called `clones`{:class='block3control'}. Then, the original sprite can be moved to the far right-hand side of the screen.

![The hills sprite.](images/hills-sprite.png)
```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
+ create clone of [myself v] //Create a copy of the hills
+ change x by (460) //Move the origial hills to the right of the screen
```
--- /task ---

When the `left`{:class='block3events'} and `right`{:class='block3events'} broadcasts are received, the **hills** sprite should move. To give the appearance of moving in the correct direction, the background moves **left** when the **rover** is moving right. The direction of motion should be **opposite** to the `broadcast`{:class='block3events'}.

So, if the broadcast is `left`{:class="block3events"}, then the `x`{:class="block3motion"} position will increase. If the broadcast is `right`{:class="block3events"}, then the `x`{:class="block3motion"} of the **hills** will decrease.

![Scratch stage shown with a sprite in the bottom right-hand corner and an x y coordinate system shown as the backdrop.](images/scratch-grid.png)

--- task ---

Add blocks to control the motion of the **hills** sprite and its clone.

![The hills sprite.](images/hills-sprite.png)
```blocks3
when I receive [left v]
change x by (3)

when I receive [right v]
change x by (-3)
```

--- /task ---

--- task ---

**Test**: Use the controller or the <kbd>arrow</kbd> keys to move around. The rover should appear to be moving left and right.

--- /task ---

At the moment, there are two copies of the **hills** sprite. The original and a clone. When you get to the end of either one, you'll notice that the screen is just white.

To fix this, the sprite and its clone need to be moved to the other side of the screen, when they go too far.

--- task ---

Create a new broadcast called `scroll`{:class='block3events'} and add it to the `start`{:class='block3events'} script.

![The hills sprite.](images/hills-sprite.png)
```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
create clone of [myself v]
change x by (460) 
+ broadcast [scroll v]
```

--- /task ---

--- task ---

Add code to detect if the **hills** sprite or its clone have moved too far to the left or right, and then reset their positions to the other side of the screen.

![The hills sprite.](images/hills-sprite.png)
```blocks3
when I receive [scroll v]
forever
if <(x position) > (460)> then //The **hills** sprite is off the right side of the screen
set x to (-460) //Reset to the left side of the screen
end
if <(x position) < (-460)> then //The **hills** sprite is off the left side of the screen
set x to (460) //Reset to the right side of the screen
end
```
--- /task ---

--- task ---

**Test**: Use the controller or <kbd>arrow</kbd> keys to move the **rover**. The background should scroll, and the **rover** should never reach the end.

--- /task ---

--- save ---
