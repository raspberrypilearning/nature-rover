## पृष्ठभूमि को स्क्रॉल करें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
यह दिखाने के लिए की रोवर बाएं और दाएं घूम रहा है, **rover** स्प्राइट हिलने के बजाय, **backgrown** स्प्राइट बाईं या दाईं ओर चलता है या स्क्रॉल करता है।
</div>
<div>
![](images/step-3.gif){:width="300px"}
</div>
</div>

--- task ---

**hills** स्प्राइट चुनें। खेल की शुरुआत में, आपको यह सुनिश्चित करने की ज़रूरत है कि यह सही स्थिति में है और पीछे की परत पर है।

![hills स्प्राइट।](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
```

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**लेयर्स **</span> स्पष्ट प्लास्टिक की एक के ऊपर एक रखी शीट की तरह हैं जिन पर आप चित्र बना सकते हैं। यदि ढेर के शीर्ष पर एक चित्र उसके नीचे के चित्र को ढक कर रही है, तो आप नीचे के चित्र को ठीक से नहीं देख पाएंगे। पृष्टभूमि के चित्र **पीछे वाली ** परत के पास होने चाहिए। देखनेवाले के करीब के चित्र **आगे की ** लेयर के पास होने चाहिए।
</p>

--- task ---

**hills** स्प्राइट को स्वयं की एक प्रति बनाने की आवश्यकता है। इन्हें `clones`{:class='block3control'} कहा जाता है। फिर, मूल स्प्राइट को स्क्रीन के एकदम दाईं ओर ले जाया जा सकता है।

![hills स्प्राइट।](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
+ create clone of [myself v] //Create a copy of the hills
+ change x by (460) //Move the original hills to the right of the screen
```

--- /task ---

जब `left`{:class='block3events'} और `right`{:class='block3events'} प्रसारण प्राप्त होते हैं, तो **hills** स्प्राइट हिलना चाहिए। सही दिशा में गतिमान होने का आभास देने के लिए, जब **रोवर** दाईं ओर घूम रहा हो तो पृष्ठभूमि **left** चलती है। हिलने की दिशा `broadcast`{:class='block3events'} के</strong> विपरीत ** होनी चाहिए</p>

इसलिए, यदि प्रसारण `left`{:class="block3events" है, तो `x`{:class="block3motion"} स्थिति बढ़ जाएगी। यदि प्रसारण `right`{:class="block3events"}है, तो **hills** का `x`{:class="block3motion"} घट जाएगा।

![Scratch मंच नीचे दाएं कोने में एक स्प्राइट और पृष्ठभूमि के रूप में दिखाया गया एक x y समन्वय प्रणाली के साथ दिखाया गया है।](images/scratch-grid.png)

--- task ---

**hills** स्प्राइट और उसके क्लोन की गति को नियंत्रित करने के लिए ब्लॉक जोड़ें।

![hills स्प्राइट।](images/hills-sprite.png)

```blocks3
when I receive [left v]
change x by (3)

when I receive [right v]
change x by (-3)
```

--- /task ---

--- task ---

**परिक्षण**: घूमने के लिए कंट्रोलर या <kbd>arrow</kbd> कुंजियों का उपयोग करें। रोवर को बाएँ और दाएँ चलते हुए दिखना चाहिए।

--- /task ---

इस समय पर, **hills** स्प्राइट की दो प्रतियां हैं: मूल और एक क्लोन। जब आप किसी एक के अंत तक पहुँचते हैं, तो आप देखेंगे कि स्क्रीन बिलकुल सफ़ेद है।

इसे ठीक करने के लिए, स्प्राइट और उसके क्लोन को बहुत दूर जाने पर स्क्रीन के दूसरी तरफ ले जाने की आवश्यकता होती है।

--- task ---

`scroll`{:class='block3events'} नामक एक नया प्रसारण बनाएं और इसे `start`{:class='block3events'} स्क्रिप्ट में जोड़ें।

![hills स्प्राइट।](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
create clone of [myself v]
change x by (460) 
+ broadcast [scroll v]
```

--- /task ---

--- task ---

यह पता लगाने के लिए कोड जोड़ें कि क्या **hills** स्प्राइट या उसका क्लोन बाईं या दाईं ओर बहुत दूर चला गया है, और फिर उनकी स्थिति को स्क्रीन के दूसरी तरफ रीसेट करें।

![hills स्प्राइट।](images/hills-sprite.png)

```blocks3
when I receive [scroll v]
forever
if <(x position) > (460)> then //The hills sprite is off the right side of the screen
set x to (-460) //Reset to the left side of the screen
end
if <(x position) < (-460)> then //The hills sprite is off the left side of the screen
set x to (460) //Reset to the right side of the screen
end
```

--- /task ---

--- task ---

**Test**: Click the green flag to reset the scene and then use the controller or <kbd>arrow</kbd> keys to move the **rover**. पृष्ठभूमि को स्क्रॉल करना चाहिए, और **rover** को कभी भी अंत तक नहीं पहुंचना चाहिए।

--- /task ---

--- save ---
