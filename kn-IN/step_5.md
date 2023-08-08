## ಮಾದರಿಯನ್ನು ಸಂಗ್ರಹಿಸಿ

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ಈ ಹಂತದಲ್ಲಿ, ರೋವರ್ ಮಾದರಿಗಳನ್ನು ಸಂಗ್ರಹಿಸುವುದನ್ನು ತೋರಿಸಲು ನೀವು ಸ್ಪ್ರೈಟ್ ಮತ್ತು ರೋವರ್‌ನ ನೋಟವನ್ನು ಬದಲಾಯಿಸುತ್ತೀರಿ.
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

**rover** ಸ್ಪ್ರೈಟ್‌ನ ಉಡುಪುಗಳನ್ನು ನೋಡಿ. ಆರು ಅನಿಮೇಶನ್‌ಗಳು ಲಭ್ಯವಿರುತ್ತವೆ. **rover**:
- ಅದರ ತೋಳುಗಳನ್ನು ವಿಸ್ತರಿಸಬಹುದು

![ರೋವರ್‌ ತೋಳನ್ನು ವಿಸ್ತರಿಸುವುದನ್ನು ತೋರಿಸುತ್ತಿರುವ ಮೂರು ಉಡುಪುಗಳು.](images/arm-animation.png)

- ನೆಲವನ್ನು ಕೊರೆಯಬಹುದು
- ಗಾಳಿಯನ್ನು ಒಳಕ್ಕೆಳೆದುಕೊಳ್ಳಬಹುದು
- ಸೌರ ಫಲಕವನ್ನು ವಿಸ್ತರಿಸಬಹುದು
- ಚಿತ್ರವನ್ನು ತೆಗೆದುಕೊಳ್ಳಬಹುದು
- ಏನನ್ನಾದರೂ ಮೊಗೆದು ತೆಗೆಯಬಹುದು

--- /task ---

ಅನೇಕ ಉಡುಪುಗಳ ಬದಲಾವಣೆಗಳಂತಹ ಬಹಳಷ್ಟು ಕೋಡ್‌ಗಳನ್ನುನೀವು Scratch ನಲ್ಲಿ ಸಂಯೋಜಿಸಲು ಬಯಸಿದಾಗ, `My Blocks`{:class="block3myblocks"} ಉಪಯೋಗಿಸುವುದು ಉಪಯುಕ್ತವಾಗಿರುತ್ತದೆ. ಇದು ನಿಮಗೆ ನಿಮ್ಮದೇ ಆದ ಬ್ಲಾಕ್‌ಗಳನ್ನು ರಚಿಸಲು ಅನುವುಮಾಡಿಕೊಡುತ್ತದೆ.

ನಿಮ್ಮ **rover** ಸ್ಪ್ರೈಟ್‌ ಪ್ರತಿಯೊಂದು ಅನಿಮೇಶನ್‌ಗೆ `My Block`{:class="block3myblocks"} ಹೊಂದಿರುತ್ತದೆ.

--- task ---

`My Blocks`{:class="block3myblocks"} ಮೆನುನಲ್ಲಿ, **Make a Block** ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ, ಮತ್ತು ನಿಮ್ಮ ಹೊಸ ಬ್ಲಾಕ್‌ನ್ನು `sample fruit`{:class="block3myblocks"} ಎಂದು ಹೆಸರಿಸಿ.

--- /task ---

ನಿಮ್ಮ ಬರಹದಲ್ಲಿ ಹೊಸ ಬ್ಲಾಕ್‌ ಕಾಣಿಸಿಕೊಳ್ಳಬೇಕು. ಅದು ಈ ರೀತಿ ಕಾಣಿಸುತ್ತದೆ:

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

ಈ ಬ್ಲಾಕ್‌ ಕೆಳಗೆ, ರೋಬೋಟ್‌ನ್ನು ಅನಿಮೇಟ್‌ ಮಾಡಲು ಕೆಲವು `switch costume`{:class="block3looks"} ಬ್ಲಾಕ್‌ಗಳನ್ನು ಮತ್ತು `wait`{:class="block3control"} ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ.

**ಸಲಹೆ:** ನಿಮ್ಮ ಮೊದಲ `switch costume`{:class='block3looks'} ಬ್ಲಾಕ್‌ ಮತ್ತು `wait`{:class='block3control'} ಬ್ಲಾಕ್‌ ರಚಿಸುವುದು ಬೇಗ ಆಗುತ್ತದೆ, ನಂತರ ಅವುಗಳನ್ನು ನಕಲು ಮಾಡಿ, ಮತ್ತು ಉಪಯೋಗಿಸುತ್ತಿರುವ ಉಡುಪನ್ನು ಬದಲಾಯಿಸಿ.

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
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

**rover** ಸ್ಪ್ರೈಟ್‌ ಹಣ್ಣಿನ ಮಾದರಿಯನ್ನು ಸಂಗ್ರಹಿಸಿದಾಗ ಧ್ವನಿಯನ್ನು ನುಡಿಸುವಂತೆ ಬ್ಲಾಕ್‌ ಸೇರಿಸಿ.

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ start sound (Collect v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---


--- task ---

ನೀವು ಅನಿಮೇಶನ್‌ ನೋಡಲು `define sample fruit`{:class="block3myblocks"} ಬ್ಲಾಕ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಬಹುದು. ನೀವು ಸಣ್ಣ ಪರದೆಯನ್ನು ಉಪಯೋಗಿಸುತ್ತಿದ್ದರೆ, ನೀವು ಹತ್ತಿರದಿಂದ ನೋಡಬೇಕಾಗಬಹುದು.

ನೀವು ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ನಲ್ಲಿ ಇನ್ನೂ ನಿಮ್ಮ ಹೊಸ `sample fruit block`{:class='block3myblocks'} ಉಪಯೋಗಿಸಿಲ್ಲವಾದುದರಿಂದ ಹಸಿರು ಬಾವುಟದ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗಲೂ ಅನಿಮೇಶನ್‌ ರನ್‌ ಆಗುವುದಿಲ್ಲ.

--- /task ---

--- task ---

ನಿಮ್ಮ ಹೊಸ ಬ್ಲಾಕ್‌ನ್ನು ಉಪಯೋಗಿಸಲು, ನೀವು ಅದನ್ನು `event`{:class="block3events"} ಬ್ಲಾಕ್‌ಗೆ ಸೇರಿಸಬಹುದು. `My Blocks`{:class="block3myblocks"} ಮೆನುನಲ್ಲಿ, ನೀವು ಮಾಡಿದ ಬ್ಲಾಕ್‌ನ್ನು ನೀವು ನೋಡಬೇಕು. ಈ ಕೆಳಗಿನ ಬರಹದಲ್ಲಿ ಅದನ್ನು ಉಪಯೋಗಿಸಿ.

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

**rover** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ, ಮತ್ತು ನೀವು ಅನಿಮೇಶನ್‌ ನೋಡಬೇಕು.

--- /task ---

ಈಗ ನೀವು ರೋವರ್‌ ನಿಜವಾಗಿ ಮಾದರಿಯನ್ನು ಸಂಗ್ರಹಿಸುವಂತೆ ಮಾಡಬೇಕು. ಈ ಉದಾಹರಣೆಯಲ್ಲಿ, ರೋವರ್‌ ಮರದಿಂದ ಹಣ್ಣೊಂದನ್ನು ಸಂಗ್ರಹಿಸುತ್ತದೆ.

--- task ---

ಎರಡು ಬೇರೆ ಬೇರೆ ಉಡುಪುಗಳನ್ನು ಅದಕ್ಕೆ ಕೊಡಲು **tree** ಸ್ಪ್ರೈಟ್‌ನ್ನು ಎಡಿಟ್‌ ಮಾಡಬೇಕು. ಒಂದು ಹಣ್ಣು ಹಾಕಿಕೊಂಡು (`tree with fruit`{:class="block3looks"}), ಮತ್ತು ಒಂದು ಹಣ್ಣಿಲ್ಲದೆ (`tree without fruit`{:class="block3looks"}). **tree** ಗೆ ಎರಡು ಬೇರೆ ಬೇರೆ ಉಡುಪುಗಳು ಇರುವಂತೆ ಅವುಗಳಲ್ಲಿ ಒಂದು ಉಡುಪನ್ನು ಎಡಿಟ್‌ ಮಾಡಿ.

--- /task ---

--- task ---

**tree** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ, **tree** ಉಡುಪನ್ನು ಪ್ರಾಜೆಕ್ಟ್‌ ಪ್ರಾರಂಭದಲ್ಲಿ ಹೊಂದಿಸಲು, ಮತ್ತು ಅದು `sample fruit`{:class="block3events"} ಪ್ರಸಾರವನ್ನು ಸ್ವೀಕರಿಸಿದಾಗ ಬದಲಾಯಿಸಬೇಕಾದ ಉಡುಪಿಗೆ ಬ್ಲಾಕ್‌ಗಳನ್ನು ಸೇರಿಸಿ.

![ಮರ ಸ್ಪ್ರೈಟ್.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [sample fruit v]
+ switch costume to (tree without fruit v)
```

--- /task ---

--- task ---

**rover** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ, ಉಡುಪು ಬದಲಾವಣೆಯನ್ನು ಪ್ರಚೋದಿಸಲು ನೀವು ಹೊಸ `broadcast`{:class="block3events"} ಉಪಯೋಗಿಸಬಹುದು. ಈ ಹೊಸ `broadcast`{:class="block3events"} ನ್ನು ನಿಮ್ಮ`define sample fruit`{:class="block3myblocks"} ಫಂಕ್ಷನ್‌ ಒಳಗೆ ಸೇರಿಸಿ.

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

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

**ಪರೀಕ್ಷೆ:** ನಿಮ್ಮ ಕೋಡ್‌ ಕೆಲಸಮಾಡುತ್ತಿದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸಲು, ಬಾವುಟದ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ನಂತರ ನಿಮ್ಮ **rover** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ. ಅದರ ತೋಳುಗಳು ವಿಸ್ತರಿಸಬೇಕು, ಮತ್ತು **tree** ಸ್ಪ್ರೈಟ್‌ ಉಡುಪುಗಳನ್ನು ಬದಲಾಯಿಸಬೇಕು.

**ಸಲಹೆ:** ಫುಲ್‌ ಸ್ಕ್ರೀನ್‌ ಮೋಡ್‌ಗೆ ಬದಲಾಯಿಸಿ ಮತ್ತು ನೀವು ಅನಿಮೇಶನ್‌ನ್ನು ಇನ್ನೂ ಸುಲಭವಾಗಿ ನೋಡಬಹುದು.

--- /task ---

ರೋವರ್‌ ಹಣ್ಣನ್ನು ಸ್ಪರ್ಶಿಸುತ್ತಿದ್ದರೆ ಮಾತ್ರ, ಅದಕ್ಕೆ ಹಣ್ಣನ್ನು ಸಂಗ್ರಹಿಸಲು ಸಾಧ್ಯವಾಗಬೇಕು.

--- task ---

**rover** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ, `when this sprite clicked`{:class="block3events"} ಬ್ಲಾಕ್‌ಗಳ ಸೆಟ್‌ನ್ನು ಬದಲಾಯಿಸಿ, ಅದರಿಂದ **rover** ಸ್ಪ್ರೈಟ್‌ ನಿಮ್ಮ ಹಣ್ಣಿನ ಬಣ್ಣವನ್ನು ಸ್ಪರ್ಶಿಸುತ್ತಿದ್ದರೆ ಮಾತ್ರ `sample fruit`{:class="block3myblocks"} ಫಂಕ್ಷನ್‌ನ್ನು ಆಮಂತ್ರಿಸಲಾಗುತ್ತದೆ.

**ಸಲಹೆ:** ಪರೀಕ್ಷೆಯಿಂದ ನಿಮ್ಮ ಉಡುಪುಗಳ ಬದಲಾವಣೆಯು ಹಣ್ಣು ಕಾಣಿಸುತ್ತಿಲ್ಲ ಎಂದು ಅರ್ಥ ಕೊಡಬಹುದು. **tree** ಸ್ಪ್ರೈಟ್‌ಗೆ ಕಾಸ್ಟ್ಯೂಮ್‌ ಟ್ಯಾಬ್‌ ಮೇಲಷ್ಟೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ, ಮತ್ತು ಹಣ್ಣು ಕಾಣಿಸುತ್ತಿರುವ ಉಡುಪಿಗೆ ಬದಲಾಯಿಸಿ.

![ರೋವರ್‌ ಸ್ಪ್ರೈಟ್.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

ಈಗ **tree** ಸ್ಪ್ರೈಟ್ ಹಣ್ಣಿನ ಮಾದರಿ ಸಂಗ್ರಹಿಸಿದಾಗ ಬದಲಾಗುತ್ತದೆಯಾದುದರಿಂದ, ಅದು ಪರದೆಯಿಂದ ಹೊರಹೋದಾಗ ನೀವು ಸ್ಪ್ರೈಟ್‌ನ್ನು ಅದರ ಮೊದಲನೆಯ ಉಡುಪಿಗೆ ಮರುಹೊಂದಿಸಬೇಕು.

![ಮರ ಸ್ಪ್ರೈಟ್.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (tree with fruit v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (tree with fruit v)
end
end
```

--- /task ---

--- task ---

**ಪರೀಕ್ಷೆ:** **rover** ಸ್ಪ್ರೈಟ್‌ ಹಣ್ಣನ್ನು ಸ್ಪರ್ಶಿಸುವಂತೆ ಅದನ್ನು ಚಲಿಸಿ, ನಂತರ **rover** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ಅದು ಮರದಿಂದ ಹಣ್ಣು ಸಂಗ್ರಹಿಸುವುದನ್ನು ವೀಕ್ಷಿಸಿ.

--- /task ---


--- save ---
