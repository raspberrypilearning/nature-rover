## Adding more samples

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Add an introductory sentence. What will learners achieve by the end of this step?
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Create functions that use the other rover animations, in the same way you did for extending the arm.

Here is one to operate the rover's drill

```blocks3
define sample soil
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (drill 1 v)
wait (0.3) seconds
switch costume to (drill 2 v)
wait (0.3) seconds
switch costume to (drill 3 v)
wait (0.3) seconds
broadcast (sample soil v)
switch costume to (drill 2 v)
wait (0.3) seconds
switch costume to (drill 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

Use costume changes, size changes and graphics effects to change the appearance of the sprites, once they receive their broadcast.

Here is how the cloud is set up on the example provided.

```blocks3
when flag clicked
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

when I receive [sample air v]
repeat (5)
change size by (-10)
hide
```
--- /task ---

--- task ---

The functions can then be called when the rover is clicked and it is touching another sprite or colour.

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then
sample air ::custom
+ if <touching (cloud v) ?> then
sample air ::custom
+ if <touching (soil v) ?> then
sample soil ::custom
+ if <touching color (#87CEEB) ?> then
recharge ::custom
```

--- /task ---

--- save ---
