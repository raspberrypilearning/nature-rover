## تمرير المزيد من الكائنات

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
عند إضافة المزيد من الكائنات لمشهدك، تحتاج هذه إلى التمرير إلى اليسار واليمين أيضًا.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

يمكنك الآن إضافة المزيد من الأشياء لمشهدك، وتمريرها بطريقة مماثلة.

--- task ---

أضف كائن **شجرة** إلى مشروعك، ثم اضبط موضع البداية.

![كائن الشجرة.](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(0) y:(-80)
```

--- /task ---

كائن **الشجرة** يجب أيضا أن يتحرك إلى الجانب **المقابل** للبث كذلك.

![تحريك الشجرة المتحركة لليمين واليسار، يظهر تغير في الإحداثيات x.](images/scrolling-tree.gif)

بما أن الشجرة أقرب إلى المشاهد، يجب أن تبدو تتحرك مسافة أكبر من التلال كل مرة يُضغط الزر أو المفتاح.

--- task ---

لتحصل على هذا المؤثر الحركي’ غيّر قيمة الـ`<code>x`{:class='block3motion'} التي تحرك كائن **الشجرة** عندما يُبث أو يُستقبل `اليسار`{:class="block3events"}و <0>اليمين</code>{:class="block3events"}.

![كائن الشجرة.](images/tree-sprite.png)

```blocks3
when I receive [left v]
change x by (10) //Use a bigger number than for the hills

when I receive [right v]
change x by (-10) //Use a bigger number than for the hills
```

--- /task ---

--- task ---

**Test:** Click the green flag and check your left and right buttons now. الشجرة يجب أن تتحرك كلما ضغطت على المتحكم.

**اختبار:** ماذا يحدث إذا ابتعدت عن الشجرة قدرما أمكن؟

--- /task ---

هل لاحظت أن الشجرة عندما تصل إلى أقصى حافة الشاشة، تتوقف عن الحركة؟ يمكنك إصلاح هذا بتحريك الشجرة إلى الجانب الآخر من الشاشة، عندما تكون الإحداثية `×`{: class = 'block3motion'} جد مرتفعة أو جد منخفضة.

--- task ---

مستخدما حلقة `دائما`{:class='block3control'}, و مجموعة `إذا`{:class='block3control'}, تحقق إحداثية الشجرة `x`{:class='block3motion'}, و حركها إلى الجانب الآخر من الشاشة عندما يكون `x`{:class='block3motion'} أكبر من `290` أو أصغر من `-290`.

![كائن الشجرة.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ forever
if <(x position) > (290)> then //The tree is at the far right
set x to (-280) //Move the tree to the far left
end
if <(x position) < (-290)> then //The tree is at the far left
set x to (280) //Move the tree to the far right
end
end
```

--- /task ---

--- task ---

الآن حرك كائن **كشافك** في أرجاء الشاشة. عندما تصل الشجرة إلى الحافة، يجب أن تتلاشى من حافة الشاشة وتعاود الظهور على الجانب الآخر.

--- /task ---

--- task ---

Lastly, make the **rover** turn left and right so that it faces the direction it is moving in, and resets at the start.

![كائن الكشّاف.](images/rover-sprite.png)

```blocks3
when flag clicked
go to [front v] layer
broadcast [start v]
+ set rotation style [left-right v]

when I receive [left v]
point in direction (-90)

when I receive [right v]
point in direction (90)

when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
go to [front v] layer
+ point in direction (90)
```

--- /task ---

--- task ---

**اختبار:**شغل مشروعك و اختبره. تأكد من ظهور الشجرة تسقط من حافة الشاشة و تظهر على الجانب الآخر عندما يتحرك الكشاف.

--- /task ---
