# Function Reference

## mti_armoury_vehicles_mutt_fnc_adjustPlow

**Description:** Shows dialog to adjust the shovels of the plow.  

**Arguments:**
- `_vehicle` - Vehicle
- `_side` = 0: left / 1: right

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_adjustPlow;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_buildTrenchPFH

**Description:** PFH to handle trench building with the plow  

**Arguments:**
- `_vehicle` - The vehicle

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_buildTrenchPFH;
(end)

```

**Author:** Mokka 

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

## mti_armoury_vehicles_mutt_fnc_changeTrenchType

**Description:** Shows a select menu to change the type of trench to dig  

**Arguments:**
- `_vehicle` - Vehicle to show type selection for

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_changeTrenchType;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_deminePFH

**Description:** Detonates nearby mines while the plow of the MUTT-L is lowered  

**Arguments:**
- `_vehicle` - The MUTT-L

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_deminePFH;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_getCommander

**Description:** Helper function to return the MUTT's commander since the commander turret is implemented as a cargo turret.  

**Arguments:**
- `_vehicle` - The vehicle to return the commander of

**Return Value:** Commander of _vehicle, or objNull if commander seat empty  

**Example:**
```

(begin example)
[vehicle player] call mti_armoury_vehicles_mutt_fnc_getCommander;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_handleEpeContactStart

**Description:** Handle plow physx collision events.  

**Arguments:**
- `_vehicle` - object with attached handler (Object)
- `_object` - object which is colliding with object1 (Object)
- `_selection` 1 - selection of object1 which is colliding - not in use at this moment, empty string is always returned (String)
- `_selection` 2 - selection of object2 which is colliding - not in use at this moment, empty string is always returned (String)
- `_force` - force of collision (Number)
- `_reactVect` - impact reaction force vector (Array)
- `_worldPos` - point of impact in world coordinates (PositionWorld)

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_handleEpeContactStart;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_handleExplosion

**Description:** Handles explosion events while the plow is down.  

**Arguments:**
- `_vehicle` - object the event handler is assigned to (Object)
- `_damage` - damage inflicted to the object (Number)
- `_source` - may be objNull in some cases (Object)

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_handleExplosion;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_handleScrollWheel

**Description:** Handles scroll wheel for plow adjustments  

**Arguments:**
- `_scroll` - Scroll amount

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_handleScrollWheel;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_initVehicle

**Description:** Takes care of initialising some values and scripted functionality on the MUTT.  

**Arguments:**
- `_vehicle` - The MUTT

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_armoury_vehicles_mutt_fnc_initVehicle;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_isCrew

**Description:** Checks whether given unit is a crew member of the MUTT  

**Arguments:**
- `_vehicle` - Vehicle
- `_unit` - Unit

**Return Value:** isCrew?  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_isCrew;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_mapOnDrawEH

**Description:** Handles the map during onDraw events.  

**Arguments:**
- `_mapControl` - The map control in question

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_armoury_vehicles_mutt_fnc_mapOnDrawEH;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_rotatePlowVertical

**Description:** Handles setting plow vertical rotation  

**Arguments:**
- `_vehicle` - Vehicle to rotate plow on
- `_state` - State, being -1: lower / 0: level / 1: raise

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_armoury_vehicles_mutt_fnc_rotatePlowVertical;
(end)

```

**Author:** Mokka 

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

## mti_armoury_vehicles_mutt_fnc_trenchModFunc

**Description:** Modifier func to include currently selected trench type in action name  

**Arguments:**
- `_target` - Target
- `_player` - Player
- `_params` - Action params
- `_actionData` - Action data

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_armoury_vehicles_mutt_fnc_trenchModFunc;
(end)

```

**Author:** Mokka 

## mti_armoury_vehicles_mutt_fnc_updateInfoDisplay

**Description:** Updates the info display of the MUTT  

**Arguments:**
- `_vehicle` - The MUTT vehicle in question
- `_infoDisplay` - The info display reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_armoury_vehicles_mutt_fnc_updateInfoDisplay;
(end)

```

**Author:** Mokka 

