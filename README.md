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

New in this version
=======================================================================================================
-You can now select Encore mode when running the rando, to do this set the option for Game Mode to Encore, you will still start the game from a 'No Save' Mania Mode file. Encore mode may have a few minor bugs but I wanted to get this version out because it contained a few other bug fixes that I thought were important. In Encore mode, if the custom character primary or secondary slots are enabled, it resets the reserve character slots, 3-5, back to no character each act. This is to keep players from storing one character they want to use and not dealing with what random give them in slots 1 and 2. This is a design decisions, not a bug. Also Mirage Saloon Act 1 Mania and Egg Reverie both still work when Encore mode is set, it will however revert the game to Mania mode for just those levels and then revert back to Encore afterward.

-There are now options to disable Super Music. There are a few minor audio bugs with this setting.

-There is also an option for choosing Sonic's Ability, with one of the choices being random.

-There is now an option to select which versions of levels you want in the pool for the random game. Choices are: Mania, Encore, and All.

-I changed the random game option to 'Write Random Game to RAM', hopefully this makes it more clear that the custom game and random game options are exclusive to themselves.

-The custom game interface has had some GUI upgrades. The boxes are now multiselect for the levels, enjoy being able to select multiple levels at once to add or remove. For characters an option to insert a number of times you would like to add the selected character has been added, so if you want a 24 level run with Sonic as the primary character the whole time you only need to type 24 in this box then select Sonic and add once. This box also works with the secondary character slot and an option for 'None' has been added to the secondary character slot. This should speed up custom game creation.

Bug Fixes
=======================================================================================================
-Fixed bug where big ring flags were not being reset each act but only after an act 2 had been completed. This resulted in some bing rings being disabled without having gone into the special stage. This is now fixed.

-Fixed bug where having an amount of rings to activate super above 50 could cause super transformations to not trigger in ERZ, resulting in deaths. When ERZ starts it now reverts the rings to activate super back to 50. 

Intructions
========================================================================================================
-Make sure Sonic Mania is running. (This is based off of Sonic Mania Plus and uses code from the Encore 
	DLC, please have the latest version of Mania with the Encore DLC.)

-With Sonic Mania running you can start the Sonic Mania Rando.EXE cheat engine trainer. (Cheat Engine 
	trainers require that the applications they are tied to is running before they are started to 
	attach to the process.)

-Click on the check box marked 'Attach New Code to Sonic Mania'. This option sets the necessary hooks
	for the rest of the program to work. Unchecking the box reverts the game code to it's default
	state. Checking or unchecking the checkbox will revert the application back to it's default 
	settings as well.

-With that set you have a few options. You can build a custom game or generate a random game.

Universal Settings
========================================================================================================
Allow Custom level order - This setting allows for a random or custom built level order, without this checkbox checked the game will use the default level order.
	
Allow Custom Character Order - This setting allows for a random or custom built character order, without this checkbox checked the game will use whichever character is selected at the start of the game. This checkbox being checked without the secondary checkbox checked only allows for solo character combos, so no Sonic and Tails or Knuckles and Knuckles without also checking the next box.
	
Allow Custom Secondary Character - This setting allows for a random or custom built character order, without this checkbox checked the game will use whichever secondary character is selected at the start of the game. If 'Custom Primary Character' is selected without this setting then no secondary characters will appear, if this is selected without 'Allow Custom Character Order' selected then you will keep whatever primary character you chose at the start of the game and have a random or custom secondary character, which will overwrite in game options like '& Knuckles' and 'Sonic & Tails'. 'No character' is also an option for secondary character, so in a random game with this option set it is still possible to roll a solo character.
	
Emeralds:
Emerald Count - Sets the starting emerald count. Options are 0-7 and Random. 0-7 give the emeralds in order with 4 having emeralds 1, 2, 3, and 4 and 5 giving those plus emerald 5, leaving the last two emerald stage to complete. Random gives not just a random amount but random emeralds, so you could start with emeralds 1,4, and 5 leaving emerald stages 2, 3, 6, and 7 to complete. Further the stage order will be shuffled on random, so for the above example you won't necessarily have the stages appear in that sequential order (2, 3, 6, 7) it may be that you need to complete the stages in the order 3, 7, 2, and 6.

Emerald Mode - Sets whether emerald stages are their encore or mania mode variants. Options are mania, encore, or random. Random will set whether a stage is mania or encore on a stage by stage basis, so one run can have both mania and encore variants appear.
	
Random Game
========================================================================================================
Level Count - Sets how many levels will happen before the ending in a random game. Options are 1 to 49. The randomizer will attempt to make sure that levels do not repeat and if the level count is 24 or under it will not repeat the a variant on the same level. For instance if Encore Green Hill Act 1 comes up as a level then Mania Green Hill Act 1 will not appear in that seed. If the level is set to over 24 levels then you wont see the other variation of a certain stage until after the 24th level. So for the above example, if you get Encore Green Hill Act 1 in the first 24 levels then Mania Green Hill Act 1 can't appear until level 25 plus. Other consideration have been made for Mirage Saloon Zone Act 1, if level count is set to 49 then all three variations should appear in the run. If Mirage Saloon Act 1 Knuckles appears the game will give the player either Knuckles or Tails or Tails in the secondary slot if 'Allow Custom Secondary Character Order' is checked.

Cap run with Egg Reverie - This should be pretty self explanitory. This will make the final level of the run into Egg Reverie, with a random super character. Egg Reverie is not used in the randomization otherwise, I figure it would be more fun as a unique "Endgame" level to celebrate the finishing of a run.

Randomize Starting Lives - This will make starting lives a random number between 0 and 4. I know both 0 and 1 are 'Game Overs' on death. So if you get zero that just means you basically start at a negative 1 deficit, don't die.

Randomize Rings Required for Super Forms - Makes rings required for turning a character super a random number between 1 and 100.

Shuffle Power Ups - This will change which monitors are which. For instance ring monitors could now be electric shields and electric shields could become speed shoes. This will be consistent throughout the seed, so if you identify what monitor types are shuffled with which then you can plan your routes on later levels around this knowledge. By default the monitor types in the shuffle include: 10 Rings, Blue Shield, Bubble Shield, Fire Shield, Electric Shield, Invincibility, Speed Shoes, Extra Life, Eggman Box, Blue Ring, and Character Switch. That's 11 monitor types that are shuffled, in mania mode only 10 different types appear, so that means one of the 11 won't appear in the seed. 

Include Random and Super Boxes in Power Up Shuffle - 'Shuffle Power Ups' must be checked for this option to be available, only one of 'Include Random and Super Boxes in Power Up Shuffle', 'Make All Power Ups Random Boxes' or 'Get a Load of This!!!!' mayb be checked at a time. This adds two more monitor types to the shuffle, so they have the potential to appear in a run but again it's 10 monitor types with now 13 possible options. 

Make All Power Ups Random Boxes - 'Shuffle Power Ups' must be checked for this option to be available, only one of 'Include Random and Super Boxes in Power Up Shuffle', 'Make All Power Ups Random Boxes' or 'Get a Load of This!!!!' mayb be checked at a time. For the truly zanny experience. This makes all monitors the '?' that you may have seen in multiplayer, it bestows a completely random power up when you break it open.

Get A Load of This!!!!! - HaHaHa!!! Let's see if you can make it through this Sonic!

Random Game - Once all settings are set click the Random Game button. If you change settings after clicking the button please do so again. The application doesn't write the necessary values to memory until this button is clicked. The random game uses a random seed. If you don't supply a random seed, a number between 1 and 999999999, then the application will auto generate one and place it in the seed number box. The seed allows for games with the same number and options to have identical results, this lets games be shared for things like races. If you would like a new seed then earse what is in the random game text box and a new one will genreate when random game is clicked again. *Note: This writes random game setting to RAM, you do not want to click the 'Write Custom Game to RAM' after this, that will overwrite your random game.*

Custom Game
=======================================================================================================
For custome games you can use the arrows to add or remove values to the level order with the lef and right arrow icons. The custom games logic uses the level amount in the 'Custom Level Order' list box to determine the level count. The characters are assigned to the same level that they share an index number with from their list box. If no primary character is assigned to a level it defaults to Sonic, if no Secondary Character is assigned to a level it defaults to 'No Character'. You also have the option to pick an ending. Once all options are set to your liking click the 'Write Custom Game to Ram'. This option will set the necessary values to make the custom game playable in game. If you change any settings make sure to click 'Write Custom Game to Ram' again.

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
	
-Only in Press Garden Act 2, the monitors will still show their default images when frozen in ice, if Power Up Shuffle is on. If you break the ice you will see the correct monitor image. This is obviously an issue with the game having specific assest for monitors frozen in ice.
	
-It has been reported that the randomizer will not work if background pausing is disabled in Sonic Mania. Make sure background pausing is enabled.

-When activating super as a mini character in MMZ2, the super music will not be disabled. 

-Deactivating super music appears to deactivate the drowning music too.

-There was a bug where it would spawn the player inside the wall when going to the boss scene for LRZ2 Mania Mode as Knuckles while in Encore Mode. You will notice that the Boss fights for LRZ2 always takes place in the Encore version, which is just a palette swap, now. This prevents this bug.

-There is some odd issue with how continues work with encore set. Often it will just spawn you back at the alst checkpoint when you die with the timer where it was at previously, not sure what causes this but it really doesn't hurt how Encore works, so for now consider it a nice help that you don't game over, you might have to watch for timer overs now though.
