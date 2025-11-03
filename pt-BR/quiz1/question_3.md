
--- question ---

---
legend: Pergunta 3 de 3
---

Este script é uma função usada para fazer um gato dançar:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Qual dos seguintes scripts usariam a animação `gato`{:class='block3myblocks'} acima para fazer o gato dançar quando o Ator fosse clicado?

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

  Este faria o gato dançar, mas não usa o bloco `animação de gato`{:class='block3myblocks'} que foi criado.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  Este está chamando um bloco `dança de gato`{:class='block3myblocks'}, mas não o bloco de gato `animação de gato`{:class='block3myblocks'}.

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

  Este faria o gato dançar, mas não quando o ator fosse clicado. Também não usa o bloco `animação de gato`{:class='block3myblocks'}.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

Sim, nesta resposta, o bloco `animação de gato`{:class='block3myblocks'} é usado quando o ator é clicado, fazendo o gato dançar.

  --- /feedback ---

--- /choices ---

--- /question ---
