## Add more samples

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Choose what the rover samples next! Do they see a new species of plant, bug or animal? Do they see some water or mysterious liquid? Do they want to sample some dirt or a rock? Or something else?
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

**Choose:** Depending on what you want the rover to sample next, you can either use the rover animations that are there already, or create more animation sequences by duplicating and editing the costumes.

- create sprite set up
- add scrolling
- function for rover
- new broadcast
- rover touching sprite or colour
- optional - add animated change to sprite

--- task ---

Create functions that use the other rover animations, in the same way you did for extending the arm. Duplicate code from the other functions, changing the dropdowns.

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


--- task ---

Add more sprites to your project. You can add a `sun` sprite, a `cloud` sprite, and a `soil` sprite. You will have to draw the soil sprite yourself.

--- /task ---

--- task ---

Add code to poistion each sprite when the flag is clicked.

--- /task ---

When a sprite receives the `left`{:class="block3events"} and `right`{:class="block3events"} messages it shoudl move.

Objects that are appear close to you be low down and move quite a large distance, such as the soil. Objects that you want to appear further away should be higher up and move a small distance, such as the sun.

In this example the soil has the following blocks:

```blocks3
when flag clicked
go to x: (-57) y: (10)

when I receive [right v]
change x by (-20)

when I receive [left v]
change x by (20)
```

--- task ---

Add code to each of your sprites so that they move when they receive `left`{:class="block3events"} and `right`{:class="block3events"} messages.

--- /task ---



--- save ---
