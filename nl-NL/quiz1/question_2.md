--- question ---

---
legend: Vraag 2 van 3
---

Bekijk dit project om een rover te tonen die een berglandschap verkent.

![animatie die de rover toont met de berg op de achtergrond en een statische wolk](images/mountain-animation.gif)

Hier is de code voor het verplaatsen van de berg.

```blocks3
when I receive [omlaag v]
change x by (10)

when I receive [rechts v]
change x by (-10)
```

Welke codeblokken zouden de wolk langzamer laten bewegen dan de berg?

--- choices ---

- ( )

```blocks3
when I receive [omlaag v]
change x by (-5)

when I receive [rechts v]
change x by (5)
```

  --- feedback ---

De wolk beweegt langzamer dan de berg hier, maar deze code maakt het moeilijk voor de rover om de wolk te bereiken omdat deze in dezelfde richting beweegt als de rover.

  --- /feedback ---

- ( )

```blocks3
when I receive [omlaag v]
change y by (5)

when I receive [rechts v]
change y by (5)

```

  --- feedback ---

  Met deze code beweegt de wolk omhoog en omlaag in plaats van naar links en rechts. Hoe kun je de wolk naar links en rechts laten bewegen? Denk aan het podium als een coördinatenraster.

  --- /feedback ---

- ( )

```blocks3
when I receive [omlaag v]
change x by (20)

when I receive [rechts v]
change y by (-20)
```

  --- feedback ---

  De wolk beweegt hier in de juiste richting, maar beweegt veel sneller dan de berg, ook al is hij verder van de rover verwijderd dan de berg.

  --- /feedback ---

- (x)

```blocks3
when I receive [omlaag v]
change x by (5)

when I receive [rechts v]
change x by (-5)
```

  --- feedback ---

Geweldig! de wolk beweegt naar rechts wanneer de rover naar links beweegt, en naar links wanneer de rover naar rechts beweegt.  De wolk beweegt langzamer dan de berg omdat x wordt veranderd in stappen van 5.

  --- /feedback ---

--- /choices ---

--- /question ---
