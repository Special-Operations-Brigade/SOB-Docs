# Function Reference

## mti_aircraft_fnc_activateSquadShield

**Description:** Handles activation of the squad shield.  

**Arguments:**
- `_vehicle` - Vehicle that activated the squad shield
- `_player` - Player that activated the squad shield

**Return Value:** None  

**Example:**
```

(begin example)
[vehicle player, player] call mti_aircraft_fnc_activateSquadShield;
(end)

```

**Author:** Arcanist 

## fnc_canDeployLAGShield.sqf

No documentation available.

## mti_aircraft_fnc_canSelectSkin

**Description:** Checks whether player can select skin of current aircraft.  

**Arguments:**
- `_target` - Aircraft
- `_player` - The player to check for
- `_actionParams` - Unused

**Return Value:** canSelectSkin?  

**Example:**
```

(begin example)
[LAAT2, player] call mti_aircraft_fnc_canSelectSkin;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_canService

**Description:** Checks whether given aircraft can be serviced by player.  

**Arguments:**
- `_target` - Aircraft
- `_player` - The player to check for
- `_actionParams` - Unused

**Return Value:** canService?  

**Example:**
```

(begin example)
[LAAT2, player] call mti_aircraft_fnc_canService;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_canToggleCloaking

**Description:** Checks whether player can toggle cloaking of current aircraft.  

**Arguments:**
- `_aircraft` - Aircraft
- `_player` - The player to check for
- `_state` - Whether cloaking should be turned on/off

**Return Value:** canToggleCloaking?  

**Example:**
```

(begin example)
[LAAT2, player, true] call mti_aircraft_fnc_canToggleCloaking;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cm_canChangeColour

**Description:** Checks, whether player can change CM colour on current aircraft.  

**Arguments:**
- `_vehicle` - The vehicle to check for
- `_player` - The player to check for

**Return Value:** canChangeColour?  

**Example:**
```

(begin example)
[vehicle player, player] call mti_aircraft_fnc_cm_canChangeColour;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cm_changeColour

**Description:** Opens the selection for the desired CM colour.  

**Arguments:**
- `_vehicle` - The vehicle whose CM colour to change
- `_player` - The player changing the colour

**Return Value:** None  

**Example:**
```

(begin example)
[vehicle player, player] call mti_aircraft_fnc_cm_changeColour;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_attach

**Description:** Attaches the passed unit to the given aircraft's CPAS.  

**Arguments:**
- `_unit` - Unit to attach
- `_aircraft` - Aircraft to attach to
- `_pylon` - The pylon to attach the unit to

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_aircraft_fnc_cpas_attach;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_canAttach

**Description:** Checks whether unit can attach self to given pylon on passed aircraft  

**Arguments:**
- `_unit` - Unit to check attaching for
- `_aircraft` - Aircraft to check attaching to
- `_pylon` - The pylon to check attaching the unit to

**Return Value:** canAttach?  

**Example:**
```

(begin example)
[player,cursorTarget,1] call mti_aircraft_fnc_cpas_canAttach;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_detach

**Description:** Detaches the passed unit from the aircraft's CPAS.  

**Arguments:**
- `_unit` - Unit to detach

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_aircraft_fnc_cpas_detach;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_handleFiredLocal

**Description:** Eventhandler to re-attach the rig to the projectile after it was fired  

**Arguments:**
- `_unit` - Unit that's attached to CPAS
- `_aircraft` - Aircraft with CPAS
- `_pylon` - Pylon that unit is attached to
- `_projectile` - The projectile object to re-attach to
- `_automaticDetach` - Detach automatically?

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_aircraft_fnc_cpas_handleFiredLocal;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_isEquipped

**Description:** Checks whether given aircraft is equipped with a CPAS, returns all pylons that are equipped with CPAS.  

**Arguments:**
- `_aircraft` - Aircraft to check
- `_checkAmmo` - If true, pylons must have ammo to count as "equipped"

**Return Value:** pylon indices where CPAS is equipped  

**Example:**
```

(begin example)
[vehicle player] call mti_aircraft_fnc_cpas_isEquipped;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_cpas_onFired

**Description:** Handles re-attaching the CPAS rig to the projectile after dropping.  

**Arguments:**
- `_aircraft` - the unit that fired
- `_weapon` - weapon used
- `_muzzle` - muzzle used
- `_mode` - mode used
- `_ammo` - ammo used
- `_magazine` - magazines used
- `_projectile` - projectile object

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_aircraft_fnc_cpas_onFired;
(end)

```

**Author:** Mokka 

## fnc_handleBowArrow.sqf

No documentation available.

## fnc_handleTrigger.sqf

No documentation available.

## mti_aircraft_fnc_laatc_load

**Description:** Loads nearby vehicles/objects into LAAT/c  

**Arguments:**
- `_aircraft` - The LAAT/c to attempt to load things into

**Return Value:** None  

**Example:**
```

(begin example)
[cursorTarget] call mti_aircraft_fnc_laatc_load;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_laatc_unload

**Description:** Unloads vehicles from the LAAT/c.  

**Arguments:**
- `_aircraft` - The LAAT/c

**Return Value:** None  

**Example:**
```

(begin example)
[cursorTarget] call mti_aircraft_fnc_laatc_unload;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_onFired_SmokeLauncher

**Description:** Handles deploying a smoke screen after the smoke launcher CM has been activated. Based on BIS_fnc_effectFiredSmokeLauncher.  

**Arguments:**
- `_vehicle` - The vehicle whose smoke launcher has been activated
- `_unit` - The unit that activated the smoke launcher

**Return Value:** None  

**Example:**
```

(begin example)
[vehicle player, player] call mti_aircraft_fnc_onFired_SmokeLauncher;
(end)

```

**Author:** Mokka 

## fnc_scalplekill.sqf

No documentation available.

## mti_aircraft_fnc_selectSkin

**Description:** Opens skin selector for given aircraft.  

**Arguments:**
- `_aircraft` - Aircraft
- `_player` - The player selecting the skin
- `_actionParams` - Unused

**Return Value:** None  

**Example:**
```

(begin example)
[LAAT2, player] call mti_aircraft_fnc_selectSkin;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_service

**Description:** Services the given aircraft.  

**Arguments:**
- `_target` - Aircraft
- `_player` - The player servicing
- `_actionParams` - Unused

**Return Value:** None  

**Example:**
```

(begin example)
[LAAT2, player] call mti_aircraft_fnc_service;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_setServicingKart

**Description:** Sets the given vehicle up as a servicing kart that can be used to repair, refuel and rearm aircraft.  

**Arguments:**
- `_veh` - The vehicle to set up
- `_repairOnly` 

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_aircraft_fnc_setServicingKart;
(end)

```

**Author:** Mokka 

## mti_aircraft_fnc_toggleCloaking

**Description:** Toggles cloaking device of given aircraft on/off.  

**Arguments:**
- `_aircraft` - Aircraft
- `_player` - Player
- `_state` - Whether cloaking should be turned on/off

**Return Value:** None  

**Example:**
```

(begin example)
[LAAT2, player, true] call mti_aircraft_fnc_toggleCloaking;
(end)

```

**Author:** Mokka 

