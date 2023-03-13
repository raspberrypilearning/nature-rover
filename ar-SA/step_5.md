## جمع عيّنة

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
في هذه الخطوة، ستغير مظهر كائن والكشاف لإظهار الكشاف يجمع عينات.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

أنظر إلى زي كائن **الكشاف**. هناك ستة رسوم متحركة متوفرة. **الكشاف** يستطيع:
- مد ذراعه

![ثلاثة صور تظهر الكشاف يمد ذراعه.](images/arm-animation.png)

- خرق الأرض
- الحوم في الهواء
- تمديد لوحة شمسية
- التقاط صورة
- إلتقاط شيء ما

--- /task ---

عندما تريد تنظيم الكثير من الأكواد في سكراتش، مثل العديد من تغييرات الأزياء ، فمن المفيد استخدام `مجموعتي`{:class="block3myblocks"}. هذا يسمح لك بإنشاء كتلك الجاهزة.

كائنك **الكشاف** سيملك `كتلتي`{:class="block3myblocks"} لكل رسمة متحركة.

--- task ---

في قائمة `كتلتي`{:class="block3myblocks"}، اضغط على **اجعل مجموعة**، و سم كتلتك الجديدة `عينة فاكهة`{:class="block3myblocks"}.

--- /task ---

يجب أن تظهر مجموعة جديدة في البرنامج النصي الخاص بك. ستبدو كهذه:

![كائن الكشاف.](images/rover-sprite.png)

```blocks3
define عينة الفاكهة
```

--- task ---

تحت هذه المجموعة، اربط بعض كتل `أزياء التبديل`{:class="block3looks"} و كتل `انتظر`{:class="block3control"}, لتحريك رسوم الروبوت.

**نصيحة:** من الأسرع إنشاء أول مجموعة `تبديل زي`{:class='block3looks'} و مجموعة `انتظر`{:class='block3control'}، ثم نسخهما، و تبديل الأزياء المستخدمة.

![كائن الكشاف.](images/rover-sprite.png)

```blocks3
define عينة الفاكهة //حرّك الروبوت لجمع الفاكهة
switch costume to (خامل v)
wait (0.3) seconds
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (الذراع 2 v)
wait (0.3) seconds
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (خامل v)
```

--- /task ---

--- task ---

أضف مجموعة بحيث كائن **الكشاف** يصدر صوتاً عندما يجمع عينة فاكهة.

![كائن الكشاف.](images/rover-sprite.png)

```blocks3
define عينة الفاكهة //حرّك الروبوت لجمع الفاكهة
switch costume to (خامل v)
wait (0.3) seconds
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (الذراع 2 v)
wait (0.3) seconds
+ start sound (Collect v)
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (خامل v)
```

--- /task ---


--- task ---

يمكنك الضغط على مجموعة `عين عينة فاكهة`{:class="block3myblocks"} لرؤية الرسوم المتحركة. إذا كنت على شاشة صغيرة، قد تحتاج إلى النظر عن كثب.

لن يتم تشغيل الرسوم المتحركة عند نقرك على العلم الأخضر، لأنك لم تستخدم كتلك الجديد `عينة فاكهة`{:class='block3myblocks'} في مشروعك.

--- /task ---

--- task ---

لاستخدام مجموعتك الجديدة، يمكنك إرفاقها بمجموعة `حدث`{:class="block3events"}. في قائمة `مجموعاتي`{:class="block3myblocks"}، تفترض رؤيتك للمجموعة التي صنعتها. استخدمه في البرنامج النصي التالي.

![كائن الكشّاف.](images/rover-sprite.png)

```blocks3
when this sprite clicked
عينة الفاكهة ::custom //شغّل الرسوم المتحركة
```

--- /task ---

--- task ---

اضغط على كائن **الكشاف**، و يفترض أن ترى الرسوم المتحركة.

--- /task ---

الآن تحتاج جعل الكشاف يجمع عينة حقا. في هذا المثال، الكشاف سيجمع فاكهة من شجرة.

--- task ---

كائن **الشجرة** يجب تعديله ليعطي مظهرين مختلفين. واحد مع فاكهة على(`شجرة بفاكهة`{:class="block3looks"})، و واحدة بدون فاكهة (`شجرة بلا فاكهة`{:class="block3looks"}). عدل أحد الأزياء، بحيث يكون لـ **الشجرة** مظهرين مختلفين.

--- /task ---

--- task ---

على كائن **الشجرة**، أضف مجموعة لتعيين مظهر **الشجرة** في بداية المشروع، و الزي يجب أن يتبدل عندما يستقبل عينة `عينة فاكهة`{:class="block3events"}.

![كائن الشجرة.](images/tree-sprite.png)

```blocks3
when I receive [إبدأ v]
go to x:(-90) y:(-80)
+ switch costume to (شجرة بالفاكهة v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [عينة الفاكهة v]
+ switch costume to (شجرة بدون فاكهة v)
```

--- /task ---

--- task ---

على كائن **الكشاف**، يمكنك استعمال `البث`{:class="block3events"} الجديد لإطلاق تبدل المظهر. أضف هذ `البث`{:class="block3events"} الجديد إلى دالتك `عرف عينة فاكهة`{:class="block3myblocks"}.

![كائن الكشاف.](images/rover-sprite.png)

```blocks3
define عينة الفاكهة
switch costume to (خامل v)
wait (0.3) seconds
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (الذراع 2 v)
wait (0.3) seconds
+ broadcast (عينة الفاكهة v)
switch costume to (ذراع 1 v)
wait (0.3) seconds
switch costume to (خامل v)
```

--- /task ---

--- task ---

**اختبار:** للتحقق من عمل الكود الخاص بك، انقر فوق العلم، من ثم انقر على كائن **الكشاف**. يجب أن يمتد ذراعه، كائن **الشجرة** يفترض تغيير مظهره.

**نصيحة:** بدل إلى وضع شاشة كاملة و ستصبح رؤية الرسوم المتحركة أسهل.

--- /task ---

ينبغي أن يكون الكشاف قادراً على جمع الثمار فقط إذا لمسها.

--- task ---

على كائن **الكشاف**، غير مجموعة المجموعات `عند النقر على هذا الكائن`{:class="block3events"}، بحيث الدالة `عينة فاكهة`{:class="block3myblocks"} تستدعى فقط إذا كان كائن **الكشاف** يلامس لون فاكهتك.

**نصيحة:** تغير مظهر من الإختبار قد يعني أن فاكهتك شفافة. فقط انقر على تبويب المظهر لكائن **الشجرة** و بدل للمظهر مع الفواكه الشفافة.

![كائن الكشاف.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //لون الفاكهة
عينة الفاكهة ::custom
```

--- /task ---

--- task ---

الآن بما أن كائن **الشجرة** يتغير عند تعيين فاكهة، تحتاج إعادة تعيين الكائن لمظهره الأول عندما يخرج من الشاشة.

![كائن الشجرة.](images/tree-sprite.png)

```blocks3
when I receive [إبدأ v]
go to x:(-90) y:(-80)
switch costume to (شجرة بالفاكهة v)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (شجرة بالفاكهة v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (شجرة بالفاكهة v)
end
end
```

--- /task ---

--- task ---

**اختبار:** حرك كائن **الكشاف** بحيث يكون يلمس الفاكهة، ثم انقر على كائن **الكشاف** و شاهده يجمع الفواكه من الشجرة.

--- /task ---


--- save ---
