--- question ---

---
legenda: Pergunta 2 de 3
---

Dê uma olhada neste projeto mostrando um robô explorando um cenário de montanha.

![animação mostrando o rover com uma montanha se movendo ao fundo e uma nuvem estática](images/mountain-animation.gif)

Aqui está o código para mover a montanha.

```blocks3
when I receive [left v]
change x by (10)

when I receive [right v]
change x by (-10)
```

Quais blocos de código fariam a nuvem a se mover mais devagar que a montanha?

--- choices ---

- ( )

```blocks3
when I receive [left v]
change x by (-5)

when I receive [right v]
change x by (5)
```

  --- feedback ---

A nuvem está se movendo mais devagar que a montanha aqui, mas este código torna a nuvem difícil de ser alcançada pelo rover porque ela se move na mesma direção que ele.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change y by (5)

when I receive [right v]
change y by (5)

```

  --- feedback ---

  Com este código, a nuvem se moverá para cima e para baixo em vez de para a esquerda e para a direita. Como você pode fazer a nuvem se mover para a esquerda e para a direita? Pense no palco como uma grade coordenada.

  --- /feedback ---

- ( )

```blocks3
when I receive [left v]
change x by (20)

when I receive [right v]
change y by (-20)
```

  --- feedback ---

  A nuvem está se movendo na direção certa aqui, porém ela está se movendo muito mais rápido que a montanha, mesmo estando mais distante do rover do que da montanha.

  --- /feedback ---

- (x)

```blocks3
when I receive [left v]
change x by (5)

when I receive [right v]
change x by (-5)
```

  --- feedback ---

Ótimo! a nuvem se move para a direita quando o rover se move para a esquerda e para a esquerda quando o rover se move para a direita.  A nuvem se move mais lentamente do que a montanha porque x é alterado em incrementos de 5.

  --- /feedback ---

--- /choices ---

--- /question ---
