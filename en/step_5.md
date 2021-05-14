## Collect an air sample


<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Another way of making the rover appear to collect samples, is by changing some of the properties of a sprite, rather than it's costume.
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**Parallax scrolling**</span> is when...
</p>

--- task ---

Add a cloud sprite to your project from the library of sprites in Scratch, or draw one yourself, and position it below the sky.

--- /task ---

--- task ---

Using some graphic effects, change the appearance of the cloud sprite, so that it looks a little bit like a swirling ball of gas. You can play with different graphic effects, but the below example makes the sprite appear a little transparent and makes it swirl around.

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

--- /task ---

--- task ---

The cloud needs to move, when it receives the `left`{:class='block3events'} and `right`{:class='block3events'} messages. As the cloud is further away from the viewer than the tree, it should move a smaller distance each time, and still dissapear off the edge of the screen and reappear on the other side.

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)

when I receive [start v]
+ forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end
```

--- /task ---

--- task ---

Set up an animation function for the rover, so that it appears to collect the air sample.

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

--- task ---

Create a new broadcast message called `sample air`{:class='block3events'} and then add it into your `sample air`{:class='block3custom'} function.

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

--- task ---

The function should only be called, if the rover is touching the cloud.

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then
sample fruit ::custom
+ if <touching [cloud v]> ? then
sample air ::custom
```

--- /task ---

--- task ---

Add an animated effect to the cloud, so that it appears to be being sucked up by the rover. Here is an example created, by changing the size of the cloud.

```blocks3
when I receive [sample air v]
repeat (5)
change size by (-10)
hide
```

--- /task ---

--- task ---

**Test** your project by clicking the green flag and then moving your rover until it touches the cloud. Click on the rover and it should appear to suck up the cloud.

--- /task ---


--- save ---