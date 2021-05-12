## Make the controller

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will create an on-screen controller that can be used to move your rover around the stage.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Open the starter project online at...
Offline ...

--- /task ---

You should see a scene with a robotic rover and a hilly background. 

--- task ---

Create a controller using 5 different sprites. One should be the body of the controller, and the other four are direction buttons. Here's an example to help you.

![image of a controller on the Scratch stage with four green buttons on a yellow oval background](images/controller.png)

--- /task ---

The rover needs to move when the direction buttons are clicked.

--- task ---

Add code to each button so that when they are clicked, they `broadcast`{:class="block3events"} their own name. You will need to create a `New message`{:class="block3events"} for each sprite. Here is an example for the `up` button.

```blocks3
when this sprite clicked
broadcast (up v)
```

--- /task ---

When the `up` and `down` buttons are clicked, the rover should change its `y` position, by a small amount. Increasing `y` will make the rover move up. Decreasing `y` will make the rover move down.

--- task ---

Add code so the buttons make the rover move up and down.

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)
```

--- /task ---

--- task ---

**Test:** your rover's controls by clicking on the up and down buttons.

--- /task ---

--- task ---

The rover needs to go back to the same starting position at the starn of each new mission.

```blocks3
when flag clicked
go to x: (0) y: (-90)
```
--- /task ---

You do not need to add code move the rover left and right yet. In the next step, you will add left and right controls.

--- save ---
