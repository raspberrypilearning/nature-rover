--- question ---

---
legend: Question 2 sur 3
---

Jette un coup d'oeil à ce projet montrant un rover explorant une scène de montagne.

![animation montrant un rover avec une montagne en mouvement en arrière-plan et un nuage statique](images/mountain-animation.gif)

Voici le code pour déplacer la montagne.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

Quels blocs de code feraient défiler le nuage plus lentement que la montagne ?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---

Le nuage défile plus lentement que la montagne ici, mais ce code rend le nuage difficile à atteindre pour le rover car il se déplace dans la même direction que le rover.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  Avec ce code, le nuage se déplacera vers le haut et vers le bas au lieu de gauche et de droite. Comment peux-tu faire bouger le nuage à gauche et à droite ? Pense à la scène comme une grille de coordonnées.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  Le nuage défile dans la bonne direction ici, mais il défile beaucoup plus vite que la montagne, même s'il est plus éloigné du rover que la montagne.

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

Super ! le nuage se déplace vers la droite lorsque le rover se déplace vers la gauche, et vers la gauche lorsque le rover se déplace vers la droite.  Le nuage défile plus lentement que la montagne car x est modifié par incréments de 5.

  --- /feedback ---

--- /choices ---

--- /question ---
