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

ब्लॉक जोडा जेणेकरून **rover** स्प्राईट फळ नमूना गोळा करतो तेव्हा साऊंड प्ले करेल.

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

**tree** स्प्राईट दोन वेगवेगळे कॉश्चुम देण्यासाठी एडिट करायला हवा. एक फळासहित (`tree with fruit`{:class="block3looks"}), आणि दुसरा फळाशिवाय (`tree without fruit`{:class="block3looks"}). एक कॉश्चुम एडिट करा, जेणेकरून **tree** ला दोन वेगवेगळे कॉश्चुम असतील.

--- /task ---

--- task ---

**tree** स्प्राईटवर, प्रोजेक्टच्या सुरूवातीला, **tree** चा कॉश्चुम सेट करण्यासाठी ब्लॉक्स जोडा, आणि त्याचा कॉश्चुम त्याला `sample fruit`{:class="block3events"} ब्रॉडकास्ट प्राप्त झाल्यावर बदलायला हवा.

![tree स्प्राईट.](images/tree-sprite.png)

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

**rover** स्प्राईटवर, कॉश्चुम बदल प्रवर्तीत होण्यासाठी तुम्ही नवीन `broadcast`{:class="block3events"} चा वापर करू शकता. हा नवीन `broadcast`{:class="block3events"} तुमच्या `define sample fruit`{:class="block3myblocks"} फंक्शन मध्ये जोडा.

![rover स्प्राईट.](images/rover-sprite.png)

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

**चाचणी:** तुमचा कोड काम करतो का ते तपासण्यासाठी, झेंड्यावर क्लिक करा, आणि त्यानंतर तुमच्या **rover** स्प्राईटवर क्लिक करा. त्याचा हात वाढवायला हवा, आणि **tree** स्प्राईटने कॉश्चुम बदलायला हवा.

**टीप:** फूल स्क्रीन मोड बदला आणि तुम्ही जास्त सहजतेने ऍनिमेशन बघू शकाल.

--- /task ---

रोव्हर त्याला स्पर्श करत असल्यासच केवळ फळ गोळा करू शकतो.

--- task ---

**rover** स्प्राईटवर, `when this sprite clicked`{:class="block3events"} ब्लॉक्सचा सेट बदला, जेणेकरून `sample fruit`{:class="block3myblocks"} फंक्शन तेव्हाच करा जेव्हा **rover** स्प्राईट तुमच्या फळाच्या रंगाला स्पर्श करेल.

**टीप:** चाचणीमधून तुमचा कॉश्चुम बदलला याचा अर्थ फळ दिसत नाही असा असू शकतो. **tree** स्प्राईट साठी केवळ कॉश्चुम टॅबवर क्लिक करा, आणि दिसणाऱ्या फळासह कॉश्चुम बदला.

![rover स्प्राईट.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

आता, **tree** स्प्राईट फळ नमूना घेतला गेल्यावर बदलतो, तुम्हाला स्प्राईट त्याच्या पहिल्या कॉश्चुमला रीसेट करणे आवश्यक आहे जेव्हा तो स्क्रीनवर जातो.

![tree स्प्राईट.](images/tree-sprite.png)

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

**चाचणी:** **rover** स्प्राईट हलवा जेणेकरून तो फळावर स्पर्श करेल, त्यानंतर **rover** स्प्राईटवर क्लिक करा आणि तो झाडावरून फळे गोळा करतो का ते बघा.

--- /task ---


--- save ---
