
--- question ---

---
legend: प्रश्न 3 पैकी 3
---

हा स्क्रिप्ट एक फंक्शन आहे जीचा कॅटला डान्स करण्यासाठी वापर केला जातो:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

खालीलपैकी कोणत्या स्क्रिप्टचा `cat animation`{:class='block3myblocks'} च्या वर Sprite क्लिक केल्यावर कॅटला डान्स करण्यासाठी वापर केला जाईल?

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

  This would make the cat dance, but does not use the `cat animation`{:class='block3myblocks'} block that has been made.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  याला `cat dance`{:class='block3myblocks'} ब्लॉक म्हटले जाते, परंतु कॅट `cat animation`{:class='block3myblocks'} ब्लॉक नाही.

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

  यामुळे कॅट डान्स करेल, परंतु स्प्राईटवर क्लिक केल्यावर नाही. तो `cat animation`{:class='block3myblocks'} ब्लॉक वापरत नाही.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

हो, या उत्तरामध्ये, `cat animation`{:class='block3myblocks'} ब्लॉकचा स्प्राईट क्लिक केल्यावर वापर केला जातो, ज्यामुळे कॅट डान्स करते.

  --- /feedback ---

--- /choices ---

--- /question ---
