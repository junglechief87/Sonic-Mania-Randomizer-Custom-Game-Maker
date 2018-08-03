This is the Sonic Mania Randomizer/Custom Game Maker made using Cheat Engine assembly and lua scripting.
This requires Cheat Engine 6.7 or greater to run.

This application allows the creation of custom level orders through Mania Mode, including Encore levels,
and character orders. It should be played on a Mania Mode'No Save' file as certain things this 
application can do have undesired effects. For instance, trying to load a save file that was written to while 
using this application can cause crashing. Want the first level to be Titanic Monarch Act 1 with Knuckles,
then jump into Stardust Speedway Act 1 with Mighty as the second level? This application will let you
set that up. It also contains functionality to create a random game using seeds, so the experience
can be different each time you play. You can even share the seed number with someone so they can have
the same experience or start a race with the same level and character layout.

Intructions
========================================================================================================
-Make sure Sonic Mania is running. (This is based off of Sonic Mania Plus and uses code from the Encore 
	DLC, please have the latest version of Mania with the Encore DLC.)

-With Sonic Mania running you can start the Sonic Mania Rando.EXE cheat engine trainer. (Cheat Engine 
	trainers require that the applications they are tied to is running before they are started to 
	attach to the process.)

-Click on the check box marked 'Allow Custom Level/Character Order'. This option sets the necessary hooks
	for the rest of the program to work. Unchecking the box reverts the game code to it's default
	state.

-With that set you have a few options. You can build a custom game or generate a random game.

Random Game
========================================================================================================
Click the Random Game button. The random game uses a random seed. If you don't supply a random seed, a 
number between 1 and 999999999, then the application will auto generate one and place it in the seed
number box. The seed allows for games with the same number to have identical results, this lets games
be shared for things like races. The random game shuffles the zone order, keeping acts from the same
zones paired together, and changes on a level by level basis whether the act uses the Encore or Mania
Mode layout. Then it shuffles characters on a zone by zone basis. The game uses the end coordinates 
from the first act on many stages to set the starting coordinates of the second act, this is why certain
things are randomized zone by zone instead of act by act, similarly characters could end up in some 
weird states if you were, let's say, flying with Tails while act 1 was clearning then turned into Sonic.
I would like to eventually have all of this randomized level by level but for now this is done to ensure
stability. Furthermore, if the game rolls Mirage Saloon Act 1 Knuckles then it will ensure that your 
character is either Tails or Knuckles for that zone, yes that level is completable with Tails. 

Custom Game
=======================================================================================================
For a custom game you will fill in the provided boxes with level 'scene' numbers (these are the 
internal numbers the game uses to reference where in the game the player is) and character numbers.
Feel free to use any combos you want but remember that some could create undesireable effects, I 
referenced some of these effects in the Random Game section. It's not hard to end up stuck in the floor
of Studiopolis Act 1 when coming from a different Act 1. Make sure to fill in an ending after your final
level. I have provided an ending slot if you use all 24 level slots or you could put the ending 'scene'
number in an earlier level slot for shorter games, this is to ensure your game has a natural ending (not
having to forcibly terminate the game). I have provided the internal numbers the game uses for relevant
scenes and characters below:

Scene Numbers for Stages:<br>
Vanilla<br>
09 GHZ 1<br>
10 GHZ 2<br>
11 CPZ 1<br>
12 CPZ 2<br>
13 SPZ 1<br>
14 SPZ 2<br>
15 FBZ 1<br>
16 FBZ 2<br>
17 PGZ 1<br>
18 PGZ 2<br>
19 SSZ 1<br>
20 SSZ 2<br>
21 Metal Sonic<br>
22 HCZ 1<br>
23 HCZ 2<br>
24 MSZ 1<br>
25 MSZ 1 K<br>
26 MSZ 2<br>
27 OOZ 1<br>
28 OOZ 2<br>
29 LRZ 1<br>
30 LRZ 2<br>
31 LRZ Boss<br>
32 MMZ 1<br>
33 MMZ 2<br>
34 TMZ 1<br>
35 TMZ 2<br>
36 TMZ Boss<br>
37 ERZ<br>
Encore Stages<br>
38 GHZ 1<br>
39 GHZ 2<br>
40 CPZ 1<br>
41 CPZ 2<br>
42 SPZ 1<br>
43 SPZ 2<br>
44 FBZ 1<br>
45 FBZ 2<br>
46 PGZ 1<br>
47 PGZ 2<br>
48 SSZ 1<br>
49 SSZ 2<br>
50 Metal Sonic<br>
51 HCZ 1<br>
52 HCZ 2<br>
53 MSZ 1<br>
54 MSZ 2<br>
55 OOZ 1<br>
56 OOZ 2<br>
57 LRZ 1<br>
58 LRZ 2<br>
59 LRZ Boss<br>
60 MMZ 1<br>
61 MMZ 2<br>
62 TMZ 1<br>
63 TMZ 2<br>
64 TMZ Boss<br>
vanilla<br>
65 emerald stage 1<br>
66 emerald stage 2<br>
67 emerald stage 3<br>
68 emerald stage 4<br>
69 emerald stage 5<br>
70 emerald stage 6<br>
71 emerald stage 7<br>
Encore<br>
72 emerald stage 1<br>
73 emerald stage 2<br>
74 emerald stage 3<br>
75 emerald stage 4<br>
76 emerald stage 5<br>
77 emerald stage 6<br>
78 emerald stage 7<br>
Ending Scenes<br>
126 Sonic Ending<br>
127 Encore Ending<br>
128 Tails Ending<br>
129 Knuckles Ending<br>
130 Mighty Ending<br>
131 Ray Ending<br>
132 Super Sonic Ending<br>

Character Values:<br>
sonic    01<br>
tails    02<br>
knuckles 04<br>
mighty   08<br>
ray	 16<br>

Known Issues
=======================================================================================================
-The issues mentioned above with save files. The game seems to have trouble understanding some things 
	if you try to load saved files that were created while using this application. Also worth 
	mentioning the way sequencing is done on this there could be other issues with trying to load 
	existing files. This is why 'No Save' is recommended.
	
-Coming from Mirage Saloon Act 1 Knuckles Mania Mode to Mirage Saloon Act 2 Encore or coming from 
	Mirage Saloon Act 1 Knuckles Mania Mode as Tails to Mirage Saloon Act 2 Mania Mode or Encore 
	is likely to have you stuck slightly in the ground at the start of Act 2. The collision here
	is favorable, so you can just mash jump and you'll get out or just hit restart.
	
-Knuckles can make it into the Heavy Rider fight quite naturally in Encore Mode Lava Reef Act 2. When
	the game tries to play his transition animation, after the act, Knuckles will just continually 
	walk into the wall at the edge of the arena. Since cutscene skip exists in this version of the 
	game, just hit start and you will head to the next zone.

-Going from Green Hill Act 1 Encore Mode to Green Hill Act 2 Mania Mode causes the color palettes to 
	become blended for some reason, you should still be able to tell the background changed and 
	that the level is the Encore or Mania Mode version as the level starts. 
	
-Cheat Engine uses lua for some strange reason as it's scripting language, so this is what the 
	randomizer is written in. Lua has notoriously bad random functions. I have taken some steps
	to mitigate this but if you find that you are getting similar seeds or seed numbers then I
	would recommend just going to random.org and grabbing a seed number from there and pasting
	it into the randomizer gui.
