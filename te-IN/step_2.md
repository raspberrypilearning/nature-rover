## రోవర్‌ను నియంత్రించండి

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ఈ దశలో, మీరు మీ రోవర్‌ని పైకి క్రిందికి తరలించడానికి ఆన్-స్క్రీన్ కంట్రోలర్ లేదా కీబోర్డ్‌ని ఉపయోగిస్తారు.
</div>
<div>
![](images/step-2.gif){:width="300px"}
</div>
</div>

--- task ---

ఆన్‌లైన్‌లో స్టార్టర్ ప్రాజెక్ట్‌ను [rpf.io/nature-rover-starter](https://rpf.io/nature-rover-starter){:target="_blank"}లో తెరవండి.

--- collapse ---
---
title: ఆఫ్‌లైన్‌లో పని చేస్తోంది
---

మీరు ఆఫ్‌లైన్‌లో పని చేస్తుంటే, స్టార్టర్ ప్రాజెక్ట్‌ను [rpf.io/p/en/nature-rover-go](https://rpf.io/p/en/nature-rover-go)లో కనుగొనవచ్చు

--- /collapse ---


--- /task ---

మీరు రోబోటిక్ రోవర్, కొండ ప్రాంతపు నేపథ్యం మరియు దిగువ ఎడమవైపు మూలలో కంట్రోలర్‌తో కూడిన దృశ్యాన్ని చూడాలి.

![కొండలు, మట్టి కుప్ప మరియు రోబోట్‌ని చూపిస్తూ చూపిస్తున్న నేపథ్యం.](images/starter-background.png)

రోవర్ వీక్షకుడి వైపు లేదా దూరంగా కదులుతున్నట్లు కనిపించేలా చేయడానికి మీరు కంట్రోలర్ లేదా కీబోర్డ్ నియంత్రణలను ఉపయోగించబోతున్నారు.

--- task ---

ప్రతి బటన్ కోసం **Code** ట్యాబ్‌ను చూడండి. కోడ్ ఇలా కనిపిస్తుంది:

![Up sprite.](images/up-sprite.png)

```blocks3
when this sprite clicked
broadcast (up v)

when I receive [start v]
forever
go to [front v] layer
go to x:(-190) y: (-121)
end
```

ఇది బటన్‌లను సరైన స్థితిలో ఉంచుతుంది మరియు వాటిని క్లిక్ చేసినప్పుడు వాటి దిశలను బ్రాడ్ కాస్ట్ చేస్తుంది.

--- /task ---

The **rover** needs to be visible at all times, by making sure it is on the **front** layer.

--- task ---

Add a `go to front layer`{:class='block3looks'} to a `green flag clicked`{:class='block3events'} block.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when flag clicked
+ go to [front v] layer
```

--- /task ---

**rover** అన్ని ఇతర sprite ల కోసం ఆట ప్రారంభాన్ని కంట్రోల్ చేయబోతుంది; కాబట్టి ఆకుపచ్చ జెండాను క్లిక్ చేసినప్పుడు, **rover** sprite `start`{:class='block3events'} సందేశాన్ని బ్రాడ్ కాస్ట్ చేయాలి.

--- task ---

Add a `broadcast`{:class='block3events'} block.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when flag clicked
go to [front v] layer
+ broadcast [start v]
```

--- /task ---

--- task ---

మీరు కంప్యూటర్‌లో పని చేస్తున్నట్లయితే, బటన్‌లను ఉపయోగించడం కంటే కీబోర్డ్ కంట్రోల్స్ ను ఉపయోగించడం సులభం కావచ్చు. కీబోర్డ్ కంట్రోల్స్ **rover** sprite కు జోడించబడతాయి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when [up arrow v] key pressed
broadcast [up v]

when [down arrow v] key pressed
broadcast [down v]

when [right arrow v] key pressed
broadcast [right v]

when [left arrow v] key pressed
broadcast [left v]
```

మీరు కంట్రోలర్‌ను ఉపయోగించకూడదనుకుంటే, ప్రతి **button** sprite లపై క్లిక్ చేసి `looks`{:class='block3looks'} మెనులో కల `hide`{:class='block3looks'} బ్లాక్‌పై క్లిక్ చేయండి.

```blocks3
hide
```

--- /task ---

**up** బటన్ క్లిక్ చేసినపుడు లేదా <kbd>up arrow</kbd> ప్రెస్ చేసినపుడు, **rover** చిన్న మొత్తంలో తన `y`{:class="block3motion"} పొజిషన్ ను మార్చుకోవాలి. `y`{:class="block3motion"} పెంచడం ద్వారా **rover** ను పైవైపుకు కదిలించవచ్ఛు. `y`{:class="block3motion"} ని తగ్గించడం ద్వారా **rover** రోవర్ ను క్రిందికి కదిలించవచ్చు.

--- task ---

**up** బటన్ **rover** ని పైకి కదిలేలా చేయడానికి కోడ్‌ని జోడించండి.

![Rovef sprite.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)

when I receive [down v]
change y by (-10)
```

--- /task ---

**మీరు ఇంకా ఎడమ మరియు కుడి కదలికల గురించి ఆందోళన చెందాల్సిన అవసరం లేదు. ప్రాజెక్ట్ యొక్క తదుపరి దశలో ఎడమ మరియు కుడి కదలిక జోడించబడుతుంది.**

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**Perspective**</span> దృశ్యాన్ని మరింత వాస్తవికంగా చేయడానికి కంప్యూటర్ గ్రాఫిక్స్‌లో ఉపయోగించబడుతుంది. సాధారణంగా దూరంగా ఉన్న వస్తువులు స్క్రీన్‌పై చిన్నవిగా మరియు ఎత్తుగా కనిపిస్తాయి. దగ్గరగా ఉన్న వస్తువులు స్క్రీన్‌పై పెద్దవిగా మరియు క్రిందికి కనిపిస్తాయి.
</p>

--- task ---

అది పైకి కదులుతున్నప్పుడు చిన్నదిగా మరియు క్రిందికి కదులుతున్నప్పుడు పెద్దదిగా కనిపించేలా మీ **rover** కి **perspective** ని జోడించండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [up v]
change y by (10)
change size by (-1) //Smaller looks further away


when I receive [down v]
change y by (-10)
change size by (1) //Bigger looks closer
```

--- /task ---

--- task ---

మీరు గేమ్ ప్రారంభంలో **rover** పరిమాణాన్ని రీసెట్ చేయాలి.

```blocks3
when I receive [start v]
set size to (50) %
```

--- /task ---


--- task ---

**పరీక్ష:** **rover** కంట్రోల్ ను తనిఖీ చేయడానికి **up** మరియు **down** బటన్‌లను క్లిక్ చేయండి లేదా యారో కీ లను ఉపయోగించండి.

--- /task ---

--- task ---

ఇప్పుడు ఆట ప్రారంభమైన ప్రతిసారీ **rover** స్థానాన్ని రీసెట్ చేయండి.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
+ go to x: (0) y: (-90)
```

--- /task ---

--- task ---

ప్రస్తుతానికి, **rover** ఇతర sprite ల కన్నా ముందు కనిపించాలి. **rover** ని ముందు లేయర్ కు తరలించండి.

![The rover sprite.](images/rover-sprite.png)

```blocks3
when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
+ go to [front v] layer
```

--- /task ---

--- task ---

**పరీక్ష**: మీ గేమ్ సరిగ్గా రీసెట్ చేయబడిందో లేదో పరీక్షించడానికి ఆకుపచ్చ జెండాను క్లిక్ చేయండి.

--- /task ---

--- save ---
