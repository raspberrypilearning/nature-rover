
--- question ---

---
legend: Vraag 3 van 3
---

Dit script is een functie die wordt gebruikt om een kat te laten dansen:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Welke van de volgende scripts zouden de `kat animatie`{:class='block3myblocks'} hierboven gebruiken om de kat te laten dansen wanneer op de Sprite wordt geklikt?

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

  Dit zou de kat laten dansen, maar er wordt geen `kat animatie`{:class='block3myblocks'} gebruikt, die hiervoor werd gemaakt.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  Dit roept een `kat dans`{:class='block3myblocks'} blok op, maar niet het kat `kat animatie`{:class='block3myblocks'} blok.

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

  Hierdoor zou de kat dansen, maar niet wanneer op de sprite wordt geklikt. Het gebruikt ook geen `kat-animatie`{:class='block3myblocks'} blok.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Ja, in dit antwoord wordt het `kat animatie`{:class='block3myblocks'} blok gebruikt wanneer op de sprite wordt geklikt, waardoor de kat gaat dansen.

  --- /feedback ---

--- /choices ---

--- /question ---
