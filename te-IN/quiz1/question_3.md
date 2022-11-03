
--- question ---

---
legend: 3లో 3వ ప్రశ్న
---

ఈ స్క్రిప్ట్ పిల్లిని నృత్యం చేయించడానికి ఉపయోగించే ఒక ఫంక్షన్:

```blocks3
define cat animation
switch costume to [costume 1 v]
wait (0.1) seconds
switch costume to [costume 2 v]
wait (0.1) seconds
```

Spriteని క్లిక్ చేసినప్పుడు పిల్లి నృత్యం చేయడానికి `cat animation`{:class='block3myblocks'} స్క్రిప్ట్‌లలో ఏది ఉపయోగించ బడుతుంది?

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

  This would make the cat dance, but does not use the `cat animation`{:class='block3myblocks'} block that has been made.

  --- /feedback ---

- ( )

```blocks3
when this sprite clicked
cat dance ::custom
```

  --- feedback ---

  ఇది `cat dance`{:class='block3myblocks'} బ్లాక్ అని పిలువబడుతుంది, కానీ `cat animation`{:class='block3myblocks'} బ్లాక్ కాదు.

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

  ఇది పిల్లిని నృత్యం చేయిస్తుంది, కానీ sprite క్లిక్ చేసినప్పుడు కాదు. ఇది `cat animation`{:class='block3myblocks'} బ్లాక్‌ని కూడా ఉపయోగించదు.

  --- /feedback ---

- (x)

```blocks3
when this sprite clicked
cat animation ::custom
```

  --- feedback ---

అవును, ఈ సమాధానంలో, `cat animation`{:class='block3myblocks'} బ్లాక్ ఉపయోగించబడుతుంది, దీని వలన పిల్లి నృత్యం చేస్తుంది.

  --- /feedback ---

--- /choices ---

--- /question ---
