## नमुना गोळा करा

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
या टप्प्यात, तुम्ही नमुने गोळा करणारे रोव्हर दाखवण्यासाठी स्प्राइट आणि रोव्हरचे स्वरूप बदलाल.
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

**rover** स्प्राईटच्या कॉश्चुमकडे बघा. सहा ऍनिमेशन उपलब्ध आहेत. **rover** हे करू शकतो:
- त्याचा हात वाढवा

![रोव्हरचा हात वाढत असल्याचे दाखवणारे तीन कॉश्चुम.](images/arm-animation.png)

- जमिनीत ड्रिल करा
- हवेत चोखणे
- सोलर पॅनेल वाढवा
- फोटो घ्या
- काहीतरी स्कूप करा

--- /task ---

तुम्हाला Scratch मधील बरेच कोड संयोजित करायचे असल्यास, जसेकी अनेक कॉश्चुम बदल, तर `My Blocks`{:class="block3myblocks"} वापरणे उपयुक्त ठरते. यामुळे तुम्ही स्वतःचे कस्टम ब्लॉक्स तयार करू शकता.

तुमच्या **rover** स्प्राईटला प्रत्येक ऍनिमेशन साठी `My Block`{:class="block3myblocks"} असतील.

--- task ---

`My Blocks`{:class="block3myblocks"} मेनूमध्ये, **Make a Block** वर क्लिक करा, आणि तुमच्या नवीन ब्लॉकला नाव द्या `sample fruit`{:class="block3myblocks"}.

--- /task ---

तुमच्या स्क्रिप्टमध्ये नवीन ब्लॉक दिसला पाहिजे. तो असा दिसेल:

![rover स्प्राईट.](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

या ब्लॉकच्या खाली, काही `switch costume`{:class="block3looks"} ब्लॉक्स अटॅच करा आणि रोबोट ऍनिमेट करण्यासाठी `wait`{:class="block3control"} ब्लॉक.

**टीप:** तुमचा पहिला `switch costume`{:class='block3looks'} ब्लॉक आणि `wait`{:class='block3control'} ब्लॉक तयार करणे, त्यानंतर त्यांना डुप्लीकेट करणे, आणि वापरला जाणारा कॉश्चुम बदलणे जलद आहे.

![rover स्प्राईट.](images/rover-sprite.png)

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

Add a block so that the **rover** sprite plays a sound when it collects the fruit sample. You can find the **Collect** sound in the Sound gallery.

![rover स्प्राईट.](images/rover-sprite.png)

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

तुम्ही ऍनिमेशन बघण्यासाठी `define sample fruit`{:class="block3myblocks"} ब्लॉकवर क्लिक करू शकता. तुम्ही लहान स्क्रीनवर असलात, तर तुम्हाला जवळून बघण्याची आवश्यकता असू शकते.

तुम्ही हिरव्या झेंड्यावर क्लिक केल्यावर सुद्धा ऍनिमेशन रन होणार नाही, कारण तुम्ही अद्याप तुमच्या प्रोजेक्टमध्ये तुमचे नवीन `sample fruit block`{:class='block3myblocks'} वापरले नाही.

--- /task ---

--- task ---

तुमचा नवीन ब्लॉक वापरण्यासाठी, तुम्ही तो `event`{:class="block3events"} ब्लॉक मध्ये अटॅच करू शकता. `My Blocks`{:class="block3myblocks"} मेनूमध्ये, तुम्ही तयार केलेला ब्लॉक तुम्ही बघायला हवा. त्याचा खालील स्क्रिप्टमध्ये वापर करा.

![rover स्प्राईट.](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

**rover** स्प्राईटवर क्लिक करा, आणि तुम्ही ऍनिमेशन बघायला हवे.

--- /task ---

आता तुम्हाला रोव्हरला प्रत्यक्षात नमुना गोळा करण्याची गरज आहे. या उदाहरणात, रोव्हर झाडावरून फळ गोळा करेल.

--- task ---

The **tree** sprite needs two costumes, one without fruit on (`tree without fruit`{:class="block3looks"}), and one with fruit (`tree with fruit`{:class="block3looks"}). Add another costume to the **tree**, change the names and draw some fruit on the **with fruit** one.

![The 'tree with fruit' costume, with 5 light red circles on it to represent fruit](images/tree-with-fruit.png)

--- /task ---

--- task ---

On the **tree** sprite, add blocks to set the costume of the **tree** at the start of the project, and the costume it should switch to when it receives a `sample fruit`{:class="block3events"} broadcast.

![The tree sprite.](images/tree-sprite.png)

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

On the **rover** sprite, you can use the new `broadcast`{:class="block3events"} to trigger the costume change. Add this new `broadcast`{:class="block3events"} into your `define sample fruit`{:class="block3myblocks"} function.

![The rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
start sound (Collect v)
wait (0.3) seconds
+ broadcast (sample fruit v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

**Test:** To check that your code is working, click on the flag, and then click on your **rover** sprite. Its arm should extend, and the **tree** sprite should change costumes.

**Tip:** Switch to full screen mode and you will be able to see the animation more easily.

--- /task ---

The rover should only be able to collect the fruit, if it is touching it.

--- task ---

On the **rover** sprite, change the `when this sprite clicked`{:class="block3events"} set of blocks, so that the `sample fruit`{:class="block3myblocks"} function is only called if the **rover** sprite is touching the colour of your fruit.

**Tip:** Your costume change from testing might mean that the fruit is not visible. Just click on the costumes tab for the **tree** sprite, and switch to the costume with the visible fruit.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

Now that the **tree** sprite changes when a fruit is sampled, you need to reset the sprite to its first costume when it goes off the screen.

![The tree sprite.](images/tree-sprite.png)

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

**Test:** Move the **rover** sprite so that it is touching the fruit, then click on the **rover** sprite and watch it collect the fruit from the tree.

--- /task ---


--- save ---
