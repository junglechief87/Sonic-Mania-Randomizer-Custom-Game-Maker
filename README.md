This is the Sonic Mania Randomizer/Custom Game Maker made using Cheat Engine assembly and lua scripting.
This requires Cheat Engine 6.7 or greater to run.

This application allows the creation of custom level orders through Mania Mode, including Encore levels,
and character orders. It should be played on a Mania Mode'No Save' file as certain things this 
application can do have undesired effects when trying to load a save file that was written to while 
using this application, like crashing. Want the first level to be Titanic Monarch Act 1 with Knuckles,
then jump into Stardust Speedway Act 1 with Mighty as the second level, this application will let you
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
Click the Random Game button. The random game uses a random seed, if you don't supply a random seed, a 
number between 1 and 999999999, then the application will auto generate one and place it in the seed
number box. The seed allows for games with the same number to have identical results, this lets games
be shared for things like races. The random game shuffles the Zone order, keeping acts from the same
zones paired together, and changes on a level by level basis whether the act uses the Encore or Mania
Mode layout. Then it shuffles characters on a zone by zone basis. The game uses the end coordinates 
from the first act on many stages to set the starting coordinates of the second act, this is why certain
things are randomized zone by zone instead of act by act, similarly characters could end up in some 
weird states if you were let's say flying with Tails while act 1 was clearning then turned into Sonic.
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
number in an earlier level slot of shorter games, this is to ensure your game has a natural ending (not
having to forcibly terminate the game). I have provided the internal numbers the game uses for relevant
scenes and characters below:

*Going to add this list shortly*