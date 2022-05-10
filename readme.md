
# IT266 Quake 2 Mod - KF2 Inspired Wave Survival Mod

1. [Description](#Description)
1. [Deliverables](#Deliverables)
1. [Changes](#Changes)
3. [Testing](#Testing)

## Description
This KF2 inspired mod is a mod in which the player chooses between three unique classes and tries to 
survive for as long as they can agaisnt waves of enemies. From killing enemies, players can earn xp and cash (called dosh in-game),
allowing them to become stronger by earning perks and buying new weapons and armor.

## Deliverables
Below are the deliverables for this mod:
- Enemies Spawn in Waves
- Three classes to choose from (Gunslinger, Demolitionist, Berserker)
- Player earns xp and levels up to unlock perks (3 for each class)
- In-game shop where player can buy ammo, armor, and guns
- Enemies drop currency that players can pick up

## Changes
#### Enemies Spawn in waves (In 20 second intervals, can only spawn next wave if player clears prior wave)
#### Players now pick out of three of the classes to spawn in as (Gunslinger, Demolitionist, Beserker) (Perks detailed in Testing)
##### - Gunslinger has 75 health and 50 shield (Great single-target damage)
##### - Demolitionist has 125 health and 75 shield (Explosive Oriented)
##### - Beserker has 200 health and 100 shield (Tank)
#### Player spawns in on one specific map (q2dm1 "The Edge")
#### Buy menu can be accessed in-game to purchase items (Needs to be keybinded)
#### Money is gathered by killing enemeies and picking up the item "dosh" (Will automatically go to player if not spawned in correctly)
#### Player can level up can unlock perks by killing enemies
#### Help included to assist player with understanding how to play the game

## Testing
Below explains how to test each deliverable:

### Enemies spawn in waves
Launch into the map, wait around 20 seconds and the first wave will begin to spawn. This will occur in intervals of 20 seconds,
but a wave will not spawn on an interval until the player has cleared the prior wave.

### Three classes to choose from (Gunslinger, Demolitionist, Beserker)
On game startup, the player will launch into baseq1, but be redirected to the survival map. Once in, the player should choose their class immidiatly upon load.
They can enter the commandline to choose their class as so:
- class gunslinger
- class demo
- class berserker
These can also be binded to a key, and the config file included already includes the keybinds for choosing classes

### Player earns xp and levels up to unlock perks (3 for each class)
There are three classes, each with three perks that unlock at player levels 5, 10, and 15.
Players earn 10 xp per kill no matter the enemy, and it takes 50 xp to level up each time.
To test the perks, reach level 15 from playing the game or set player level to 15 by typing
this command into the console: 'level 15'. All perks will be active for the respective class chosen.
Below are the perks for each class:
#### Gunslinger (Single-Target Damager Dealer)
- Level 5: 20% chance to not consume ammo when firing
- Level 10: Weapons fire faster (Excluding Chaingun)
- Level 15: For each consecutive hit on an enemy, deal 20% more damage (Stacks up to 10: 3x more damage being done). Resets if damage is done to player
#### Demolitionist (Zones with Explosives)
- Level 5: Player gains resistance to explosive splash damage (Rocket, Grenade Launchers, and Grenades)
- Level 10: Explosive splash damage and range is doubled (Rocket, Grenade Launchers, and Grenades)
- Level 15: Explosive grenades now shoot a spread of rockets (Grenade Launchers, and Grenades)
#### Beserker (Tank)
- Level 5: Shield get converted to health, max health is now increased by max shield
- Level 10: For every kill, the player gains 5 health back
- Level 15: Melee damage taken is reduced by 40% (Can be up to 50% depending on the enemy)

### Ingame shop where player can buy ammo, armor, guns
Make sure to bind the 'buymenu' to a key in the settings menu.
Once in a game, hit the key binded to the buymenu, and the menu to purchase items will popup.
Once opened, the player will be able to scroll down and purchase items from the menu. Works similar to inventory
Hit enter on the item you want, and if you have enough currency, the item will appear in your inventory. You will know an item is purchased if
the dosh counter at the bottom right decreases in count. If you do not have enough dosh, then you cannot buy the items.

### Enemies drop currency that players can pick up
Very simple to test, kill an enemy and the currency will drop. It looks like an armor shard, walk over it and it should notify the player if currencny has been aquired. To double check that you acquired it, you can check the dosh counter on the bottom right of the hud
and see if it increased. Currently, each enemy drops 100 dosh.
