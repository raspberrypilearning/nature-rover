
--- question ---

---
legend: Question 3 sur 3
---

Ce script est une fonction utilisée pour faire danser un chat :

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Lequel des scripts suivants utiliserait `l'animation de chat`{:class='block3myblocks'} ci-dessus pour faire danser le chat lorsque l'on clique sur le Sprite ?

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

  Cela ferait danser le chat, mais n'utiliserait pas l'`animation de chat`{:class='block3myblocks'} qui a été faite.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  Ceci appelle un bloc `danse du chat`{:class='block3myblocks'}, mais pas le bloc `animation de chat`{:class='block3myblocks'}.

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

  Cela ferait danser le chat, mais pas lorsque le sprite est cliqué. Il n'utilise pas non plus le bloc `animation de chat`{:class='block3myblocks'}.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Oui, dans cette réponse, le bloc `animation de chat`{:class='block3myblocks'} est utilisé lorsque le sprite est cliqué, provoquant la danse du chat.

  --- /feedback ---

--- /choices ---

--- /question ---
