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

एक ब्लॉक जोड़ें ताकि**rover** स्प्राइट फलों का नमूना एकत्र करते समय ध्वनि बजाए।

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

**tree** स्प्राइट को दो अलग-अलग पोशाकें देने के लिए संपादित किया जाना चाहिए। एक जिस पर पर फल है (`tree with fruit`{:class="block3looks"}), और एक बिना फल वाला (`tree without fruit`{:class="block3looks"})। किसी एक पोशाक को संपादित करें, ताकि <**tree** में दो अलग-अलग पोशाकें हों।

--- /task ---

--- task ---

प्रॉजेक्ट के शुरू में **tree** की पोशाक और जब इसे `sample fruit`{:class="block3events"} प्रसारण प्राप्त होता है तो इसे जिस पोशाक में बदलना है सेट करने के लिए **tree** स्प्राइट पर ब्लॉक जोड़ें।

![tree स्प्राइट।](images/tree-sprite.png)

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

**rover** स्प्राइट पर, पोशाक परिवर्तन को ट्रिगर करने के लिए आप नये `broadcast`{:class="block3events"} का उपयोग कर सकते हैं। इस नए `broadcast`{:class="block3events"} को अपने `define sample fruit`{:class="block3myblocks"} फलन में जोड़ें।

![rover स्प्राइट।](images/rover-sprite.png)

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

**परिक्षण:** यह जांचने के लिए कि आपका कोड काम कर रहा है, झंडे पर क्लिक करें और फिर अपने **rover** स्प्राइट पर क्लिक करें। इसकी बाँह आगे बढ़नी चाहिए, और **tree** स्प्राइट को पोशाक बदलनी चाहिए।

**सलाह:** फुल स्क्रीन मोड पर स्विच करें और आप एनीमेशन को अधिक आसानी से देख पाएंगे।

--- /task ---

रोवर केवल तभी फल को इकट्ठा करने में सक्षम होना चाहिए, जब वह इसे छू रहा हो।

--- task ---

**रोवर** स्प्राइट पर, `when this sprite clicked`{:class="block3events"} ब्लॉक के सेट को बदलें, ताकि `sample fruit`{:class="block3myblocks"} फलन को केवल तभी कॉल किया जा सके जब **रोवर** आपके फल के रंग को छू रहा है।

**सलाह:** परीक्षण से आपके पोशाक परिवर्तन का अर्थ यह हो सकता है कि फल दिखाई नहीं दे रहा है। **tree** स्प्राइट के लिए कॉस्ट्यूम टैब पर क्लिक करें, और दृश्यमान फल के साथ पोशाक पर स्विच करें।

![rover स्प्राइट।](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

अब जब फल का नमूना ले लिया गया है **tree** स्प्राइट बदल जाता है, तो स्क्रीन से बाहर जाने पर आपको स्प्राइट को उसकी पहली पोशाक पर रीसेट करना होगा।

![tree स्प्राइट।](images/tree-sprite.png)

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

**परीक्षण:** **rover** स्प्राइट को हिलाएँ करें ताकि वह फल को छू सके, फिर **rover** स्प्राइट पर क्लिक करें और इसे पेड़ से फल इकट्ठा करते हुए देखें।

--- /task ---


--- save ---
