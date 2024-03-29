## Quick quiz

Answer the three questions. There are hints to guide you to the correct answer.

When you have answered each question, click on **Check my answer**.

Have fun!


--- question ---

---
legend: Question 1 of 3
---

Here is a controller that broadcasts up when the up button is clicked and down when the down button is clicked:

![four button controller](images/controller.png)

Which of the following code blocks would you add to **the rover sprite** to make it move up and down

--- choices ---

- ( ) 

```blocks3
when flag clicked
forever
if <touching [up button v]> then
change y by (10)
end
if <touching [down button v]> then
change y by (-10)

```


  --- feedback ---

  This would move the rover when it is touching the buttons, rather than when the buttons are pressed.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  This would move the rover when it was clicked on, rather than when the buttons are clicked on.

  --- /feedback ---

- (x)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)

``` 

  --- feedback ---

  Yes, this script receives the up and down broadcasts from the controller buttons and gets the rover to move up and down.

  --- /feedback ---

- ( ) 

```blocks3
define up
change y by (10)

define down
change y by (-10)

```


  --- feedback ---

  This creates functions for moving up and down, but as the functions are not called, the rover would not move.

  --- /feedback ---

--- /choices ---

--- /question ---
