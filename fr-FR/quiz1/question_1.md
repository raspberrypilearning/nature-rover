## Questionnaire rapide

Réponds aux trois questions. Il y a des indices pour te guider vers la bonne réponse.

Lorsque tu as répondu à chaque question, clique sur **Vérifier ma réponse**.

Amuse-toi bien !


--- question ---

---
legend: Question 1 sur 3
---

Voici un contrôleur qui diffuse vers le haut lorsque le bouton haut est cliqué et vers le bas lorsque le bouton bas est cliqué :

![contrôleur à quatre boutons](images/controller.png)

Lequel des blocs de code suivants ajouterais-tu au **sprite du rover** pour le faire monter et descendre

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

  Cela déplacerait le rover quand il touche les boutons, plutôt que lorsque les boutons sont enfoncés.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  Cela déplacerait le rover quand il a été cliqué, plutôt que lorsque les boutons sont cliqués.

  --- /feedback ---

- (x)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)

```

  --- feedback ---

  Oui, ce script reçoit les diffusions de haut et de bas des boutons du contrôleur et fait monter et descendre le rover.

  --- /feedback ---

- ( )

```blocks3
define up
change y by (10)

define down
change y by (-10)

```


  --- feedback ---

  Cela crée des fonctions pour monter et descendre, mais comme les fonctions ne sont pas appelées, le rover ne bouge pas.

  --- /feedback ---

--- /choices ---

--- /question ---
