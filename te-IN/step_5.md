## ఒక నమూనా సేకరించండి

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ఈ దశలో, మీరు నమూనాలను సేకరించే రోవర్‌ను చూపించడానికి sprite మరియు రోవర్ రూపాన్ని మారుస్తారు.
</div>
<div>
![Animation of the rover moving across the stage, from time to time the rover appears to move further into the background getting smaller and then returning to the foreground](images/step-4.gif){:width="300px"}
</div>
</div>

--- task ---

**rover** sprite యొక్క costume లను చూడండి. ఆరు యానిమేషన్లు అందుబాటులో ఉన్నాయి. **rover** చేయగలిగినవి:
- దాని చేతిని విస్తరించండి

![రోవర్ చేయి విస్తరించి ఉన్న మూడు costumes.](images/arm-animation.png)

- భూమిలోకి డ్రిల్ చేయండి
- గాలి పీల్చుకోండి
- సోలార్ ప్యానెల్‌ను విస్తరించండి
- ఫోటో తీయ్యండి
- ఏదైనా కొంచెం తవ్వి తీయండి

--- /task ---

మీరు Scratchలో వివిధ costume మార్పుల వంటి అనేక కోడ్‌లను నిర్వహించాలనుకున్నప్పుడు, `My Blocks`{:class="block3myblocks"} ని ఉపయోగించడం ప్రయోజనకరంగా ఉంటుంది. ఇది మీ స్వంత కస్టమ్ బ్లాక్‌లను సృష్టించడానికి మిమ్మల్ని అనుమతిస్తుంది.

మీ **rover** sprite ప్రతి యానిమేషన్ కోసం ఒక `My Block`{:class="block3myblocks"} కలిగి ఉంటుంది.

--- task ---

`My Blocks`{:class="block3myblocks"} మెనులో **Make a Block** పైన క్లిక్ చేయండి, మీ క్రొత్త బ్లాక్ కు `sample fruit`{:class="block3myblocks"} అని పేరు ఇవ్వండి.

--- /task ---

మీ స్క్రిప్ట్‌లో కొత్త బ్లాక్ కనిపించాలి. ఇది ఇలా కనిపిస్తుంది:

![Rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit
```

--- task ---

ఈ బ్లాక్ కింద, కొన్ని `switch costume`{:class="block3looks"} బ్లాకులు మరియు `wait`{:class="block3control"} బ్లాకులను, రోబోట్ ను యానిమేట్ చేయడం కోసం జోడించండి.

**చిట్కా:** మీ మొదటి `switch costume`{:class='block3looks'} బ్లాక్ మరియు `wait`{:class='block3control'} బ్లాక్‌ని సృష్టించడం త్వరగా జరుగుతుంది, ఆపై వాటిని డూప్లికేట్ చేసి, ఉపయోగించిన costume లను మార్చండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

పండ్ల నమూనాను సేకరించినప్పుడు **rover** sprite ధ్వనిని ప్లే చేసేలా బ్లాక్‌ను జోడించండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit //Animates the robot to collect fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ start sound (Collect v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---


--- task ---

మీరు యానిమేషన్‌ను చూడటానికి `define sample fruit`{:class="block3myblocks"} బ్లాక్‌పై క్లిక్ చేయవచ్చు. మీరు చిన్న స్క్రీన్‌పై ఉన్నట్లయితే, మీరు దగ్గరగా చూడవలసి ఉంటుంది.

`sample fruit block`{:class='block3myblocks'}ని ఉపయోగించనందున, మీరు ఆకుపచ్చ జెండాను క్లిక్ చేసినప్పుడు యానిమేషన్ అమలు చేయబడదు.

--- /task ---

--- task ---

మీ కొత్త బ్లాక్‌ని ఉపయోగించడానికి, మీరు దానిని `event`{:class="block3events"} బ్లాక్‌కి జోడించవచ్చు. `My Blocks`{:class="block3myblocks"} మెనులో, మీరు చేసిన బ్లాక్‌ని మీరు చూడాలి. కింది స్క్రిప్ట్‌లో దీన్ని ఉపయోగించండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when this sprite clicked
sample fruit ::custom //Run the animation
```

--- /task ---

--- task ---

**rover** sprite పై క్లిక్ చేయండి మరియు మీరు యానిమేషన్‌ను చూడాలి.

--- /task ---

ఇప్పుడు మీరు రోవర్ నిజానికి నమూనాను సేకరించేలా చేయాలి. ఈ ఉదాహరణలో, రోవర్ ఒక చెట్టు నుండి పండ్లను సేకరిస్తుంది.

--- task ---

**tree** spriteకి రెండు వేర్వేరు costumes ఉండేలా ఎడిట్ చేయాలి. పండుని కలిగింది ఒకటి (`tree with fruit`{:class="block3looks"}), మరియు పండు లేనిది ఒకటి (`tree without fruit`{:class="block3looks"}). Costumesలో ఒకదానిని ఎడిట్ చేయండి, తద్వారా **tree** లో రెండు వేర్వేరు costumes ఉంటాయి.

--- /task ---

--- task ---

**tree** sprite లో, ప్రాజెక్ట్ ప్రారంభంలో **tree** costume ను మరియు `sample fruit`{:class="block3events"} బ్రాడ్ కాస్ట్ ని అందుకున్నప్పుడు అది మారవలసిన costume ను, సెట్ చేయడానికి బ్లాక్‌లను జోడించండి.

![Tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
+ switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
end
if <(x position) < (-290)> then
set x to (280)
end
end

+ when I receive [sample fruit v]
+ switch costume to (tree without fruit v)
```

--- /task ---

--- task ---

**rover** sprite లో, costume మార్పు చేయడానికి, మీరు కొత్త `broadcast`{:class="block3events"} ని ఉపయోగించవచ్చు. ఈ కొత్త `broadcast`{:class="block3events"} ని, మీ `define sample fruit`{:class="block3myblocks"} ఫంక్షన్ లోనికి జోడింఛండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
define sample fruit
switch costume to (inactive v)
wait (0.3) seconds
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (arm 2 v)
wait (0.3) seconds
+ broadcast (sample fruit v)
switch costume to (arm 1 v)
wait (0.3) seconds
switch costume to (inactive v)
```

--- /task ---

--- task ---

**పరీక్ష:** మీ కోడ్ పని చేస్తుందో లేదో తనిఖీ చేయడానికి, ఫ్లాగ్‌పై క్లిక్ చేసి, ఆపై మీ **rover** sprite పై క్లిక్ చేయండి. దాని చేయి విస్తరించాలి మరియు **tree** sprite costume లను మార్చాలి.

**చిట్కా:** పూర్తి స్క్రీన్ మోడ్‌కి మారండి మరియు మీరు యానిమేషన్‌ను మరింత సులభంగా చూడగలరు.

--- /task ---

రోవర్ పండ్లను తాకినట్లయితే మాత్రమే దానిని సేకరించగలగాలి.

--- task ---

**rover** sprite పైన, `when this sprite clicked`{:class="block3events"} బ్లాకుల సెట్ ను మార్చండి, తద్వారా **rover** sprite పండు కలర్ ను తాకినప్పుడు మాత్రమే, `sample fruit`{:class="block3myblocks"} ఫంక్షన్ పిలవబడుతుంది.

**చిట్కా:** టెస్టింగ్ నుండి మీ costume మారడం వల్ల పండు కనిపించడం లేదని అర్థం కావచ్చు. **tree** sprite కోసం costume ట్యాబ్‌పై క్లిక్ చేసి, కనిపించే పండుతో గల costumeకి మారండి.

![Rover sprite.](images/rover-sprite.png)

```blocks3
when this sprite clicked
if <touching color (#FFA500) ?> then //Colour of fruit
sample fruit ::custom
```

--- /task ---

--- task ---

ఇప్పుడు **tree** sprite ఒక పండును శాంపిల్ చేసినప్పుడు మారుతుంది, కాబట్టి మీరు sprite స్క్రీన్‌పైకి వెళ్లినప్పుడు దాని మొదటి కాస్ట్యూమ్‌కి రీసెట్ చేయాలి.

![Tree sprite.](images/tree-sprite.png)

```blocks3
when I receive [start v]
go to x:(-90) y:(-80)
switch costume to (tree with fruit v)
forever
if <(x position) > (290)> then
set x to (-280)
+ switch costume to (tree with fruit v)
end
if <(x position) < (-290)> then
set x to (280)
+ switch costume to (tree with fruit v)
end
end
```

--- /task ---

--- task ---

**పరీక్ష:** **rover** sprite ను అది పండ్లను తాకేలా తరలించి, ఆపై **rover** sprite పై క్లిక్ చేసి, చెట్టు నుండి పండ్లను సేకరించడాన్ని చూడండి.

--- /task ---


--- save ---
