# 7DTD Server Configs
Configuration Changes for 7DTD Server Version 13.6

# Tweaks to items.xml

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
  
# Tweaks to blocks.xml

309: campfire
  * Can now be repaired using up to 5 rockSmall as materials

311: oven
  * Can now be repaired using up to 5 forgedIron
  
349: fridge
  * Can now be repaired using up to 5 forgedIron
  
365: airConditioner
  * Added scrapCable as a harvestable item with a probability of 0.1 to recieve 1
  
840: fridgeTop
  * Can now be repaired using up to 5 forgedIron
  
841: fridgeBottom
  * Can now be repaired using up to 5 forgedIron
  
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
  
# Tweaks to entityclasses.xml

zombiedog
  * cleaned up the extra 'xxx' text after the xml node
  
# Tweaks to recipes.xml

gunPowder
  * count increased from 1 to 2
  
glue
  * count increased from 1 to 2
  * added additional recipe that requires boneShive instead of femur for ingredient
  
gasCan
  * reduced grainAlcohol required from 6 to 3
  
# Tweaks to loot.xml

lootgroup: junk
  * increased ductTape count from 1,3 to 1,6
  
lootgroup: undamagedCar
  * new lootgroup that is similar to the automotive+tools+junk lootgroup
  * junk probability set to 0.5
  * junk count set to 1,2
  * automotive probability set to 0.45
  
lootcontainer 100: "Undamaged Cars"
  * new lootcontainer that makes use of the undamagedCar lootgroup
  * spawns 1 instance of the lootgroup in a 7x4 container
  * takes 4 seconds to open an untouched container
  
# Tweaks to spawning.xml
  
Extended out the '49th' day spawn
  * copied the 49th 'NightHorde' day to every 7 days after, up to the 294th day
  
# Tweaks to buffs.xml

Removed the wellness penalty from getting stunned

# Tweaks to progression.xml

Improved the Athletics skill
  * Added a scaling increase to stamina recovery. Stamina recovery should be twice as effective at skill lvl 100
  * Added a scaling increase to wellness gain. Food that provices wellness should be twice as effective at skill lvl 100
  
Improved the Medicine skill
  * Previously, the Medicine skill had no effects at all
  * Added a scaling increase to hp regeneration. HP should regen at twice the rate at skill lvl 100
