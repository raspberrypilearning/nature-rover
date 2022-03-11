## एक और नमूना बनाएं

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
चुनें कि आगे रोवर कौनसा नमूना लेता है! क्या यह पौधे, कीड़े या जानवर की एक नई प्रजाति को देखता है? क्या इसे कुछ पानी या रहस्यमय तरल दिखाई देता है? क्या यह कुछ गंदगी या चट्टान, या यहां तक कि हवा का नमूना लेना चाहता है? या कुछ और?
</div>
<div>
![](images/step-6.gif){:width="300px"}
</div>
</div>

--- task ---

**चुनें:** रोवर के लिए इकट्ठा करने के लिए एक नया **sample** जोड़ें। आप इसे अपने प्रोजेक्ट में या तो प्रोग्राम संग्रह से किसी एक का चयन करके या अपना स्वयं का चित्र बनाकर जोड़ सकते हैं।

--- /task ---

अपने **sample** स्प्राइट से स्क्रॉल करवाएँ। यदि यह स्क्रीन पर नीचे की ओर है तो इसे और अधिक चलना चाहिए(`change x by`{:class='block3motion'} `5`से अधिक होना चाहिए), और यदि यह स्क्रीन पर ऊपर है तो इसे कम चलना चाहिए (`change x by`{:class='block3motion'} `5`से कम होना चाहिए)।

--- task ---

कोड जोड़ें ताकि आपका स्प्राइट स्क्रॉल करे।

--- /task ---

**चुनें:** इस पर निर्भर करते हुए कि आप रोवर को आगे क्या नमूना देना चाहते हैं, आप या तो पहले से मौजूद रोवर एनिमेशन का उपयोग कर सकते हैं, या पोशाक को डुप्लिकेट और संपादित करके अधिक एनीमेशन अनुक्रम बना सकते हैं।

--- task ---

आपके **rover** स्प्राइट में एक `My Blocks`{:class='block3myblocks'} ब्लॉक जोड़ें ताकि जब रोवर नया नमूना एकत्र करे तो उसे एनिमेट किया जा सके। आपके द्वारा बनाए गये `My Blocks`{:class='block3myblocks'} में से किसी एक से कोड को कॉपी और पेस्ट कर सकते हैं।

उदाहरण के लिए, यहाँ सौर ऊर्जा एकत्र करने के लिए एक पोशाक अनुक्रम दिया गया है:

![रोवर के साथ सौर पैनल का विस्तार करते हुए दिखाए गए तीन पोशाकें।](images/solar-animation.png)

पोशाकों की इस श्रृंखला को एनिमेट करने के लिए आप निम्नलिखित कोड का उपयोग कर सकते हैं:

```blocks3
define recharge
switch costume to [inactive v]
wait (0.3) seconds
switch costume to [solar 1 v]
wait (0.3) seconds
switch costume to [solar 2 v]
wait (0.3) seconds
switch costume to [solar 3 v]
wait (0.3) seconds
switch costume to [solar 2 v]
wait (0.3) seconds
switch costume to [solar 1 v]
wait (0.3) seconds
switch costume to [inactive v]
wait (0.3) seconds
```

--- /task ---

--- task ---

इसके बाद, आपके नये ब्लॉक `My Block`{:class='block3myblocks'} में एक नया संदेश`broadcast`{:class='block3events'} करें जो **sample** स्प्राइट में `costume`{:class='block3looks'} या `graphic effect`{:class='block3looks'}परिवर्तन का कारण बनेगा।

--- /task ---

--- task ---

यह पता लगाने के लिए कि क्या रोवर स्प्राइट को छू रहा है या स्प्राइट पर किसी रंग को छू रहा है, `if`{:class='block3control'} ब्लॉक का उपयोग करें ताकि तब केवल नये `My Block`{:class='block3myblocks'} का ही उपयोग किया जा सके फिर।

--- /task ---

--- task ---

यदि आप चाहें, तो स्प्राइट में एक एनीमेशन जोड़ें, ताकि रोवर द्वारा नमूना एकत्र करने पर उसका स्वरूप बदल जाए।

--- /task ---

--- save ---
