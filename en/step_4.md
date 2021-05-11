## Collecting samples


<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will change the appearance of the sprites and the rover when the rover as samples are collected.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Look at the rovers costumes. There are four animations available. The rover can extend it's arm, drill in the ground, suck in air and extend a solar panel. You can add more animation sequences if you like, by duplicating and editing the costumes.

--- /task ---

When we want to organise a lot of code, such as several costume changes, it is useful to use a programming technique called functions. In Scratch functions are called `My Blocks`{:class="block3custom"}

In this first example, a function will be used to animate the rover's arm, to make it look like it is grabbing something.

--- task ---

In the `My Blocks`{:class="block3custom"} menu click on **Make a Block**, and name your new block `sample fruit`{:class="block3custom"}.

--- /task ---

A new block should appear in your script. It will look like this:

```blocks3
define sample fruit
```

--- task ---

Beneath this block, attach some `switch costume`{:class="block3looks"} and `wait`{:class="block3control"} blocks, to animate the robot

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

You can click on the `define sample fruit`{:class="block3custom"} block to see the animation happen. It won't run when we click the green flag though, as you have not yet **called** the function in your script.

--- /task ---

--- task ---

To use your new function, you can attach it to an `event`{:class="block3events"} block. In the `My Blocks`{:class="block3custom"} menu, you should see the block you made. Use it in the following script.

```blocks3
when this sprite clicked
sample fruit ::custom
```

--- /task ---

--- task ---

Click on the rover, and you should see the rover animation.

--- /task ---

Now you need to make the rover actually collect a sample. In this example, the rover will collect a fruit from a tree.

--- task ---

The tree sprite has been edited to give it two different costumes. One with a fruit on, and one without a fruit. Edit one of your sprites, so that it has two different costumes.

--- /task ---

--- task ---

Back on the rover sprite, you can create a new `broadcast`{:class="block3events"} that will be used to trigger the costume change. Add this new broadcast into your `define sample fruit`{:class="block3custom"} function.

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ broadcast (sample fruit v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

On the tree sprite, add blocks to set the costume of the tree at the start of the project, and the costume it should switch to when it receives the `sample fruit`{:class="block3evens"} broadcast.

```blocks3
when flag clicked
go to x: (-90) y: (-80)
switch costume to (tree1 v)

when I receive [sample fruit v]
switch costume to (tree2 v)
```

--- /task ---

--- task ---

Test that your code is working, by clicking on the flag, and then clicking on your rover. It's arm should extend, and the tree sprite should change costumes.

--- /task ---

The rover should only be able to collect the fruit, if it is touching it.

--- task ---

On the rover sprite, change the `when this sprite clicked`{:class="block3events"} set of blocks, so that the `sample fruit`{:class="block3custom"} function is only called if the rover is touching the colour of your fruit.

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then
sample air ::custom
```

--- /task ---

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
