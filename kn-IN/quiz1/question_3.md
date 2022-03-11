
--- question ---

---
legend: ಪ್ರಶ್ನೆ 3 ರಲ್ಲಿ 3
---

ಈ ಬರಹವು ಬೆಕ್ಕನ್ನು ನೃತ್ಯ ಮಾಡಿಸಲು ಉಪಯೋಗಿಸುವ ಫಂಕ್ಷನ್:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

ಸ್ಪ್ರೈಟ್‌ನ್ನು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಬೆಕ್ಕು ನೃತ್ಯ ಮಾಡುವಂತೆ ಮಾಡಲು ಈ ಕೆಳಗಿನ ಯಾವ ಬ್ಲಾಕ್‌ಗಳನ್ನು `cat animation`{:class='block3myblocks'} ಉಪಯೋಗಿಸುತ್ತವೆ?

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

  ಇದು ಬೆಕ್ಕು ನೃತ್ಯ ಮಾಡುವಂತೆ ಮಾಡುತ್ತದೆ, ಆದರೆ ಅದನ್ನು ಮಾಡಿದ `cat animation`{:class='block3myblocks'} ನ್ನು ಉಪಯೋಗಿಸುವುದಿಲ್ಲ.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  ಇದು `cat dance`{:class='block3myblocks'} ಬ್ಲಾಕ್‌ ಆಮಂತ್ರಿಸುವುದು, ಆದರೆ ಬೆಕ್ಕಿನ `cat animation`{:class='block3myblocks'} ಬ್ಲಾಕ್‌ ಅಲ್ಲ.

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

  ಇದು ಬೆಕ್ಕು ನೃತ್ಯ ಮಾಡುವಂತೆ ಮಾಡುತ್ತದೆ, ಆದರೆ ಸ್ಪ್ರೈಟ್‌ ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಅಲ್ಲ. ಇದು `cat animation`{:class='block3myblocks'} ಬ್ಲಾಕ್‌ನ್ನೂ ಸಹ ಉಪಯೋಗಿಸುವುದಿಲ್ಲ.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

ಹೌದು, ಈ ಉತ್ತರದಲ್ಲಿ, `cat animation`{:class='block3myblocks'} ಬ್ಲಾಕ್‌ನ್ನು ಸ್ಪ್ರೈಟ್‌ ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಉಪಯೋಗಿಸಲಾಗಿದೆ, ಅದು ಬೆಕ್ಕು ನೃತ್ಯ ಮಾಡುವಂತೆ ಮಾಡುತ್ತದೆ.

  --- /feedback ---

--- /choices ---

--- /question ---
