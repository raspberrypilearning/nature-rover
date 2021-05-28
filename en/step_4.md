## Collect a sample

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will change the appearance of a sprite and the rover when the rover collects samples.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

Look at the rover's costumes. There are six animations available. The rover can:
- extend its arm
- drill in the ground
- suck in air
- extend a solar panel
- take a picture, or 
- scoop something up. 

--- /task ---

When we want to organise a lot of code, such as several costume changes, it is useful to use a programming technique called a **function**. In Scratch, functions are called `My Blocks`{:class="block3myblocks"}.

For your rover, each function will relate to one of the rover animations.

Now, use a function to animate the rover's arm, so it can grab the fruit from the tree sprite.

--- task ---

In the `My Blocks`{:class="block3myblocks"} menu click on **Make a Block**, and name your new block `sample fruit`{:class="block3myblocks"}.

--- /task ---

A new block should appear in your script. It will look like this:

![rover sprite](images/rover-sprite.png)
```blocks3
define sample fruit
```

--- task ---

Beneath this block, attach some `switch costume`{:class="block3looks"} blocks and `wait`{:class="block3control"} blocks, to animate the robot

![rover sprite](images/rover-sprite.png)
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

You can click on the `define sample fruit`{:class="block3myblocks"} block to see the animation happen. It won't run when we click the green flag though, as you have not yet **called** the function in your script.

--- /task ---

--- task ---

To use your new function, you can attach it to an `event`{:class="block3events"} block. In the `My Blocks`{:class="block3myblocks"} menu, you should see the block you made. Use it in the following script.

![rover sprite](images/rover-sprite.png)
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

The tree sprite should be edited to give it two different costumes. One with a fruit on (`tree 1`{:class="block3looks"}), and one without a fruit (`tree 2`{:class="block3looks"}). Edit one of your costumes, so that it has two different costumes.

--- /task ---

--- task ---

Back on the rover sprite, you can create a new `broadcast`{:class="block3events"} that will be used to trigger the costume change. Add this new broadcast into your `define sample fruit`{:class="block3myblocks"} function.

![rover sprite](images/rover-sprite.png)
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

![The Tree sprite](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ switch costume to (tree 1 v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [sample fruit v]
+ switch costume to (tree 2 v)
```

--- /task ---

--- task ---

Test that your code is working, by clicking on the flag, and then clicking on your rover. It's arm should extend, and the tree sprite 
should change costumes.

--- /task ---

The rover should only be able to collect the fruit, if it is touching it.

--- task ---

On the rover sprite, change the `when this sprite clicked`{:class="block3events"} set of blocks, so that the `sample fruit`{:class="block3custom"} function is only called if the rover is touching the colour of your fruit.

![rover sprite](images/rover-sprite.png)
```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then
sample fruit ::custom
```

--- /task ---

--- task ---

Now that the tree sprite changes when a fruit is sampled, you need to reset the sprite to it's first costume when it goes off the screen.0faeb0

![tree sprite](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (tree1 v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (tree1 v)
end
end
```

--- /task ---

--- save ---
