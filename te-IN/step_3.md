## నేపథ్యాన్ని స్క్రోల్ చేయండి

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
రోవర్ ఎడమ మరియు కుడి వైపుకు కదులుతున్నట్లుగా కనిపించాలంటే, **rover** sprite కదలడం కాకుండా, **background** sprite ఎడమ లేదా కుడి వైపుకు కదులుతుంది లేదా స్క్రోల్ చేస్తుంది.
</div>
<div>
![](images/step-3.gif){:width="300px"}
</div>
</div>

--- task ---

**hills** sprite ని ఎంచుకోండి. ఆట ప్రారంభంలో, మీరు అది సరైన స్థానంలో మరియు వెనుక లేయర్లో ఉందని నిర్ధారించుకోవాలి.

![Hills sprite.](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
```

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">**లేయర్‌లు**</span> మీరు చిత్రాలను గీయగలిగే స్పష్టమైన ప్లాస్టిక్‌తో పేర్చబడిన షీట్‌ల వలె ఉంటాయి. స్టాక్ పైభాగంలో ఉన్న చిత్రం దాని క్రింద ఉన్న చిత్రాన్ని కవర్ చేస్తున్నట్లయితే, మీరు దిగువ చిత్రాన్ని సరిగ్గా చూడలేరు. నేపథ్య చిత్రాలు **back** లేయర్‌కు సమీపంలో ఉండాలి. వీక్షకుడికి దగ్గరగా ఉండే చిత్రాలు **front** లేయర్‌కు సమీపంలో ఉండాలి.
</p>

--- task ---

**hills** sprite తనని తను కాపీని తయారు చేసుకోవాలి. వీటిని `clones`{:class='block3control'} అంటారు. అప్పుడు, ఒరిజినల్ sprite ని స్క్రీన్‌కి కుడి వైపునకు తరలించవచ్చు.

![Hills sprite.](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
+ create clone of [myself v] //కొండల యొక్క కాపీని సృష్టించండి
+ change x by (460) //అసలు కొండలను స్క్రీన్ కుడివైపుకి తరలించండి
```

--- /task ---

`left`{:class='block3events'} మరియు `right`{:class='block3events'} బ్రాడ్ కాస్ట్ లు అందుకోగానే, the **hills** sprite కదలడం ప్రారంభించాలి. సరైన దిశలో కదులుతున్నట్లు కనిపించడానికి, **rover** కుడివైపు కదులుతున్నప్పుడు, వెనుక నేపథ్యం **left** కి కదులుతుంది. చలన దిశ `broadcast`{:class='block3events'} కి **ఎదురుగా** గా ఉంటుంది.

కాబట్టి, ఒకవేళ బ్రాడ్ కాస్ట్ `left`{:class="block3events"} అయితే, అప్పుడు `x`{:class="block3motion"} పొజిషన్ పెరుగుతుంది. కాబట్టి, ఒకవేళ బ్రాడ్ కాస్ట్ `right`{:class="block3events"} అయితే, **hills** యొక్క `x`{:class="block3motion"} పొజిషన్ తగ్గుతుంది.

![Scratch దశ దిగువన కుడి-చేతి మూలలో sprite మరియు బ్యాక్‌డ్రాప్‌గా చూపబడిన xy కోఆర్డినేట్ సిస్టమ్‌తో Stage కనిపిస్తుంది.](images/scratch-grid.png)

--- task ---

**hills** sprite మరియు దాని క్లోన్ యొక్క కదలికను కంట్రోల్ చేయడానికి బ్లాక్‌లను జోడించండి.

![Hills sprite.](images/hills-sprite.png)

```blocks3
when I receive [left v]
change x by (3)

when I receive [right v]
change x by (-3)
```

--- /task ---

--- task ---

**పరీక్ష**: చుట్టూ తిరగడానికి కంట్రోలర్ లేదా <kbd>బాణం</kbd> కీ లను ఉపయోగించండి. రోవర్ ఎడమ మరియు కుడికి కదులుతున్నట్లు కనిపించాలి.

--- /task ---

ప్రస్తుతానికి **hills** sprite యొక్క రెండు కాపీలు ఉన్నాయి: ఒరిజినల్ మరియు క్లోన్. మీరు ఒకదాని చివరకి చేరుకున్నప్పుడు, స్క్రీన్ తెల్లగా ఉన్నట్లు మీరు గమనించవచ్చు.

దీన్ని పరిష్కరించడానికి, sprite మరియు దాని క్లోన్ చాలా దూరం వెళ్లినప్పుడు వాటిని స్క్రీన్‌కి అవతలి వైపుకు తరలించాలి.

--- task ---

`scroll`{:class='block3events'} అనే కొత్త బ్రాడ్ కాస్ట్ ను సృష్టించండి మరియు దానిని `start`{:class='block3events'} స్క్రిప్ట్‌కు జోడించండి.

![Hills sprite.](images/hills-sprite.png)

```blocks3
when I receive [start v]
go to [back v] layer
go to x: (0) y: (0)
create clone of [myself v]
change x by (460) 
+ broadcast [scroll v]
```

--- /task ---

--- task ---

**hills** sprite లేదా దాని క్లోన్ ఎడమ లేదా కుడికి చాలా దూరం తరలించబడిందో లేదో గుర్తించడానికి కోడ్‌ను జోడించి, ఆపై వాటి స్థానాలను స్క్రీన్‌కు అవతలి వైపుకు రీసెట్ చేయండి.

![Hills sprite.](images/hills-sprite.png)

```blocks3
when I receive [scroll v]
forever
if <(x position) > (460)> then //Hills sprite స్క్రీన్ కుడి వైపున ఉంది
set x to (-460) //స్క్రీన్ ఎడమ వైపుకు రీసెట్ చేయండి
end
if <(x position) < (-460)> then //Hills sprite స్క్రీన్ ఎడమ వైపున ఉంది
set x to (460) //స్క్రీన్ కుడి వైపుకు రీసెట్ చేయండి
end
```

--- /task ---

--- task ---

**పరీక్ష** **rover**ని తరలించడానికి కంట్రోలర్ లేదా <kbd>arrow</kbd> కీ లను ఉపయోగించండి. బాక్ గ్రౌండ్ స్క్రోల్ చేయాలి మరియు **rover** ఎప్పటికీ చివరకు చేరుకోకూడదు.

--- /task ---

--- save ---
