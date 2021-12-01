## Control the rover

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will use an on-screen controller or the keyboard to move your rover up and down.
</div>
<div>
![](images/step-2.gif){:width="300px"}
</div>
</div>

--- task ---

Open the starter project online at [rpf.io/nature-rover-starter](https://rpf.io/nature-rover-starter){:target="_blank"}.

--- collapse ---
---
title: Working offline
---

If you are working offline, the starter project can be found at [rpf.io/p/en/nature-rover-go](https://rpf.io/p/en/nature-rover-go)

--- /collapse ---


--- /task ---

You should see a scene with a robotic rover, a hilly background, and a controller in the bottom, left-hand corner.

![The staring background showing hills, a pile of mud, and a robot.](images/starter-background.png)

You are going to use the controller or keyboard controls to make the rover look as if it is moving towards or away from the viewer.

--- task ---

Look at the **Code** tab for each of the buttons. The code will look something like this:

![The up sprite.](images/up-sprite.png)

```blocks3
when this sprite clicked
broadcast (up v)

when I receive [start v]
forever
go to [front v] layer
go to x:(-190) y: (-121)
end
```

This keeps the buttons in the correct position, and broadcasts their directions when they are clicked.

--- /task ---

The **rover** is going to control the start of the game for all the other sprites; so when the green flag is clicked, the **rover** sprite needs to broadcast a `start`{:class='block3events'} message.

--- task ---

Add the broadcast to a `green flag clicked`{:class='block3events'} block.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when flag clicked
broadcast [start v]
``` 

--- /task ---

--- task ---

If you are working on a computer, it might be easier to use the keyboard controls, rather than using the buttons. Keyboard controls can be added to the **rover** sprite.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when [up arrow v] key pressed
broadcast [up v]

when [down arrow v] key pressed
broadcast [down v]

when [right arrow v] key pressed
broadcast [right v]

when [left arrow v] key pressed
broadcast [left v]
```

If you don't want to use the controller, then click on each of the **button** sprites and click on the `hide`{:class='block3looks'} block in the `looks`{:class='block3looks'} 
menu.

```blocks3
hide
```

--- /task ---

When the **up** button is clicked or the <kbd>up arrow</kbd> is pressed, the **rover** should change its `y`{:class="block3motion"} position by a small amount. Increasing `y`{:class="block3motion"} will make the **rover** move up. Decreasing `y`{:class="block3motion"} will make the **rover** move down.

--- task ---

Add code so the **up** button makes the **rover** move up.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)
```

--- /task ---

**You don't need to worry about the left and right motion yet. Left and right motion will be added in the next step of the project.**

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**Perspective**</span> is used in computer graphics to make a scene more realistic. Objects that are far away normally appear to be smaller and higher up the screen. Objects that are close appear to be larger and lower down the screen.
</p>

--- task ---

Add **perspective** to your **rover** by making it smaller when it moves upwards, and larger when it moves downwards.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)
change size by (-1) //Smaller looks further away


when I receive [down v]
change y by (-10)
change size by (1) //Bigger looks closer
```

--- /task ---

--- task ---

You'll need to reset the **rover's** size at the start of the game.

```blocks3
when I receive [start v]
set size to (50) %
```

--- /task ---


--- task ---

**Test:** Click the **up** and **down** buttons to check the control of your **rover**, or use the arrow keys.

--- /task ---

--- task ---

Now reset the position of the **rover** each time the game starts.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
+ go to x: (0) y: (-90)
```

--- /task ---

--- task ---

For now, the **rover** should appear in front of the other sprites. Move the **rover** to the front layer.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
+ go to [front v] layer
```

--- /task ---

--- task ---

**Test**: Click the green flag to test that your game resets correctly.

--- /task ---

--- save ---
