## Criar outra amostra

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Escolha o que o rover coletará em seguida! Ele vê uma nova espécie de planta, inseto ou animal? Ele vê alguma água ou líquido misterioso? Ele quer coletar um pouco de terra, uma pedra ou até mesmo o ar? Ou alguma outra coisa?
</div>
<div>
![](images/step-6.gif){:width="300px"}
</div>
</div>

--- task ---

**Escolha:** Adicione um novo ator **amostra** para o rover coletar. Você pode adicioná-lo ao seu projeto selecionando um da biblioteca ou desenhando o seu próprio.

--- /task ---

Faça com que seu ator **amostra** se mova. Se estiver na parte inferior da tela, ele deve se mover mais (`alterar x em`{:class='block3motion'} deve ser maior que `5`), e se estiver na parte superior da tela, ele deve se mover menos (`alterar x em`{:class='block3motion'} deve ser menor que `5`).

--- task ---

Adicione código para que seu ator se mova.

--- /task ---

**Escolha:** Dependendo do que você quer que o rover colha em seguida, você pode usar as animações do rover que já estão lá ou criar mais sequências de animação duplicando e editando as fantasias.

--- task ---

Adicione um bloco `Meus Blocos`{:class='block3myblocks'} ao seu ator **rover** para animar o rover quando ele coletar a nova amostra. Você pode copiar e colar o código de um dos outros `Meus Blocos`{:class='block3myblocks'} que você criou.

Por exemplo, aqui está uma sequência de fantasia para coletar energia solar:

![Três fantasias mostrando o rover estendendo um painel solar.](images/solar-animation.png)

Para animar esta série de fantasias você pode usar o seguinte código:

```blocks3
define recharge
switch costume to [inativo v]
wait (0.3) seconds
switch costume to [solar 1 v]
wait (0.3) seconds
switch costume to [solar 2 v]
wait (0.3) seconds
switch costume to [solar 3 v]
wait (0.3) seconds
switch costume to [solar 2 v]
wait (0.3) seconds
switch costume to [solar 1 v]
wait (0.3) seconds
switch costume to [inativo v]
wait (0.3) seconds
```

--- /task ---

--- task ---

Em seguida, `transmita`{:class='block3events'} uma nova mensagem no seu novo bloco `Meu Bloco`{:class='block3myblocks'} que causará uma mudança de `fantasia`{:class='block3looks'} ou `efeito gráfico`{:class='block3looks'} no ator **amostra**.

--- /task ---

--- task ---

Use um bloco `se`{:class='block3control'} para detectar se o rover está tocando o ator ou tocando uma cor no ator, para que então somente o novo `Meu Bloco`{:class='block3myblocks'} seja usado.

--- /task ---

--- task ---

Se desejar, adicione uma animação ao ator para que sua aparência mude quando o rover tiver coletado a amostra.

--- /task ---

--- save ---
