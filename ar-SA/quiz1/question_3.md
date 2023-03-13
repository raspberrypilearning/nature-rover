
--- question ---

---
legend: السؤال 3 من 3
---

هذا البرنامج النصي هو دالة تستخدم للحصول على قطة للرقص:

```blocks3
define تحريك القط
switch costume to [زي 1 v]
wait (0.1) seconds
switch costume to [زي 2 v]
wait (0.1) seconds
```

أي من النصوص البرمجية التالية سيستخدم `الرسوم المتحركة للقطط`{: class = 'block3myblocks'} أعلاه لجعل القطة ترقص عند النقر فوق Sprite؟

--- choices ---

- ( )

```blocks3
when this sprite clicked
switch costume to [زي 1 v]
wait (0.1) seconds
switch costume to [زي 2 v]
wait (0.1) seconds
```

  --- feedback ---

  هذا سيجعل القط يرقص، و لكن لا يستعمل `رسوم القط المتحركة`{:class='block3myblocks'} التي تم إنشاؤها.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
رقصة القط ::custom
```

  --- feedback ---

  هذه تدعى مجموعة `رقصة القط`{:class='block3myblocks'}، و ليس مجموعة`رسوم القط المتحركة`{:class='block3myblocks'}.

  --- /feedback ---

- ( )

```blocks3
when I receive [تحريك القط v]
switch costume to [زي 1 v]
wait (0.1) seconds
switch costume to [زي 2 v]
wait (0.1) seconds
```

  --- feedback ---

  هذا سيجعل القط يرقص، لكن ليس عندما يتم نقر الكائن. كما أنه لا بستعمل مجموعة `رسوم القط المتحركة`{:class='block3myblocks'}.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
تحريك القط ::custom
```

  --- feedback ---

نعم، في هذا الجواب مجموعة `رسوم القط المتحركة`{:class='block3myblocks'} استُعملت عند نقر القط, جاعلة القط يرقص.

  --- /feedback ---

--- /choices ---

--- /question ---
