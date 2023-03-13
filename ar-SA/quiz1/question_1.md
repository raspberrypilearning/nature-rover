## اختبار سريع

أجب على الاسئلة الثلاثة. هناك تلميحات لإرشادك إلى الإجابة الصحيحة.

عندما تجيب على كل سؤال، انقر فوق **تحقق من إجابتي**.

استمتع!


--- question ---

---
legend: السؤال 1 من 3
---

إليك وحدة تحكم تقوم بالبث لأعلى عند النقر فوق الزر لأعلى وأسفل عند النقر على الزر أسفل:

![أربعة أزرار تحكم](images/controller.png)

أي من مجموعات الأكواد التالية ستضيفها **لكائن الكشاف** لجعله يتحرك للأعلى و الأسفل

--- choices ---

- ( )

```blocks3
when flag clicked
forever
if <touching [فوق v]> then
change y by (10)
end
if <touching [تحت v]> then
change y by (-10)

```


  --- feedback ---

  هذا سيحرك الكشاف عند لمسه للزر، بدلاً من عند ضغط الزر.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  هذا سيحرك الكشاف عند نقره، بدلاً من عند نقر الأزرار.

  --- /feedback ---

- (x)

```blocks3
when I receive [فوق v]
change y by (10)

when I receive [تحت v]
change y by (-10)

```

  --- feedback ---

  نعم، يتلقى هذا البرنامج النصي عمليات البث لأعلى ولأسفل من أزرار وحدة التحكم ويجعل الكشاف يتحرك لأعلى ولأسفل.

  --- /feedback ---

- ( )

```blocks3
define فوق
change y by (10)

define تحت
change y by (-10)

```


  --- feedback ---

  هذا ينشئ دالة للتحرك لأعلى و أسفل، لكن بما أن الدوال لم تُستدعى، الكشاف لن يتحرك.

  --- /feedback ---

--- /choices ---

--- /question ---
