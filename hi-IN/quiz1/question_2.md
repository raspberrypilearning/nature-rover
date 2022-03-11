## सोचिए


--- question ---

---
legend: 3 में से दूसरा प्रश्न
---

इस प्रोजेक्ट पर एक नज़र डालें जिसमें एक रोवर एक पर्वत दृश्य पर घूम रहा है।

![पृष्ठभूमि में हिलते हुए पहाड़ और एक स्थिर बादल के साथ रोवर दिखाते हुए एनीमेशन](images/mountain-animation.gif)

यहाँ पहाड़ को हिलाने का कोड है।

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

कौन सा कोड ब्लॉक बादल को पहाड़ की तुलना में धीमी गति से स्क्रॉल कराएगा?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---

बादल यहां पहाड़ की तुलना में धीमी गति से स्क्रॉल कर रहा है, लेकिन यह कोड रोवर के लिए बादल तक पहुंचना मुश्किल बना देता है क्योंकि यह रोवर के समान दिशा में चलता है।

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  इस कोड के साथ, बादल बाएँ और दाएँ के बजाय ऊपर और नीचे घूमेगा। आप बादल को बाएँ और दाएँ कैसे घुमा सकते हैं? मंच को एक समन्वय ग्रिड के रूप में सोचें।

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  बादल यहां सही दिशा में स्क्रॉल कर रहा है, हालांकि यह पहाड़ की तुलना में बहुत तेजी से स्क्रॉल कर रहा है, भले ही यह पहाड़ की तुलना में रोवर से बहुत दूर है।

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

बहुत बढ़िया! जब रोवर बाईं ओर चलता है तो बादल दाएँ चलता है, और जब रोवर दाएँ चलता है तो बाएँ।  बादल पर्वत की तुलना में धीमी गति से स्क्रॉल करता है क्योंकि x 5 की वृद्धि में बदला जाता है।

  --- /feedback ---

--- /choices ---

--- /question ---
