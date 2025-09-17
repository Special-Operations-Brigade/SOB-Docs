# Function Reference

## fnc_ace_doEscortCaptive.inc.sqf

No documentation available.

## fnc_ace_handleAnimChangedHandcuffed.inc.sqf

No documentation available.

## fnc_ace_handleEffects.inc.sqf

No documentation available.

## mti_common_fnc_canChangeStance

**Description:** Checks whether player can change stance on given captive. Based on ace_captives_canRemoveHandcuffs  

**Arguments:**
- `_player` - Player unit
- `_target` - Target unit
- `_stance` - Stance to check for

**Return Value:** canChangeStance?  

**Example:**
```

(begin example)
[player,cursorTarget,1] call mti_common_fnc_canChangeStance;
(end)

```

**Author:** PabstMirror, modified by Mokka 

## fnc_canNotifyReinsert.sqf

No documentation available.

## mti_common_fnc_canSpotUnit

**Description:** Checks to see if Unit B can see Unit A  

**Arguments:**
- unitA - Unit that is being "Looked" for
- unitB - Unit that is "Looking"

**Return Value:** canBeSeen? - If Unit A  can be seen by Unit B  

**Example:**
```

(begin example)
[ace_player, enemyUnit] call mti_common_fnc_canSpotUnit;
(end)

```

**Author:** Arcanist & Mokka 

## fnc_changeSpeakVolume.sqf

No documentation available.

## mti_common_fnc_changeStance

**Description:** Changes stance of given captive unit  

**Arguments:**
- `_player` - Player unit
- `_target` - Target unit
- `_stance` - Stance to set

**Return Value:** canChangeStance?  

**Example:**
```

(begin example)
[player,cursorTarget,1] call mti_common_fnc_changeStance;
(end)

```

**Author:** Mokka 

## mti_common_fnc_clamp

**Description:** Clamps given numerical value between min and max.  

**Arguments:**
- `_value` - Value to clamp
- `_min` - Min value (inclusive)
- `_max` - Max Value (inclusive)

**Return Value:** Clamped value  

**Example:**
```

(begin example)
[1.2, 0, 1] call mti_common_fnc_clamp;
(end)

```

**Author:** Mokka 

## mti_common_fnc_command_defaultMarkers

**Description:** Handles defaultMarkers chat command.  

**Arguments:**
- Nothing

**Return Value:** Nothing  

**Example:**
```

(begin example)
[] call mti_common_fnc_command_defaultMarkers;
(end)

```

**Author:** Mokka 

## mti_common_fnc_defaultMarkers

**Description:** Creates default map markers at given position  

**Arguments:**
- `_pos` - Position at which to create default marker array

**Return Value:** Created markers  

**Example:**
```

(begin example)
[position ace_player] call mti_common_fnc_defaultMarkers;
(end)

```

**Author:** Mokka 

## mti_common_fnc_dumpConfig

**Description:** Dump (parts of the) config to clipboard and dumps them to file. Based on ConfigDumpFileIO by Denis Usenko, released under MIT License: https://github.com/pennyworth12345/ConfigDumpFileIO  REQUIRES (!) having the ConfigDumpFileIO extension loaded manually, it is not included in the mod release!  

**Arguments:**
- `_config` - The root config to dump
- `_includeInheritedPropertiesFlag` - If true, will include all inherited properties

**Return Value:** None  

**Example:**
```

(begin example)
[configFile >> "CfgVehicles", false] call mti_common_fnc_dumpConfig;
(end)

```

**Author:** Denis Usenko, modified by Mokka */  /* ORIGINAL HEADER BELOW */  // dumpConfig.sqf // Copyright (c) 2010 Denis Usenko, DenVdmj@gmail.com // MIT-style license // // Modified by Pennyworth to write to file using ConfigDumpFileIO extension.  /* ====================================================================================== Dump config to the clipboard: [config HNDL, bool IncludeInheritedPropertiesFlag] call mti_common_fnc_dumpConfig This example put section CfgVehicles on the clipboard: [configFile >> "CfgVehicles"] call mti_common_fnc_dumpConfig This example will put on the clipboard class "RscDisplayMokTech IndustriesdeUnit", all classes will contain all heritable properties, so you get a full and self-sufficient class, independent from the other classes. [configFile >> "RscDisplayMokTech IndustriesdeUnit", true] call mti_common_fnc_dumpConfig More examples: [configFile >> "RscTitle", true] call mti_common_fnc_dumpConfig [configFile >> "RscEdit", true] call mti_common_fnc_dumpConfig [configFile >> "RscToolbox", true] call mti_common_fnc_dumpConfig Warning: don't attempt to get a large classes with switched on parameter "IncludeInheritedPropertiesFlag", eg don't do so: [configFile, true] call mti_common_fnc_dumpConfig Dump the entire config, it can take over ten seconds: [configFile] call mti_common_fnc_dumpConfig ====================================================================================== 

## mti_common_fnc_emergencyBeacon

**Description:** Activates an emergency beacon with the given unit's name, kept alive for the given duration  

**Arguments:**
- `_name` - Name of the unit
- `_pos` - Position of the unit
- `_duration` - Duration to keep alive
- `_id` - Usually netid of the unit

**Return Value:** Success?  

**Example:**
```

(begin example)
[name player,position player, 240] call mti_common_fnc_emergencyBeacon;
(end)

```

**Author:** Mokka 

## mti_common_fnc_fuzzyPos

**Description:** Returns a fuzzy position for a given start pos.  

**Arguments:**
- `_pos` - Original (accurate) position
- `_radius` - Radius of the fuzzy area

**Return Value:** canChangeStance?  

**Example:**
```

(begin example)
[player,cursorTarget,1] call mti_common_fnc_fuzzyPos;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getAllUnitTraits

**Description:** Gets all relevant traits of the unit.  

**Arguments:**
- `_unit` - Unit to get traits for

**Return Value:** All relevant traits of the unit  

**Example:**
```

(begin example)
[player] call mti_common_fnc_getAllUnitTraits;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getBiology

**Description:** Wrapper function for ls_common_fnc_getBiology.  

**Arguments:**
- See ls_common_fnc_getBiology

**Return Value:** ls_common_fnc_getBiology  

**Example:**
```

(begin example)
[ace_player] call mti_common_fnc_getBiology;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getConfigOfItem

**Description:** Helper function that attempts to find and return the config path of a given item  

**Arguments:**
- `_className` - Class name to look up

**Return Value:** All unit types in order  

**Example:**
```

(begin example)
["B_Kitbag_rgr"] call mti_common_fnc_getConfigOfItem;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getGroupUnits

**Description:** Returns ordered list of all units in a given CfgGroups entry  

**Arguments:**
- `_groupPath` - Path to the CfgGroups entry

**Return Value:** All unit types in order  

**Example:**
```

(begin example)
[(configFile >> "CfgGroups" >> "East" >> "mti_factions_cis" >> "Battledroids" >> "mti_factions_cis_InfTeam")] call mti_common_fnc_getGroupUnits;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getItemWeight

**Description:** Returns mass of item.  

**Arguments:**
- `_className` - Class name of the item's mass to turn

**Return Value:** item mass  

**Example:**
```

(begin example)
["B_Kitbag_rgr"] call mti_common_fnc_getItemWeight;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getMarkerColours

**Description:** Returns all marker colours in pretty format for ZEN dialog.  

**Arguments:**
- None

**Return Value:** All marker types in format [class name, pretty name array]  

**Example:**
```

(begin example)
[] call mti_common_fnc_getMarkerColours;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getMarkerTypes

**Description:** Returns all marker types in pretty format for ZEN dialog.  

**Arguments:**
- None

**Return Value:** All marker types in format [class name, pretty name array]  

**Example:**
```

(begin example)
[] call mti_common_fnc_getMarkerTypes;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getResistances

**Description:** Returns resistances of the given unit (type)  

**Arguments:**
- `_unit` - Unit object or class name to return resistances for

**Return Value:** resistances  

**Example:**
```

(begin example)
[player] call mti_common_fnc_getResistances;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getUnitTrait

**Description:** Gets a given unit's trait.  

**Arguments:**
- `_unit` - Unit to get traits for
- `_trait` - Trait to check for

**Return Value:** If unit has that given trait  

**Example:**
```

(begin example)
[player, "Pilot"] call mti_common_fnc_getUnitTrait;
(end)

```

**Author:** Mokka 

## mti_common_fnc_getVehicleInventory

**Description:** Returns the entire vehicle inventory in format [[item, amount],...].  

**Arguments:**
- `_vehicle` - Vehicle to return inventory for

**Return Value:** canChangeStance?  

**Example:**
```

(begin example)
[cursorTarget] call mti_common_fnc_getVehicleInventory;
(end)

```

**Author:** Mokka 

## mti_common_fnc_grabGroundHolderData

**Description:** Internal helper function to grab item data for the creation of ground holders.  

**Arguments:**
- `_searchPrefix` - Prefix to use for searching

**Return Value:** groundHolderData  

**Example:**
```

(begin example)
["mti_armoury"] call mti_common_fnc_grabGroundHolderData;
(end)

```

**Author:** Mokka 

## mti_common_fnc_grabLoadOrder

**Description:** Internal helper function for assembling loadorder addons.  

**Arguments:**
- `_searchPrefix` - Prefix to use for searching addons

**Return Value:** loadOrder (JSON)  

**Example:**
```

(begin example)
["mti"] call mti_common_fnc_grabLoadOrder;
(end)

```

**Author:** Mokka 

## mti_common_fnc_grabRequiredAddons

**Description:** Builds requiredAddons for addons that have a prefix matched using given searchPrefix.  

**Arguments:**
- `_searchPrefix` - Used to filter addons

**Return Value:** requiredAddons in JSON hashmap, sorted by addon  

**Example:**
```

(begin example)
["mti"] call mti_common_fnc_grabRequiredAddons;
(end)

```

**Author:** Mokka 

## mti_common_fnc_guidedProjectile

**Description:** Spawns a guided projectile. Implementation based on Webknight's guided projectile function.  

**Arguments:**
- `_instigator` - The unit "firing" the projectile
- `_startPos` - Start position of the projectile
- `_class` - Class name of projectile in CfgAmmo
- `_target` - The target object
- `_speed` - Initial speed of the projectile
- `_destroyTarget` - If true, _target will be reliably destroyed using setDamage 1
- `_localOffset` - Local offset for target position
- `_minDistanceToTarget` - Min. distance to the target that the projectile will self-detonate
- `_instigatorOffset` - Offset from the shooter's perspective

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_common_fnc_guidedProjectile;
(end)

```

**Author:** Mokka 

## mti_common_fnc_hasItemProperty

**Description:** Checks if given unit has at least one item with the given config property set to 1 in their inventory.  

**Arguments:**
- `_unit` - Unit to check
- `_property` - Config property to check for
- `_includeWeapons` - Optional, include weapons in check? Default: false

**Return Value:** hasItemProperty?  

**Example:**
```

(begin example)
[ace_player, "mti_common_myProperty"] call mti_common_fnc_hasItemProperty;
(end)

```

**Author:** Mokka 

## mti_common_fnc_hideFace

**Description:** Handles hiding the face if necessary.  

**Arguments:**
- `_unit` - Unit to check
- `_newLoadout` - New loadout (unused)
- `_oldLoadout` - Old loadout (unused)

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_common_fnc_hideFace;
(end)

```

**Author:** Mokka 

## mti_common_fnc_hitpointToBodypart

**Description:** Converts hitpoint to bodypart  

**Arguments:**
- `_hitpoint` - Hitpoint selection array

**Return Value:** ACE Body part  

**Example:**
```

(begin example)
["spine2"] call mti_common_fnc_hitpointToBodypart;
(end)

```

**Author:** Mokka 

## mti_common_fnc_initPlayer

**Description:** Initializes the player.  

**Arguments:**
- `_unit` - Player to init
- `_groupVal` - Unit's Group

**Return Value:** None  

**Example:**
```

(begin example)
[player, 1] call mti_common_fnc_initPlayer;
(end)

```

**Author:** Mokka 

## mti_common_fnc_isCQC

**Description:** Checks whether given unit is an EOD.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** isDemo?  

**Example:**
```

(begin example)
[player] call mti_common_fnc_isCQC;
(end)

```

**Author:** Mokka 

## mti_common_fnc_isDemo

**Description:** Checks whether given unit is an EOD.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** isDemo?  

**Example:**
```

(begin example)
[player] call mti_common_fnc_isDemo;
(end)

```

**Author:** Mokka 

## mti_common_fnc_lockDoors

**Description:** Locks all or specific doors in the given building.  

**Arguments:**
- `_building` - Building the doors of which to lock, must inherit from class "house_f"
- `_doors` - Array of numbers indicating which doors to lock OR true to lock all doors

**Return Value:** None  

**Example:**
```

(begin example)
[this, true] call mti_common_fnc_lockDoors;
(end)

```

**Author:** Mokka 

## mti_common_fnc_onLoadoutLoad

**Description:** Verifies the given loadout in regards to weight limits.  

**Arguments:**
- `_loadout` - Loadout being loaded
- `_name` - Name of the loadout

**Return Value:** None  

**Example:**
```

(begin example)
[this, true] call mti_common_fnc_onLoadoutLoad;
(end)

```

**Author:** Mokka 

## fnc_parseSide.sqf

No documentation available.

## mti_common_fnc_registerTeleporter

**Description:** Registers a teleporter. Needs to be executed globally!  ["mti_common_registerTeleporter", [tp1, "Base", false]] call CBA_fnc_globalEventJIP;  

**Arguments:**
- `_object` - The object serving as the teleporter
- `_name` - The name of the teleporter, displayed on the selection
- `_oneWay` - Set to true if teleporter should not show up as a destination

**Return Value:** None  

**Example:**
```

(begin example)
[tp1, "Base", false] call mti_common_fnc_registerTeleporter;
(end)

```

**Author:** Mokka 

## fnc_reinsertNotif.sqf

No documentation available.

## mti_common_fnc_setUnitTrait

**Description:** Sets a unit's traits within the MokTech Industries Trait System.  

**Arguments:**
- `_unit` - Unit to set traits for
- `_trait` - The trait to set
- `_value` - Which value to set the trait as (NUMBER or BOOLEAN)
- `_setExclusive` - Removes all other exclusive traits, default: false
- `_notify` - Notify other admins/Zeus of the perm setting?

**Return Value:** None  

**Example:**
```

(begin example)
[this, "pilot", true] call mti_common_fnc_initPlayer;
(end)

```

**Author:** Mokka 

## mti_common_fnc_showCountdown

**Description:** Displays a countdown of the given duration on the player's screen.  

**Arguments:**
- `_duration` - Duration in seconds

**Return Value:** None  

**Example:**
```

(begin example)
[120] call mti_common_fnc_showCountdown;
(end)

```

**Author:** Mokka 

## mti_common_fnc_swapBackpacks

**Description:** Swaps the character's backpacks. If only equipped with one Backpack, keybind will put that backpack to the front (or back, depending on).  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
call mti_common_fnc_swapBackpacks;
(end)

```

**Author:** Mokka 

## mti_common_fnc_updateRespawn

**Description:** Updates respawn position  

**Arguments:**
- `_pos` 

**Return Value:** None  

**Example:**
```

(begin example)
[position player] call mti_common_fnc_updateRespawn;
(end)

```

**Author:** Mokka 

## mti_common_fnc_useTeleporter

**Description:** Opens the teleporter dialog.  

**Arguments:**
- `_object` - The object that the dialog is being opened from

**Return Value:** None  

**Example:**
```

(begin example)
[cursorTarget] call mti_common_fnc_useTeleporter;
(end)

```

**Author:** Mokka 

