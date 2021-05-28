## Collect an air sample

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Another way of making the rover appear to collect samples, is by changing some of the properties of a sprite, rather than it's costume.
</div>
<div>
![](images/step-5.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**Parallax scrolling**</span> is when background images move past the camera more slowly than foreground images
</p>

--- task ---

Add a cloud sprite to your project from the library of sprites in Scratch, or draw one yourself, and position and resize it below the sky so that the rover can reach it.

![image of the scratch scene, with an added cloud resized to 50%](images/add-cloud.png)

--- /task ---

--- collapse ---
---
title: Add graphic effects to the cloud
---

Using some graphic effects, change the appearance of the cloud sprite, so that it looks like a swirling ball of gas. You can play with different graphic effects, but the below example makes the sprite appear a little transparent and makes it swirl around.

![animation of the cloud swirling in a cycle](images/cloud.gif)

![cloud sprite](images/cloud-sprite.png)
```blocks3
when I receive [start v]
show
go to x: (190) y: (14)
clear graphic effects
set [ghost v] effect to (60)
set size to (50) %
forever
repeat (10)
change [whirl v] effect by (50)
end
repeat (20)
change [whirl v] effect by (-50)
end
repeat (10)
change [whirl v] effect by (50)
```

--- /collapse ---

For the cloud to scroll, it needs to move when it receives the `left`{:class='block3events'} and `right`{:class='block3events'} messages. As the cloud is further away from the viewer than the tree, it should move a smaller distance each time, and still dissapear off the edge of the screen and reappear on the other side. 

--- task ---

Add code to make the cloud move. You may need to adjust the numbers, depending on the size and position of the sprite. As the cloud should appear further back, it should move less than the tree.

![cloud sprite](images/cloud-sprite.png)
```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)

when I receive [start v]
+ forever
if <(x position) > (250)> then
set x to (-240)
end
if <(x position) < (-250)> then
set x to (240)
end
end
```

--- /task ---

Get the rover to collect the air sample.

--- task ---

Set up an animation function for the rover sprite, so that it can collect the air sample. You can duplicate the code from the sample tree function to do this.

--- collapse ---
---

title: Duplicating code

---

Here is an easy way of duplicating the code for your new function.

![animation showing code being duplicated](images/duplicating.gif)

--- /collapse ---

![rover sprite](images/rover-sprite.png)
```blocks3
define sample air
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (air 1 v)
wait (0.3) seconds
switch costume to (air 2 v)
wait (0.3) seconds
switch costume to (air 3 v)
wait (0.3) seconds
switch costume to (air 2 v)
wait (0.3) seconds
switch costume to (air 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

Get the rover to broadcast a message to the cloud sprite so that it knows when to animate.

--- task ---

Create a new broadcast message called `sample air`{:class='block3events'} and then add it into your `sample air`{:class='block3custom'} function.

![rover sprite](images/rover-sprite.png)
```blocks3
define sample air
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (air 1 v)
wait (0.3) seconds
switch costume to (air 2 v)
wait (0.3) seconds
switch costume to (air 3 v)
wait (0.3) seconds
+ broadcast (sample air v)
switch costume to (air 2 v)
wait (0.3) seconds
switch costume to (air 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

The function should only be called if the rover is touching the cloud sprite.

--- task ---

Add code so that the rover only `samples air`{:class='block3custom'} `if`{:class='block3control'} it is `touching the cloud`{:class='block3sensing'}.

![rover sprite](images/rover-sprite.png)
```blocks3
when this sprite clicked
if <touching color [Cloud v] ?> then
sample air ::custom
end
```

--- /task ---

Get the air sample to animate when the rover collects it. You can make it do what you like but in this example it disappears while being sucked up by the rover.

--- task ---

Add an animated effect to the cloud that changes the size.

![cloud sprite](images/cloud-sprite.png)
```blocks3
when I receive [sample air v]
repeat (5)
change size by (-10)
hide
end
set size to (50) %
```

--- /task ---

--- task ---

**Test** your project by clicking the green flag and then moving your rover until it touches the cloud. Click on the rover and it should appear to suck up the cloud.

--- /task ---

--- task ---

Now change your cloud sprite's code so that it resets when it goes off the screen.

![cloud sprite](images/cloud-sprite.png)
```blocks3
when I receive [start v]
+ forever
if <(x position) > (250)> then
set x to (-240)
show
end
if <(x position) < (-250)> then
set x to (240)
show
end
end
```

--- /task ---



--- save ---
