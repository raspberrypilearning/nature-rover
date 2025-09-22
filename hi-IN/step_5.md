## एक नमूना एकत्र करें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
इस चरण में, आप रोवर को नमूने एकत्र करते हुए दिखाने के लिए एक स्प्राइट और रोवर के रूप को बदल देंगे।
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

**rover**> स्प्राइट की वेशभूषा को देखें। छह एनिमेशन उपलब्ध हैं। **rover** कर सकता है:
- उसकी बांह बढ़ा सकता है

![रोवर की भुजा को बढ़ती हुई दिखाते हुए तीन पोशाकें।](images/arm-animation.png)

- जमीन में ड्रिल कर सकता है
- हवा को खींच सकता है
- सौर पैनल को बढ़ा सकता है
- फोटो खींचे सकता है
- कुछ एकट्ठा करके उठा सकता है

--- /task ---

जब आप Scratch में बहुत सारे कोड व्यवस्थित करना चाहते हैं, जैसे कि कई पोशाक परिवर्तन, तो `My Blocks`{:class="block3myblocks"} का उपयोग करना उपयोगी होता है। यह आपको अपने स्वयं के कस्टम ब्लॉक बनाने की अनुमति देता है।

आपके **rover** स्प्राइट में हर एनीमेशन के लिए `My Block`{:class="block3myblocks"} होगा।

--- task ---

`My Blocks`{:class="block3myblocks"} मेन्यू में, **Make a Block**पर क्लिक करें, और अपने नए ब्लॉक को `sample fruit`{:class="block3myblocks"} को नाम दें।

--- /task ---

आपकी स्क्रिप्ट में एक नया ब्लॉक दिखना चाहिए। यह ऐसा दिखाई देना चाहिए:

![rover स्प्राइट।](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

रोबोट को एनिमेट करने के लिए, इस ब्लॉक के नीचे, कुछ `स्विच कॉस्ट्यूम`{:class="block3looks"} ब्लॉक और `wait`{:class="block3control"} ब्लॉक संलग्न करें।

**सलाह:** उनकी दूसरी प्रति बनाना और फिर उपयोग की गयी पोशाक को बदलने से अपना पहला `switch costume`{:class='block3looks'} ब्लॉक और `wait`{:class='block3control'} ब्लॉक बनाना जल्दी हो जाएगा ।

![rover स्प्राइट।](images/rover-sprite.png)

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

![rover स्प्राइट।](images/rover-sprite.png)

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

एनीमेशन देखने के लिए आप `define sample fruit`{:class="block3myblocks"} ब्लॉक पर क्लिक कर सकते हैं। यदि आपका स्क्रीन छोटा है तो, तो आपको ध्यान से देखने की आवश्यकता हो सकती है।

जब आप हरे झंडे पर क्लिक करते हैं तो एनीमेशन नहीं चलेगा, क्योंकि आपने अभी तक अपने नये `sample fruit block`{:class='block3myblocks'} का उपयोग अपने प्रोजेक्ट में नहीं किया है।

--- /task ---

--- task ---

अपने नए ब्लॉक का उपयोग करने के लिए, आप इसे `event`{:class="block3events"} ब्लॉक में संलग्न कर सकते हैं। `My Blocks`{:class="block3myblocks"} मेनू में, आपको अपने द्वारा बनाया गए ब्लॉक दिखना चाहिए। निम्नलिखित स्क्रिप्ट में इसका प्रयोग करें।

![rover स्प्राइट।](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

**rover** स्प्राइट पर क्लिक करें, और आपको एनीमेशन देखना चाहिए।

--- /task ---

अब आपको रोवर से वास्तव में एक नमूना एकत्र करवाने की आवश्यकता है। इस उदाहरण में, रोवर एक पेड़ से एक फल एकत्र करेगा।

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
wait (0.3) seconds
start sound (Collect v)
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
