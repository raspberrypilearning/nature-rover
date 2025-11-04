## Teste rápido

Responda às três perguntas. Existem dicas para guiá-lo para a resposta correta.

Quando você tiver respondido a cada pergunta, clique em **Verificar minha resposta**.

Divirta-se!


--- question ---

---
legend: Pergunta 1 de 3
---

Aqui está um controle que transmite para cima quando o botão para cima é clicado, e para baixo quando o botão para baixo é clicado:

![controlador de quatro botões](images/controller.png)

Qual dos seguintes blocos de código você adicionaria ao **ator do rover** para fazê-lo mover-se para cima e para baixo

--- choices ---

- ( )

```blocks3
when flag clicked
forever
if <touching [seta para cima v]> then
change y by (10)
end
if <touching [seta para baixo v]> then
change y by (-10)

```


  --- feedback ---

  Isto moveria o rover quando está tocando os botões, ao invés de quando os botões são pressionados.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
change y by (10)
```

--- feedback ---

  Isso moveria o rover quando ele fosse clicado, e não quando os botões fossem clicados.

  --- /feedback ---

- (x)

```blocks3
when I receive [para cima v]
change y by (10)

when I receive [para baixo v]
change y by (-10)

```

  --- feedback ---

  Sim, este script recebe as transmissões para cima e para baixo dos botões de controle e faz com que o rover vá para cima e para baixo.

  --- /feedback ---

- ( )

```blocks3
define para cima
change y by (10)

define para baixo
change y by (-10)

```


  --- feedback ---

  Isso cria funções para mover para cima e para baixo, mas como as funções não são chamadas, o rover não se moveria.

  --- /feedback ---

--- /choices ---

--- /question ---
