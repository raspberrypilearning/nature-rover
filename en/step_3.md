## Add scrolling


<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
For the left and right movement of the rover, rather than making the rover move, you will make foreground and background sprites scroll to the left and right.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
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

--- task ---

Add more sprites to your project. You can add a `sun` sprite, a `cloud` sprite, and a `soil` sprite. You will have to draw the soil sprite yourself.

--- /task ---

--- task ---


Add code to poistion each sprite when the flag is clicked, and then to move the sprite when it receives the `left`{:class="block3events"} and `right`{:class="block3events"} messages. Objects that are close to you should appear low down and move quite a lot, such as the soil. Objects that are further away should appear higher up and move a small amount, such as the sun.

--- /task ---





--- save ---
