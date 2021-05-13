## Upgrade your project

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your rover needs to know when it has collected all the samples it can. Variables can help with this.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>


--- task ---

Create a new variable called `samples`{:class='block3variables'} and set it to `0` at the start of the game.

```blocks3
when I receive [start v]
go to x: (0) y: (-90)
+ set [samples v] to (0)
```

--- /task ---

Each time the rover collects a sample from the tree, the `samples`{:class='block3variables'} should increase by `1`.

--- task ---

Add a block to increase the `sample`{:class='block3variables'} when the `sample fruit`{:class='block3function'}



--- /task ---

--- collapse ---

---
title: Completed project
---

You can view the [completed project here](https://scratch.mit.edu/projects/485673032/){:target="_blank"}.

--- /collapse ---

--- save ---