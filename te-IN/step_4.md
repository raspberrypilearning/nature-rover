## మరిన్ని sprite లను స్క్రోల్ చేయండి

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
మీ సన్నివేశానికి మరిన్ని sprite లను జోడించేటప్పుడు, ఇవి ఎడమ మరియు కుడికి కూడా స్క్రోల్ చేయాలి.
</div>
<div>
![](images/step-4.gif){:width="300px"}
</div>
</div>

ఇప్పుడు మీరు మీ సన్నివేశానికి మరికొన్ని వస్తువులను జోడించవచ్చు మరియు వాటిని ఇదే విధంగా స్క్రోల్ చేయవచ్చు.

--- task ---

**tree** sprite ని జోడించి, ఆపై దాని ప్రారంభ స్థానాన్ని సెట్ చేయండి.

![Tree sprite.](images/tree-sprite.png)
```blocks3
when I receive [start v]
go to x:(0) y:(-80)
```

--- /task ---

**tree** sprite కూడా బ్రాడ్ కాస్ట్ దిశకు, **ఎదురుగా** దిశలో కదలాలి.

![చెట్టు యొక్క యానిమేషన్ కుడి మరియు ఎడమకు కదులుతుంది, తద్వారా x కోఆర్డినేట్ మారుతున్నట్లు చూపుతుంది.](images/scrolling-tree.gif)

చెట్టు వీక్షకుడికి దగ్గరగా ఉన్నందున, బటన్ లేదా కీని నొక్కిన ప్రతిసారీ అది కొండల కంటే ఎక్కువ దూరం కదులుతున్నట్లు కనిపిస్తుంది.

--- task ---

ఈ కదిలే ప్రభావాన్ని పొందడానికి, బ్రాడ్ కాస్ట్ ల ద్వారా పొందే, **tree** sprite యొక్క `left`{:class="block3events"} కి మరియు `right`{:class="block3events"} కి కదిలే `x`{:class='block3motion'} విలువలను మార్చండి.

![Tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [left v]
change x by (10) //Use a bigger number than for the hills

when I receive [right v]
change x by (-10) //Use a bigger number than for the hills
```

--- /task ---

--- task ---

**Test:** Click the green flag and check your left and right buttons now. మీరు కంట్రోలర్‌పై క్లిక్ చేసిన ప్రతిసారీ చెట్టు కదలాలి.

**పరీక్ష:** మీరు చెట్టు నుండి వీలైనంత దూరంగా వెళితే ఏమి జరుగుతుంది?

--- /task ---

చెట్టు స్క్రీన్ అంచుకు చేరుకున్నప్పుడు, అది కదలకుండా ఆగిపోతుందని మీరు గమనించారా? `x`{:class='block3motion'} కోఆర్డినేట్ చాలా ఎక్కువగా లేదా చాలా తక్కువగా ఉన్నప్పుడు మీరు చెట్టును స్క్రీన్‌కి అవతలి వైపుకు తరలించడం ద్వారా దీన్ని పరిష్కరించవచ్చు.

--- task ---

`forever`{:class='block3control'} లూప్, మరియు `if`{:class='block3control'} బ్లాకులను ఉపయోగించి, చెట్టు యొక్క `x`{:class='block3motion'} కోఆర్డినేట్ ను చెక్ చేయండి, మరియు `x`{:class='block3motion'} విలువ `290` కంటే ఎక్కువగా ఉన్నప్పుడు లేదా `-290` కన్నా తక్కువయినపుడు, దానిని, స్క్రీన్ కి అవతలి వైపుకు తరలించండి.

![Tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ forever
if <(x position) > (290)> then //The tree is at the far right
set x to (-280) //Move the tree to the far left
end
if <(x position) < (-290)> then //The tree is at the far left
set x to (280) //Move the tree to the far right
end
end
```

--- /task ---

--- task ---

ఇప్పుడు మీ **rover** sprite ని స్క్రీన్ చుట్టూ తరలించండి. చెట్టు అంచుకు చేరుకున్నప్పుడు, అది స్క్రీన్ అంచు నుండి అదృశ్యమై, మరొక వైపు మళ్లీ కనిపిస్తుంది.

--- /task ---

--- task ---

Lastly, make the **rover** turn left and right so that it faces the direction it is moving in, and resets at the start.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when flag clicked
broadcast [start v]
+ set rotation style [left-right v]

when I receive [left v]
point in direction (-90)

when I receive [right v]
point in direction (90)

when I receive [start v]
set size to (50) %
go to x: (0) y: (-90)
go to [front v] layer
+ point in direction (90)
```

--- /task ---

--- task ---

**పరీక్ష:** మీ ప్రాజెక్ట్‌ను అమలు చేయండి మరియు దానిని పరీక్షించండి. రోవర్ కదులుతున్నప్పుడు, చెట్టు స్క్రీన్ అంచు నుండి పడిపోయి, మరలా మరొక వైపు కనిపించేలా చూసుకోండి.

--- /task ---
