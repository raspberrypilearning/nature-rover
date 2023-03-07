
--- question ---

---
القائمة: السؤال 3 من 3
---

هذا البرنامج النصي هو دالة تستخدم للحصول على قطة للرقص:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

أي من النصوص البرمجية التالية سيستخدم `الرسوم المتحركة للقطط`{: class = 'block3myblocks'} أعلاه لجعل القطة ترقص عند النقر فوق Sprite؟

--- choices ---

- ( )

```blocks3
when this sprite clicked
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

  --- feedback ---

  هذا سيجعل القط يرقص، و لكن لا يستعمل `رسوم القط المتحركة`{:class='block3myblocks'} التي تم إنشاؤها.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  هذه تدعى مجموعة `رقصة القط`{:class='block3myblocks'}، و ليس مجموعة`رسوم القط المتحركة`{:class='block3myblocks'}.

  --- /feedback ---

- ( )

```blocks3
when I receive [cat animation v]
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

  --- feedback ---

  هذا سيجعل القط يرقص، لكن ليس عندما يتم نقر الكائن. كما أنه لا بستعمل مجموعة `رسوم القط المتحركة`{:class='block3myblocks'}.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

نعم، في هذا الجواب مجموعة `رسوم القط المتحركة`{:class='block3myblocks'} استُعملت عند نقر القط, جاعلة القط يرقص.

  --- /feedback ---

--- /choices ---

--- /question ---
