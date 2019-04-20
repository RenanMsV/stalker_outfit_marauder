    ----------------------
    -- File: Outfit Marauder
    -- Author: Shoker
    -- CoM visuals table: ziken
    -- CoM script adaptation: Dimeyne
    -- Ñíÿòèå áðîíè ñ òðóïîâ.
    -- CoC 1.4.22 adaptation: RenanMsV
    ----------------------

The addon makes it possible to pick up armors and helmets when looting NPC corpses.The state of things depends on the faction and rank of the deceased.
For Call of Chernobyl 1.4.22

How to config this mod (change drop chance etc...):

Edit the gamedata/configs/outfit_marauder.ltx
The default drop chance is 25%.

Item conditions based by the NPC rank (novice, experienced, legend) are enabled by default. So experienced stalker will drop outfits with a better condition. You can disable it in the config.

```ini
[global_config]
	dropchance = 25 ;outfit and helmet drop chance in % (from 0 to 100)
	outfit_Condition_Based_On_Rank = true ;if so experienced stalkers will drop outfits with a better condition
	debugMessages = false ;debug messages (for developers)
[outfit_condition] ;default armor durability in % (from 0 to 100)
	min = 10
	max = 45
[helmet_condition] ;default helmet durability in % (from 0 to 100)
	min = 10
	max = 35
[rank_condition_table] ;setup here the durability based on the npc rank, will not work if outfit_Condition_Based_On_Rank not enabled. 1 = default by config, 2 = 2x more
	novice = 1
	trainee = 1.1
	experienced = 1.2
	professional = 1.3
	veteran = 1.4
	expert = 1.5
	master = 1.6
	legend = 1.7
```

How to install :

Copy and replace this mod's gamedata folder into your game's gamedata folder.
For this mod to work with mods that change the gamedata/configs/misc/death_generic.ltx file you need to add those lines to this file (in the [keep_items] section):

```ini
novice_outfit = true
banditmerc_outfit = true
trenchcoat_outfit = true
bandit_novice_outfit = true
merc_outfit = true
helm_respirator = true
svoboda_light_outfit = true
dolg_exo_outfit = true
scientific_outfit = true
cs_light_novice_outfit = true
cs_medium_outfit = true
helm_hardhat = true
helm_m40 = true
svoboda_exo_outfit = true
dolg_scientific_outfit = true
stalker_outfit = true
ecolog_outfit_orange = true
dolg_outfit = true
exo_outfit = true
monolith_outfit = true
merc_exo_outfit = true
cs_light_outfit = true
svoboda_scientific_outfit = true
dolg_novice_outfit = true
cs_novice_outfit = true
military_outfit = true
ecolog_outfit_green = true
monolith_scientific_outfit = true
dolg_heavy_outfit = true
helm_battle = true
military_exo_outfit = true
bandit_exo_outfit = true
svoboda_novice_outfit = true
monolith_exo_outfit = true
merc_scientific_outfit = true
specops_outfit = true
cs_heavy_outfit = true
ecolog_guard_outfit = true
helm_tactic = true
svoboda_heavy_outfit = true
cs_exo_outfit = true
```

How to add new outfits:

To setup new outfits open the outfit_marauder.script with any text editor, and include values in the visuals variable. Example below:
  - stalker_visual_name = {"armor_name", "helmet_name"}
  - The helmet is not required.
  - Also if its a new outfit or helmet (non vanilla) you need to add to the gamedata/configs/misc/death_generic.ltx so the game will keep this item in the npc inventory after death. If you dont the game will randomly remove those outfits or helmets from npc's inventory. Making this mod kinda useless.

No new game required.

Changelog:

You can now fully config the mod, such as drop chance, item conditions, debug enabled, etc...

New debug option (for developers, or for you to test if your configs are correct and if the mod is working).

New outfits based in the Vanilla version 1.4.22. You can add new outfits from mods.
