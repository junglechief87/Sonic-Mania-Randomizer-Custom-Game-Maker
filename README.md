This is the Sonic Mania Randomizer/Custom Game Maker made using Cheat Engine assembly and lua scripting.
This requires Cheat Engine 6.7 or greater to run.

This application allows the creation of custom level orders through Mania Mode, including Encore levels,
and character orders. It should be played on a Mania Mode 'No Save' file as certain things this 
application does can have undesired effects on a file that saves progress. For instance, trying to load a 
save file that was written to while using this application can cause crashing. Want the first level to 
be Titanic Monarch Act 1 with Knuckles, then jump into Stardust Speedway Act 1 with Mighty as the second 
level? This application will let you set that up. It also contains functionality to create a random game 
using seeds, so the experience can be different each time you play. You can even share the seed number 
with someone so they can have the same experience or start a race with the same level and character layout.

Intructions
========================================================================================================
-Make sure Sonic Mania is running. (This is based off of Sonic Mania Plus and uses code from the Encore 
	DLC, please have the latest version of Mania with the Encore DLC.)

-With Sonic Mania running you can start the Sonic Mania Rando.EXE cheat engine trainer. (Cheat Engine 
	trainers require that the applications they are tied to is running before they are started to 
	attach to the process.)

-Click on the check box marked 'Allow Custom Level/Character Order'. This option sets the necessary hooks
	for the rest of the program to work. Unchecking the box reverts the game code to it's default
	state. Checking or unchecking the checkbox will revert the application back to it's default 
	settings as well.

-With that set you have a few options. You can build a custom game or generate a random game.

Universal Settings
========================================================================================================
Custom level order - This setting allows for a random or custom built level order, without this checkbox 
	checked the game will use the default level order.
	
Custom Primary Character - This setting allows for a random or custom built character order, without
	this checkbox checked the game will use whichever character is selected at the start of the game.
	This checkbox being checked without the secondary checkbox checked only allows for solo character
	combos, so no Sonic and Tails or Knuckles and Knuckles without also checking the next box.
	
Custom Secondary Character - This setting allows for a random or custom built character order, without
	this checkbox checked the game will use whichever secondary character is selected at the start 
	of the game. If 'Custom Primary Character' is selected without this setting then no secondary
	characters will appear, if this is selected without 'Custom Primary Character' selected then 
	you will keep whatever primary character you chose at the start of the game and have a random
	or custom secondary character, which will overwrite in game options like '& Knuckles' and 'Sonic
	& Tails'. 'No character' is also an option for secondary character, so in a random game with this 
	option set it is still possible to roll a solo character.
	
Emeralds:
Starting Emeralds - 
Emerald Mode -
	
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

Known Issues
=======================================================================================================
-The issues mentioned above with save files. The game seems to have trouble understanding some things 
	if you try to load saved files that were created while using this application. Also worth 
	mentioning the way sequencing is done on this there could be other issues with trying to load 
	existing files. This is why 'No Save' is recommended.
	
-Knuckles can make it into the Heavy Rider fight quite naturally in Encore Mode Lava Reef Act 2. When
	the game tries to play his transition animation, after the act, Knuckles will just continually 
	walk into the wall at the edge of the arena. Since cutscene skip exists in this version of the 
	game, just hit start and you will head to the next zone.
	
-Cheat Engine uses lua for some strange reason as it's scripting language, so this is what the 
	randomizer is written in. Lua has notoriously bad random functions. I have taken some steps
	to mitigate this but if you find that you are getting similar seeds or seed numbers then I
	would recommend just going to random.org and grabbing a seed number from there and pasting
	it into the randomizer gui.
