--- question ---

---
legend: Question 2 of 3
---

ರೋವರ್‌ ಪರ್ವತದ ದೃಶ್ಯವನ್ನು ಅನ್ವೇಷಣೆ ಮಾಡುವುದನ್ನು ತೋರಿಸುವ ಈ ಪ್ರಾಜೆಕ್ಟ ಒಮ್ಮೆ ನೋಡಿ.

![ಹಿನ್ನಲೆಯಲ್ಲಿ ಪರ್ವತ ಚಲಿಸುತ್ತಿರುವುದು ಮತ್ತು ಸ್ಥಿರ ಮೋಡದೊಂದಿಗೆ ರೋವರ್‌ನ್ನು ತೋರಿಸುವ ಅನಿಮೇಷನ್](images/mountain-animation.gif)

ಪರ್ವತವನ್ನು ಚಲಿಸಲು ಕೋಡ್ ಇಲ್ಲಿದೆ.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

ಯಾವ ಕೋಡ್‌ ಬ್ಲಾಕ್‌ಗಳು ಮೋಡಗಳು ಪರ್ವತಗಳಿಗಿಂತ ನಿಧಾನವಾಗಿ ಚಲಿಸುವಂತೆ ಮಾಡುತ್ತವೆ?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---

ಇಲ್ಲಿ ಮೋಡವು ಪರ್ವತಕ್ಕಿಂತ ನಿಧಾನವಾಗಿ ಚಲಿಸುತ್ತಿದೆ, ಆದರೆ ಈ ಕೋಡ್‌ ರೋವರ್‌ಗೆ ತಲುಪಲು ಮೋಡವನ್ನು ಕಷ್ಟವಾಗಿಸುತ್ತೆ ಏಕೆಂದರೆ ಅದು ರೋವರ್‌ ಚಲಿಸುವ ದಿಕ್ಕಿನಲ್ಲಿಯೇ ಚಲಿಸುತ್ತಿರುತ್ತದೆ.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  ಈ ಕೋಡ್‌ನಿಂದ, ಮೋಡವು ಎಡ ಮತ್ತು ಬಲಕ್ಕೆ ಚಲಿಸುವ ಬದಲು ಮೇಲೆ ಮತ್ತು ಕೆಳಗೆ ಚಲಿಸುತ್ತದೆ. ಮೋಡವು ಎಡ ಮತ್ತು ಬಲಕ್ಕೆ ಚಲಿಸುವಂತೆ ನೀವು ಹೇಗೆ ಮಾಡಬಹುದು? ಸ್ಟೇಜ್‌ನ್ನು ನಿರ್ದೇಶಾಂಕದ ಗ್ರಿಡ್‌ ಎಂದು ಯೋಚಿಸಿ.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  ಇಲ್ಲಿ ಮೋಡವು ಸರಿಯಾದ ದಿಕ್ಕಿನಲ್ಲಿ ಚಲಿಸುತ್ತಿದೆ, ಅದು ರೋವರ್‌ನಿಂದ ಪರ್ವತಕ್ಕಿಂತ ಬಹಳ ದೂರದಲ್ಲಿದೆಯಾದರೂ, ಅದು ಪರ್ತವಕ್ಕಿಂತ ತುಂಬಾ ವೇಗದಲ್ಲಿ ಚಲಿಸುತ್ತಿದೆ.

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

ಅತ್ಯುತ್ತಮ! ರೋವರ್‌ ಎಡಕ್ಕೆ ಚಲಿಸಿದಾಗ ಮೋಡವು ಬಲಕ್ಕೆ, ಮತ್ತು ರೋವರ್‌ ಬಲಕ್ಕೆ ಚಲಿಸದಿದಾಗ ಎಡಕ್ಕೆ ಚಲಿಸುತ್ತದೆ.  ಮೋಡವು ಪರ್ವತಕ್ಕಿಂತ ನಿಧಾನವಾಗಿ ಚಲಿಸುತ್ತದೆ ಏಕೆಂದರೆ x ನ್ನು 5 ರ ಏರಿಕೆಗಳಿಗೆ ಬದಲಾಯಿಸಲಾಗಿದೆ.

  --- /feedback ---

--- /choices ---

--- /question ---
