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

Scene Numbers for Stages:
Vanilla
09 GHZ 1
10 GHZ 2
11 CPZ 1
12 CPZ 2
13 SPZ 1
14 SPZ 2
15 FBZ 1
16 FBZ 2
17 PGZ 1
18 PGZ 2
19 SSZ 1
20 SSZ 2
21 Metal Sonic
22 HCZ 1
23 HCZ 2
24 MSZ 1
25 MSZ 1 K
26 MSZ 2
27 OOZ 1
28 OOZ 2
29 LRZ 1
30 LRZ 2
31 LRZ Boss
32 MMZ 1
33 MMZ 2
34 TMZ 1
35 TMZ 2
36 TMZ Boss
37 ERZ
Encore Stages
38 GHZ 1
39 GHZ 2
40 CPZ 1
41 CPZ 2
42 SPZ 1
43 SPZ 2
44 FBZ 1
45 FBZ 2
46 PGZ 1
47 PGZ 2
48 SSZ 1
49 SSZ 2
50 Metal Sonic
51 HCZ 1
52 HCZ 2
53 MSZ 1
54 MSZ 2
55 OOZ 1
56 OOZ 2
57 LRZ 1
58 LRZ 2
59 LRZ Boss
60 MMZ 1
61 MMZ 2
62 TMZ 1
63 TMZ 2
64 TMZ Boss
vanilla
65 emerald stage 1
66 emerald stage 2
67 emerald stage 3
68 emerald stage 4
69 emerald stage 5
70 emerald stage 6
71 emerald stage 7
Encore
72 emerald stage 1
73 emerald stage 2
74 emerald stage 3
75 emerald stage 4
76 emerald stage 5
77 emerald stage 6
78 emerald stage 7
Ending Scenes
126 Sonic Ending
127 Encore Ending
128 Tails Ending
129 Knuckles Ending
130 Mighty Ending
131 Ray Ending
132 Super Sonic Ending

Character Values:
sonic    01
tails    02
knuckles 04
mighty   08
ray	 16

Known Issues
=======================================================================================================
-The issues mentioned above with save files. The game sees to have trouble understanding some things 
	if you try to load some files that were created with this tool. Also worth mentioning the way 
	sequencing is done on this there could be other issues with trying to load existing files. 
	This is why 'No Save' is recommended.
-Coming from Mirage Saloon Act 1 Knuckles Mania Mode to Mirage Saloon Act 2 Encore or coming from 
	Mirage Saloon Act 1 Knuckles Mania Mode as Tails to Mirage Saloon Act 2 Mania Mode or Encore 
	is likely to have you stuck slightly in the ground at the start of Act 2. This collision here
	is favorable, so you can just mash jump and you'll get out or just hit restart.
-Knuckles can make it into the Heavy Rider fight quite naturally in Encore Mode Lava Reef Act 2. When
	the game tries to play his transition animation after the act Knuckles will just continually 
	walk into the wall at the edge of the arena. Since cutscene skip exists in this version of the 
	game, just hit start and you will head to the next zone.

