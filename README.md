# 7DTD Server Configs
Configuration Changes for 7DTD Server Version 13.6

## Tweaks to items.xml

20: fireaxe
  * ActionSkillGroup changed from Blade Weapons to Mining Tools
  
52: chainsaw
  * Delay changed from 0.2 to 1.5
  * DamageEntity changed from 16 to 64
  * DamageBonus.wood changed from 10 to 40
  * The above changes makes the chainsaw about 5x more effecient on gas useage
  
53: auger
  * Delay changed from 0.2 to 0.8
  * DamageEntity changed from 16 to 64
  * The above changes makes the auger about 4x more effecient on gas useage
  
245: firstAidBandage
  * Stacknumber changed from 5 to 15
  
310: bandage
  * Stacknumber changed from 5 to 15
  
732: smallEngine
  * VehicleMetersPerLiter changed from 8,12 to 40,60
  * The above changes makes the minibike about 5x more efficient on gas useage
  
1010: Cool Leather Jackets
  * added this new item to allow crafting of leatherDuster by players
  
## Tweaks to blocks.xml

309: campfire
  * Can now be repaired using up to 5 rockSmall as materials

311: oven
  * Can now be repaired using up to 5 forgedIron
  
335: trash_can01
  * Can now be repaired using up to 5 scrapIron (changed from forgedIron)
  * Can now be picked up and moved by mining the block.
  
349: fridge
  * Can now be repaired using up to 5 forgedIron
  
363: poleTop01
  * Can now be repaired using up to 10 wood

365: airConditioner
  * Added scrapCable as a harvestable item with a probability of 0.1 to recieve 1

430: barbedFence
  * Made it possible to pick up
  
517: rebar
  * Removed stray 'xxx' text next to XML node
  
840: fridgeTop
  * Can now be repaired using up to 5 forgedIron
  
841: fridgeBottom
  * Can now be repaired using up to 5 forgedIron
  
921: tubeHalfPoleWoodFull
  * Can now be repaired using up to 10 wood

1453: car03Blue
  * Loot list changed from id 19 to id 100 (see loot.xml changes for more information)
  
1454: car03BlueDamage1
  * Removed cloth from harvestable items to make it the same as other cars.
  * Changed the 'Fall' event from car03BlueDamage2 to car03Damage2

1455: car03Damage2
  * Added scrapCable as a harvestable item with a probability of 0.25 to recieve 1
  
1457: car03RedDamage1
  * Changed the 'Fall' event from car03BlueDamage2 to car03Damage2
  
1459: car03YellowDamage1
  * Changed the 'Fall' event from car03BlueDamage2 to car03Damage2
  
1461: car03WhiteDamage1
  * Changed the 'Fall' event from car03BlueDamage2 to car03Damage2
  
## Tweaks to entityclasses.xml

zombiedog
  * cleaned up the extra 'xxx' text after the xml node
  
## Tweaks to recipes.xml

gunPowder
  * count increased from 1 to 2
  
glue
  * count increased from 1 to 2
  * added additional recipe that requires boneShive instead of femur for ingredient
  
gasCan
  * reduced grainAlcohol required from 6 to 3
  
## Tweaks to loot.xml

lootgroup: junk
  * increased ductTape count from 1,3 to 1,6
  
lootgroup: undamagedCar
  * new lootgroup that is similar to the automotive+tools+junk lootgroup
  * junk probability set to 0.5
  * junk count set to 1,2
  * automotive probability set to 0.45
  
 lootgroup: commonBooks
  * added new item Cool Leather Jackets to the lootgroup
  
lootcontainer 100: "Undamaged Cars"
  * new lootcontainer that makes use of the undamagedCar lootgroup
  * spawns 1 instance of the lootgroup in a 7x4 container
  * takes 4 seconds to open an untouched container
  
## Tweaks to spawning.xml
  
Extended out the '49th' day spawn
  * copied the 49th 'NightHorde' day to every 7 days after, up to the 294th day
  * increased zombie wave size after day 100
  
## Tweaks to buffs.xml

Removed the wellness penalty from getting stunned

## Tweaks to progression.xml

Improved the Athletics skill
  * Added a scaling increase to stamina recovery. Stamina recovery should be twice as effective at skill lvl 100
  * Added a scaling increase to wellness gain. Food that provices wellness should be twice as effective at skill lvl 100
  
Improved the Medicine skill
  * Previously, the Medicine skill had no effects at all
  * Added a scaling increase to hp regeneration. HP should regen at twice the rate at skill lvl 100

# Food Mod
The food mod changes a few recipes to make them make a little more sense. Instead of using jars full of water, some recipes will now require a bowl full of water, either as a cooking tool or as an actual ingredient. Some food will return an empty bowl when eaten. Also, the stews can be canned to creat an oderless version of the food, at the cost of loosing the wellness buff. Eating the canned stew will return the empty can to you, or it can be emptied into a bowl and then warmed up to regain the wellness buff.

## Changes to recipes.xml

bowl
  * changed to be a forge produced item that takes 1 unit_clay to produce each bowl

blueberryPie
  * changed ingredient bottledWater to Bowl of Water

cornBread
  * changed cooking tool to Bowl of Water
  * removed ingredient bottledWater

cornOnTheCob
  * changed cooking tool to Bowl of Water
  * removed ingredient bottledWater

eggboiled
  * changed cooking tool to Bowl of Water
  * removed ingredient bottledWater

boiledMeat
  * changed cooking tool to Bowl of Water
  * removed ingredient bottledWater

vegetableStew
  * changed ingredient bottledWater to Bowl of Water

meatStew
  * changed ingredient bottledWater to Bowl of Water

## New additions to recipes.xml

Bowl of Water
  * created in a campfire
  * requires one Bowl of Murky Water

Canned Meat Stew
  * can be created in a campfire, same as meatStew + 2 canEmpty
  * can be crafted from 1 meatStew and 2 canEmpty
  * both recipes creat 2 items

meatStew
  * new recipe created in the campfire that requires 1 Cold Meat Stew

Cold Meat Stew
  * requires 1 bowl and 2 Canned Meat Stew

Canned Vegetable Stew
  * can be created in a campfire, same as vegetableStew + 2 canEmpty
  * can be crafted from 1 vegetableStew and 2 canEmpty
  * both recipes create 2 items

vegetableStew
  * new recipe created in the campfire that requires 1 Cold Vegetable Stew

Cold Vegetable Stew
  * requires 1 bowl and 2 Canned Vegetable Stew

Mead
  * can be created in a campfire
  * requires 1 cornMeal, 1 bottledWater, and 1 foodHoney
  * requires beaker as a cooking tool

## Changes to items.xml

238: meatStew
  * now creates a bowl when eaten

239: bowl
  * Stacknumber set to 15

234: blueberryPie
  * now creates a bowl when eaten

693: vegetableStew
  * now creates a bowl when eaten

## New additions to items.xml

950: Bowl of Murky Water
  * use a bowl on a source of water to create this item
  * behaves exactly like a bottle of murky water

951: Bowl of Water
  * create in a campfire from a Bowl of Murky Water
  * behaves exactly like a bottle of water

952: Canned Meat Stew
  * provides about half as much health and food as meatStew (because 2 are produced for each 1 meatStew)
  * does not provide wellness
  * does not have a smell

953: Cold Meat Stew
  * exactly the same as meatStew, except it provides no wellness
  * can be converted to meatStew by cooking it on a campfire

954: Canned Vegetable Stew
  * provides about half as much health and food as vegetableStew (because 2 are produced for each 1 vegetableStew)
  * does not provide wellness
  * does not have a smell

955: Cold Vegetable Stew
  * exactly the same as vegetableStew, except it provides no wellness
  * can be converted to vegetableStew by cooking it on a campfire

956: Mead
  * similar effect as drinking beer
  * provides a small amount of wellness

# Farming Mod
The farming modification adds seeds for three existing plants, making them farmable.

## New additions to items.xml

1000: Chrysanthemum Seed<br>
1001: Yucca Seed<br>
1002: Aloe Seed<br>

## New additions to blocks.xml

1600: sproutChrysanthemum<br>
1601: youngChrysanthemum<br>
1602: yuccasprout<br>
1603: yuccayoung<br>
1604: aloesprout<br>
1605: aloeyoung<br>

## New additions to recipes.xml

Chrysanthemum Seed
  * Produces 4 seeds per each Crysanthemum used (yes, that's how the plant is spelled in the game, it's missing the h)

Yucca Seed
  * Produces 2 seeds per each Yucca Plant used

Aloe Seed
  * Produces 2 seeds per each Aloe Plant used
  
# Simplified Training Mod
Some crafting skills create an inventory management nightmare when attempting to craft multiple items to train up the skill. This mod adds five new Training items that can be crafted from the same base materials normally required to train up a skill, but are stackable up to 5000.

## New additions to items.xml

1100: Training: Tool Smithing
1101: Training: Tailoring
1102: Training: Science
1103: Training: Leatherworking
1104: Training: Armor Smithing

## New additions to recipes.xml

Training: Tool Smithing
  * Requires 4 rockSmall, 4 yuccaFibers, and 4 wood
  
Training: Tailoring
  * Requires 10 yuccaFibers
  * Alternately, can be crafted with 10 cloth
  
Training: Science
  * Requires 10 cloth
  
Training: Leatherworking
  * Requires 10 leather
  
Training: Armor Smithing
  * Requires 10 forgedIron and 3 leather