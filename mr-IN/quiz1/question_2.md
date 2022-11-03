--- question ---

---
legend: Question 2 of 3
---

हा प्रोजेक्ट बघा जो पर्वताचे दृश्य शोधणारा रोव्हर दाखवतो.

![बॅकग्राऊंड आणि स्थीर क्लाऊड मध्ये हलणाऱ्या पर्वतासह रोव्हर दाखवणारे ऍनिमेशन](images/mountain-animation.gif)

पर्वत हलवण्यासाठी येथे कोड आहे.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

कोणत्या कोड ब्लॉक्सला पर्वतापेक्षा हळू स्क्रोल करण्यासाठी क्लाऊड मिळेल?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---

येथे क्लाऊड पर्वतापेक्षा हळू स्क्रोल करत आहे, परंतु हा कोड रोव्हरला पोहोचण्यासाठी क्लाऊडला कठीण बनवतो कारण तो रोव्हर प्रमाणे त्याच दिशेत हलतो.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  या कोडसह, क्लाऊड डावी आणि उजवी कडे ऐवजी वर आणि खाली हलेल. तुम्हाला डावी आणि उजवीकडे हलणारा क्लाऊड कसा मिळू शकतो? कोऑर्डीनेट ग्रीड प्रमाणे stage बद्दल विचार करा.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  येथे क्लाऊड उजव्या दिशेत स्क्रोल करत आहे, तरीसुद्धा तो पर्वतापेक्षा जास्त जलद स्क्रोल करतो, तो पर्वतापेक्षा रोव्हरपासून दूर असली तरीही.

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

उत्तम! रोव्हर डावीकडे हलल्यावर क्लाऊड उजवीकडे हलतो, आणि उजवीकडे हलल्यावर डावीकडे हलतो.  क्लाऊड पर्वतापेक्षा हळू स्क्रोल करतो कारण x 5 च्या वाढीमध्ये बदलतो.

  --- /feedback ---

--- /choices ---

--- /question ---
