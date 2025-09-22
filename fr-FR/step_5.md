## Recueillir un échantillon

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Dans cette étape, tu vas modifier l'apparence d'un sprite et du rover pour montrer que le rover collecte des échantillons.
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

Regarde les costumes du sprite **rover**. Il y a six animations disponibles. Le **rover** peut :
- Étendre son bras

![Trois costumes montrant le bras du rover en extension.](images/arm-animation.png)

- Forer le sol
- Aspirer l'air
- Étendre un panneau solaire
- Prendre une photo
- Ramasser quelque chose

--- /task ---

Quand tu veux organiser beaucoup de code dans Scratch, comme plusieurs changements de costumes, il est utile d'utiliser `Mes Blocs`{:class="block3myblocks"}. Cela te permet de créer tes propres blocs personnalisés.

Ton sprite **rover** aura un `Mon Bloc`{:class="block3myblocks"} pour chaque animation.

--- task ---

Dans le menu `Mes Blocs`{:class="block3myblocks"}, clique sur **Créer un bloc**, et nomme ton nouveau bloc `échantillon de fruits`{:class="block3myblocks"}.

--- /task ---

Un nouveau bloc devrait apparaître dans ton script. Ça ressemblera à ça :

![Le sprite rover.](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

Sous ce bloc, attache quelques blocs `basculer sur le costume`{:class="block3looks"} et `attendre`{:class="block3control"}, pour animer le robot.

**Astuce :** Il est plus rapide de créer ton premier bloc `basculer sur le costume`{:class='block3looks'} et `attendre`{:class='block3control'}, puis duplique-les et change le costume utilisé.

![Le sprite rover.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

Add a block so that the **rover** sprite plays a sound when it collects the fruit sample. You can find the **Collect** sound in the Sound gallery.

![Le sprite rover.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ start sound (Collect v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---


--- task ---

Tu peux cliquer sur le bloc `définir échantillon de fruits`{:class="block3myblocks"} pour voir l'animation. Si tu es sur un petit écran, tu devras peut-être regarder attentivement.

L'animation ne s'exécutera pas quand tu cliques sur le drapeau vert, comme tu n'as pas encore utilisé ton nouveau `bloc échantillon de fruits`{:class='block3myblocks'} dans ton projet.

--- /task ---

--- task ---

Pour utiliser ton nouveau bloc, tu peux l'attacher à un bloc `événement`{:class="block3events"}. Dans le menu `Mes Blocs`{:class="block3myblocks"}, tu devrais voir le bloc que tu as créé. Utilise-le dans le script suivant.

![Le sprite rover.](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

Clique sur le sprite **rover** et tu devrais voir l'animation.

--- /task ---

Maintenant tu dois faire en sorte que le rover collecte un échantillon. Dans cet exemple, le rover ramassera un fruit d'un arbre.

--- task ---

The **tree** sprite needs two costumes, one without fruit on (`tree without fruit`{:class="block3looks"}), and one with fruit (`tree with fruit`{:class="block3looks"}). Add another costume to the **tree**, change the names and draw some fruit on the **with fruit** one.

![The 'tree with fruit' costume, with 5 light red circles on it to represent fruit](images/tree-with-fruit.png)

--- /task ---

--- task ---

On the **tree** sprite, add blocks to set the costume of the **tree** at the start of the project, and the costume it should switch to when it receives a `sample fruit`{:class="block3events"} broadcast.

![The tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [sample fruit v]
+ switch costume to (tree without fruit v)
```

--- /task ---

--- task ---

On the **rover** sprite, you can use the new `broadcast`{:class="block3events"} to trigger the costume change. Add this new `broadcast`{:class="block3events"} into your `define sample fruit`{:class="block3myblocks"} function.

![The rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
start sound (Collect v)
+ broadcast (sample fruit v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

**Test:** To check that your code is working, click on the flag, and then click on your **rover** sprite. Its arm should extend, and the **tree** sprite should change costumes.

**Tip:** Switch to full screen mode and you will be able to see the animation more easily.

--- /task ---

The rover should only be able to collect the fruit, if it is touching it.

--- task ---

On the **rover** sprite, change the `when this sprite clicked`{:class="block3events"} set of blocks, so that the `sample fruit`{:class="block3myblocks"} function is only called if the **rover** sprite is touching the colour of your fruit.

**Tip:** Your costume change from testing might mean that the fruit is not visible. Just click on the costumes tab for the **tree** sprite, and switch to the costume with the visible fruit.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

Now that the **tree** sprite changes when a fruit is sampled, you need to reset the sprite to its first costume when it goes off the screen.

![The tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (tree with fruit v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (tree with fruit v)
end
end
```

--- /task ---

--- task ---

**Test:** Move the **rover** sprite so that it is touching the fruit, then click on the **rover** sprite and watch it collect the fruit from the tree.

--- /task ---


--- save ---
