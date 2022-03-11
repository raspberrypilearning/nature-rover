
--- question ---

---
legend: 3 में से तीसरा प्रश्न
---

यह स्क्रिप्ट एक फलन है जिसका उपयोग बिल्ली को नृत्य करने के लिए किया जाता है:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

निम्नलिखित में से कौन सी स्क्रिप्ट ऊपर दी गयी`cat animation`{:class='block3myblocks'} का उपयोग बिल्ली को स्प्राइट क्लिक करने पर नृत्य करने के लिए करेगी?

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

  यह बिल्ली को नृत्य करा देगा, लेकिन `cat animation`{:class='block3myblocks'} का उपयोग नहीं करता है जिसे बनाया गया है।

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  इसे `cat dance`{:class='block3myblocks'} ब्लॉक बुलाना कहा जाता है ना की `cat animation`{:class='block3myblocks'} ब्लॉक

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

  यह बिल्ली को नृत्य करा देगा, लेकिन तब नहीं जब स्प्राइट क्लिक किया जाता है। यह `cat animation`{:class='block3myblocks'} ब्लॉक का भी उपयोग नहीं करता है।

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

हाँ, इस उत्तर में, `cat animation`{:class='block3myblocks'} ब्लॉक का उपयोग तब किया जाता है जब स्प्राइट पर क्लिक किया जाता है, जिससे बिल्ली नृत्य करती है।

  --- /feedback ---

--- /choices ---

--- /question ---
