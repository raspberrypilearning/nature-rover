## Snelle quiz

Beantwoord de drie vragen. Er zijn tips om je naar het juiste antwoord te leiden.

Wanneer je elke vraag hebt beantwoord, klik je op **Verzenden**.

Veel plezier!


--- question ---

---
legend: Vraag 1 van 3
---

Hier is een controller die omhoog uitzendt wanneer op de omhoog-knop wordt geklikt en omlaag wanneer op de omlaag-knop wordt geklikt:

![controller met vier knoppen](images/controller.png)

Welke van de volgende codeblokken zou je toevoegen aan **de rover sprite** om hem omhoog en omlaag te laten bewegen

--- choices ---

- ( )

```blocks3
when flag clicked
forever
if <touching [up button v]> then
change y by (10)
end
if <touching [down button v]> then
change y by (-10)

```


  --- feedback ---

  Dit zou de rover verplaatsen wanneer de knoppen worden aangeraakt, in plaats van wanneer er op de knoppen wordt gedrukt.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  Dit zou de rover bewegen wanneer er op de rover sprite wordt geklikt, in plaats van wanneer op de knoppen wordt geklikt.

  --- /feedback ---

- (x)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)

```

  --- feedback ---

  Ja, dit script ontvangt de omhoog en omlaagsignalen van de controllerknoppen en laat de rover omhoog en omlaag bewegen.

  --- /feedback ---

- ( )

```blocks3
define up
change y by (10)

define down
change y by (-10)

```


  --- feedback ---

  Dit creëert functies om omhoog en omlaag te bewegen, maar omdat de functies niet worden aangeroepen, zal de rover niet bewegen.

  --- /feedback ---

--- /choices ---

--- /question ---
