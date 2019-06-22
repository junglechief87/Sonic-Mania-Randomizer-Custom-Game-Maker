*Fixes for 1.6 are up, use the version with 1.0.6 in the title. The other version is if you are using Sonic Mania 1.3.

This is the Sonic Mania Randomizer/Custom Game Maker made using Cheat Engine assembly and lua scripting.
This requires Cheat Engine 6.7 or greater to run.

This application allows the creation of custom level orders through Mania Mode, including Encore levels,
and character orders. It should be played on a 'No Save' file for the mode of your choice as certain things 
this application does can have undesired effects on a file that saves progress.  Want the first level to 
be Titanic Monarch Act 1 with Knuckles, then jump into Stardust Speedway Act 1 with Mighty as the second 
level? This application will let you set that up. It also contains functionality to create a random game 
using seeds, so the experience can be different each time you play. You can even share the seed number 
with someone so they can have the same experience or start a race with the same level and character layout.

New in this version
=======================================================================================================
-Mid-level warps(These are the screen fadouts that happen in Stardust Speedway Act 2, Laval Reef Act 2, and Titanic Monarach Act 2 and are technically Act 3 in the game's code) can now be shuffled amongst eachother. Included with this setting are the Knuckles spawn points in levels. This includes Green Hill Act 1, Mirage Saloon Act 2, and Lava Reef Act 3 or the Heavy King area. 

-Boss HP can now be randomized. This setting uses a high and low range to determine it's random number, the default is the recommended range. 

-Act and boss music can now by shuffled. Act music is randomized between all unique tracks in the game and boss music is randomized on the fly per attempt from all boss music stored in an act's data file. 

-Act start points can now be randomized among a number of fixed starting positions.

-There is now a "Boss Rush Mode". This uses the fixed starting positions to spawn the player before the boss of each level along with all the rest of their random settings.

-Angel Island is now in the Shuffle. Similar to how the Mirage Saloon Auto-Scroller switches the game mode back to Mania for it's duration, Angel Island sets the game to Encore. When Angel Island appears in the shuffle it is replacing Green Hill Zone 1 Encore.

-Max level count is now 50, to include Angel Island.

-Removed game mode button. 'No Save' game files now work from either the Mania Mode or Encore Mode Screen with the randomizer, I think this is a more intuitive way for players to select game mode. 

-A "New Seed" button was added next to the "Write Random Game to RAM" button. This button behaves the same as the "Write Random Game to RAM" button and can be used to generates seeds just the same, the only difference is it clears the seed text window before generating the random game. Basically if the player wants to cycle through seed numbers this saves them the clicks from having to erase a current seed. 

Bug Fixes
=======================================================================================================
-All sound bugs tied to the "Disable Super Music" option have been fixed.

-Game Overs now work correctly in Encore.

-All act transition bugs have been fixed. 

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

Disable Super Music - Pretty self explanatory, keeps the super music from ever playing which can get pretty repetitive while playing the game.

Random Game
========================================================================================================
Level Count - Sets how many levels will happen before the ending in a random game. Options are 1 to 50. The randomizer will attempt to make sure that levels do not repeat and if the level count is 24 or under it will not repeat a variant on the same level. For instance if Encore Green Hill Act 1 comes up as a level then Mania Green Hill Act 1 will not appear in that seed. If the level is set to over 24 levels then you wont see the other variation of a certain stage until after the 24th level. So for the above example, if you get Encore Green Hill Act 1 in the first 24 levels then Mania Green Hill Act 1 can't appear until level 25 plus. Other consideration have been made for Mirage Saloon Zone Act 1, if level count is set to 49 then all three variations should appear in the run. If Mirage Saloon Act 1 Knuckles appears the game will give the player either Knuckles or Tails or Tails in the secondary slot if 'Allow Custom Secondary Character Order' is checked. If the level count is 50 then Angel Island is guaranteed to appear. 

Cap run with Egg Reverie - This should be pretty self explanitory. This will make the final level of the run into Egg Reverie, with a random super character. Egg Reverie is not used in the randomization otherwise, I figure it would be more fun as a unique "Endgame" level to celebrate the finishing of a run.

Randomize Starting Lives - This will make starting lives a random number between 0 and 4. I know both 0 and 1 are 'Game Overs' on death. So if you get zero that just means you basically start at a negative 1 deficit, don't die.

Shuffle Act 3 and Knuckles Entrances - This shuffles mid-level warps(These are the screen fadouts that happen in Stardust Speedway Act 2, Laval Reef Act 2, and Titanic Monarach Act 2 and are technically Act 3 in the game's code) amongst eachother. Included with this setting are the Knuckles spawn points in levels. This includes Green Hill Act 1, Mirage Saloon Act 2, and Lava Reef Act 3 or the Heavy King area. Boss Rush disables this setting, Boss Rush uses different logic for spawning into the Heavy King area.

Shuffle Level Start Spawns - Randomizes act start points among a number of fixed starting positions. Each level has a 1 out of 100 chance of putting the player near the end of the level with this setting. The average level has around 4 spawn points generally picked from divergent route points early in levels. 

Boss Rush - This setting just guarantees the play starts at he final checkpoint before the boss when picking level spawn points. If the level is Lava Reef Act 2, Stardust Speedway Act 2, or Titanic Monarch Act 2, it instead sets the level to what is technically act 3 for those zones, where the boss fights happen. 

Randomize Rings Required for Super Forms - Makes rings required for turning a character super a random number between 1 and 100.

Shuffle Power Ups - This will change which monitors are which. For instance ring monitors could now be electric shields and electric shields could become speed shoes. This will be consistent throughout the seed, so if you identify what monitor types are shuffled with which then you can plan your routes on later levels around this knowledge. By default the monitor types in the shuffle include: 10 Rings, Blue Shield, Bubble Shield, Fire Shield, Electric Shield, Invincibility, Speed Shoes, Extra Life, Eggman Box, Blue Ring, and Character Switch. That's 11 monitor types that are shuffled, in mania mode only 10 different types appear, so that means one of the 11 won't appear in the seed. 

Add Swaps (Select this if doing Encore) - This setting was added since Mode Select is not longer in the GUI. This just helps make sure the correct number of boxes are chosen from for Encore by adding the Character Switch into the shuffle.

Include Random and Super Boxes in Power Up Shuffle - 'Shuffle Power Ups' must be checked for this option to be available, only one of 'Include Random and Super Boxes in Power Up Shuffle', 'Make All Power Ups Random Boxes' or 'Get a Load of This!!!!' mayb be checked at a time. This adds two more monitor types to the shuffle, so they have the potential to appear in a run but again it's 10 monitor types with now 13 possible options. 

Make All Power Ups Random Boxes - 'Shuffle Power Ups' must be checked for this option to be available, only one of 'Include Random and Super Boxes in Power Up Shuffle', 'Make All Power Ups Random Boxes' or 'Get a Load of This!!!!' mayb be checked at a time. For the truly zanny experience. This makes all monitors the '?' that you may have seen in multiplayer, it bestows a completely random power up when you break it open.

Get A Load of This!!!!! - HaHaHa!!! Let's see if you can make it through this Sonic!

Random Music - This shuffles the music files for all unique tracks in the game. This includes all 26 unique act tracks (Mirage Saloon 1 Knuckles and Angel Island Zone add 2 to the normal 24 stages) and the three unique boss tracks (Metal Sonic, Final Boss, and Egg Reverie). Similar to the base game the same music will play on Green Hill Act 1 whether it's the Mania or Encore version. This also adds randomized boss music. Per boss atempt the game selects one of four boss music files tied to the level's data file. For most stages these tracks are the mini boss, Eggman 1, Eggman 2, and Hard Boiled Heavy boss tracks. Bosses with unique music will have other unique tracks shuffled into their slots. Egg Reverie is still kept with it's own music. 

Allow Repeat - This essentially removes the shuffle for the unique tracks in the game when doing "Random Music". Allowing the same unique music tracks to appear throughout the game. 

Randomize Boss HP - *This defaults to a low and high range of 1-16, this is the recommended setting but have fun breaking the game with some loopsided numbers if you choose* This simply randomizes the boss hit point count. There is some logic for this. Certain bosses that had non-standard HP totals in the base game do some extra math to bring their HP more in line with what you expect: standard bosses that took 8 hits in the base game will use the range displayed here, minibosses take the random number from the range and multiply by 75%, the final boss doubles whatever number it randomizes, the Green Hill Zone 1 boss divides the number it randomizes in two and applies it to both targets, multi form bosses use percents for each form or phase that make sense with how many hits the form or phase took relative to it's total HP, other non-standard bosses have randmoized HP values multiplied by values relative to other bosses. Hard Boiled Heavy will always take 3 or less hits, the boss of Metallic Madness Act 2 Minions use a random value for how many hits they all take and will spawn a random number of minions but it will always be 8 or fewer, etc. . There are lots of other little behavior differences between bosses, so experiement, find out, and have fun. 

Level Layouts in the Shuffle - This setting lets the player toggle between all levels being Mania Mode levels or Encore Mode levels.

Write Random Game to RAM - Once all settings are set click the Random Game button. If you change settings after clicking the button please do so again. The application doesn't write the necessary values to memory until this button is clicked. The random game uses a random seed. If you don't supply a random seed, a number between 1 and 999999999, then the application will auto generate one and place it in the seed number box. The seed allows for games with the same number and options to have identical results, this lets games be shared for things like races. If you would like a new seed then earse what is in the random game text box and a new one will genreate when random game is clicked again. *Note: This writes random game setting to RAM, you do not want to click the 'Write Custom Game to RAM' after this, that will overwrite your random game.*

New Seed - The replaces the current seed in the seed textbox and randomizes the game again. This saves clicks when rolling a new seed.

Custom Game
=======================================================================================================
For custome games you can use the arrows to add or remove values to the level order with the lef and right arrow icons. The custom games logic uses the level amount in the 'Custom Level Order' list box to determine the level count. The characters are assigned to the same level that they share an index number with from their list box. If no primary character is assigned to a level it defaults to Sonic, if no Secondary Character is assigned to a level it defaults to 'No Character'. You also have the option to pick an ending. Once all options are set to your liking click the 'Write Custom Game to Ram'. This option will set the necessary values to make the custom game playable in game. If you change any settings make sure to click 'Write Custom Game to Ram' again.

Known Issues
=======================================================================================================
-The issues mentioned above with save files. The game seems to have trouble understanding some things 
	if you try to load saved files that were created while using this application. Also worth 
	mentioning the way sequencing is done on this there could be other issues with trying to load 
	existing files. This is why 'No Save' is recommended.
	
-Only in Press Garden Act 2, the monitors will still show their default images when frozen in ice, if Power Up Shuffle is on. If you break the ice you will see the correct monitor image. This is obviously an issue with the game having specific assest for monitors frozen in ice.
	
-It has been reported that the randomizer will not work if background pausing is disabled in Sonic Mania. Make sure background pausing is enabled.
