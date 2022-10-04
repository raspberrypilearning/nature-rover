## Faire défiler plus de sprites

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Lorsque tu ajoutes plus de sprites à ta scène, ceux-ci doivent également défiler à gauche et à droite.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

Tu peux maintenant ajouter d'autres objets à ta scène, et les faire défiler de la même manière.

--- task ---

Ajoute un sprite **arbre** à ton projet, puis définis sa position de départ.

![Le sprite arbre.](images/tree-sprite.png)
```blocks3
when I receive [départ v]
go to x:(0) y:(-80)
```

--- /task ---

Le sprite **arbre** devrait également se déplacer dans la direction **opposée** à la diffusion également.

![Animation d'un arbre se déplaçant à droite et à gauche, montrant le changement de coordonnées x.](images/scrolling-tree.gif)

Comme l'arbre est plus proche du spectateur, il devrait sembler se déplacer sur une plus grande distance que les collines chaque fois que le bouton ou la touche est enfoncé.

--- task ---

Pour obtenir cet effet de déplacement, modifie les valeurs `x`{:class='block3motion'} par lesquelles le sprite **arbre** se déplace lorsque les diffusions `à gauche`{:class="block3events"} et `à droite`{:class="block3events"} sont reçues.

![Le sprite arbre.](images/tree-sprite.png)

```blocks3
when I receive [à gauche v]
change x by (10) //Utiliser un plus grand nombre que pour les collines

when I receive [à droite v]
change x by (-10) //Utiliser un plus grand nombre que pour les collines
```

--- /task ---

--- task ---

**Test :** Vérifie maintenant tes boutons gauche et droite. L'arbre doit se déplacer à chaque fois que tu cliques sur le contrôleur.

**Test :** Que se passe-t-il si tu t'éloignes le plus possible de l'arbre ?

--- /task ---

As-tu remarqué que lorsque l'arbre atteint le bord de l'écran, il arrête de bouger ? Tu peux corriger cela en déplaçant l'arbre de l'autre côté de l'écran, quand sa coordonnée `x`{:class='block3motion'} est trop élevée ou trop faible.

--- task ---

Utilise une boucle `répéter indéfiniment`{:class='block3control'}, et des blocs `si`{:class='block3control'}, vérifie les coordonnées `x`{:class='block3motion'} de l'arbre, et déplace-le vers l'autre côté de l'écran lorsque `x`{:class='block3motion'} est supérieur à `290` ou inférieur à `-290`.

![Le sprite arbre.](images/tree-sprite.png)

```blocks3
when I receive [départ v]
go to x:(-90) y:(-80)
+ forever
if <(x position) > (290)> then //L'arbre est à l'extrême droite
set x to (-280) //Déplacer l'arbre vers l'extrême gauche
end
if <(x position) < (-290)> then //L'arbre est à l'extrême gauche
set x to (280) //Déplacer l'arbre à l'extrême droite
end
end
```

--- /task ---

--- task ---

Maintenant, déplace ton sprite **rover** sur l'écran. Lorsque l'arbre atteint le bord, il devrait disparaître du bord de l'écran et réapparaître de l'autre côté.

--- /task ---

--- task ---

Enfin, fais tourner le **rover** à gauche et à droite pour qu'il fasse face à la direction dans laquelle il se déplace.

![Le sprite rover.](images/rover-sprite.png)

```blocks3
when flag clicked
broadcast [départ v]
+ set rotation style [left-right v]

when I receive [à gauche v]
point in direction (-90)

when I receive [à droite v]
point in direction (90)
```

--- /task ---

--- task ---

**Test** : Exécute ton projet et teste-le. Assure-toi que l'arbre semble tomber du bord de l'écran et apparaît de l'autre côté lorsque le rover se déplace.

--- /task ---
