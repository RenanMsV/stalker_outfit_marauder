Help to develop it : https://gitlab.com/RenanMsV/stalker_outfit_marauder

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

How to install :

Copy and replace this mod's gamedata folder into your game's gamedata folder.
For this mod to work with mods that change the gamedata/configs/misc/death_generic.ltx file you need to add those lines to this file (in the [keep_items] section):

novice outfit = true
banditmerc_outfit = true
trenchcoat_brown_outfit = true
bandit_novice_outfit = true
merc_stalker_outfit = true
helm_respirator = true
svoboda_light_outfit = true
dolg_exo_outfit = true
scientific_outfit = true
cs_light_novice_outfit = true
cs_medium_outfit = true
helm_hardhat = true
trenchcoat_outfit = true
helm_m40 = true
svoboda_exo_outfit = true
dolg_scientific_outfit = true
stalker_outfit = true
ecolog_outfit_white = true
merc_outfit = true
ecolog_outfit_orange = true
dolg_outfit = true
exo_outfit = true
m />merc exo_outfit = true
cs_light_outfit = true
svoboda_scientific_outfit = true
dolg_novice_outfit = true
cs_novice_outfit = true
cs_stalker_outfit = true
military_outfit = true
ecolog_outfit_green = true
m />dolg heavy_outfit = true
helm_battle = true
exolight_outfit = true
cs_scientific_outfit = true
commander_outfit = true
bandit_specops_outfit = true
ecolog_outfit_blue = true
military_exo_outfit = true
bandit_exo_outfit = true
svoboda_novice_outfit = true
m />merc_scientific_outfit = true
svoboda_exolight_outfit = true
specops_outfit = true
cs_heavy_outfit = true
ecolog_guard_outfit = true
helm_tactic = true
svoboda_heavy_outfit = true
cs_exo_outfit = true
barmerc_outfit = true
ecolog_outfit_yello = true

How to add new outfits:

To setup new outfits open the outfit_marauder.script with any text editor, and include values in the visuals variable. Example below:
-- stalker_visual_name = {"armor_name", "helmet_name"}
-- The helmet is not required.
-- Also if its a new outfit or helmet (non vanilla) you need to add to the gamedata/configs/misc/death_generic.ltx so the game will keep this item in the npc invemtory after death. If you dont the game will randomly remove those outfits or helmets from npc's inventory. Making this mod kinda usefull.

No new game required.

Changelog:

You can now fully config the mod, such as drop chance, item conditions, debug enabled, etc...

New debug option (for developers, or for you to test if your configs are correct and if the mod is working).

New outfits based in the Vanilla version 1.4.22. You can add new outfits from mods.