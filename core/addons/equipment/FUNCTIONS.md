# Function Reference

## mti_equipment_fnc_canEquipKnife

**Description:** Checks whether given unit can equip a knife.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canEquipKnife?  

**Example:**
```

(begin example)
[ace_player] call mti_equipment_fnc_canEquipKnife;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_canExtendBlades

**Description:** Checks whether given unit can extend blades.  

**Arguments:**
- `_unit` - Unit

**Return Value:** canExtend  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_canExtendBlades;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_canPlaceFlag

**Description:** Checks whether given player is able to place flag of given type.  

**Arguments:**
- `_unit` - Unit to check
- `_item` - Type of flag

**Return Value:** canPlaceFlag?  

**Example:**
```

(begin example)
[ace_player,"mti_flags_red"] call mti_equipment_fnc_canPlaceFlag;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_canRepairRadio

**Description:** Checks whether given player is able to repair a fried radio  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canRepairRadio?  

**Example:**
```

(begin example)
[ace_player] call mti_equipment_fnc_canRepairRadio;
(end)

```

**Author:** Arcanist 

## mti_equipment_fnc_canRetractBlades

**Description:** Checks whether given unit can retract blades.  

**Arguments:**
- `_unit` - Unit

**Return Value:** canRetract  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_canRetractBlades;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_eatMRE

**Description:** Makes unit eat food yummy :)  

**Arguments:**
- `_unit` - Unit to eat food

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_eatMRE;
(end)

Arcanist
```

## mti_equipment_fnc_extendBlades

**Description:** Extends blades of given unit.  

**Arguments:**
- `_unit` - Unit

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_extendBlades;
(end)

```

**Author:** Mokka 

## fnc_handleBeforeTangent.sqf

No documentation available.

## mti_equipment_fnc_handleRespawn

**Description:** Handles player respawning, resets some values.  

**Arguments:**
- `_unit` - The unit that respawned

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_player] call mti_equipment_fnc_handleRespawn;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_handleScrollWheel

**Description:** Handles changing height when placing the marker flags.  

**Arguments:**
- `_scrollAmount` - Scroll amount

**Return Value:** Handled?  

**Example:**
```

(begin example)
[] call mti_equipment_fnc_handleScrollWheel;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_hasBlades

**Description:** Checks whether given unit has access to compatible blades.  

**Arguments:**
- `_unit` - Unit

**Return Value:** hasBlades?  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_hasBlades;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_hasKnife

**Description:** Checks whether given unit has access to a clone knife.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasKnife?  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_hasKnife;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_hasMRE

**Description:** Checks whether given unit has any ACE MREs.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasMRE?  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_hasMRE;
(end)

Arcanist
```

## mti_equipment_fnc_hideHelmet

**Description:** Hides currently equipped helmet, nvg and facewear.  

**Arguments:**
- `_unit` - Unit whose items to hide

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_equipment_fnc_hideHelmet;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_nvg_setEffect

**Description:** Sets up the post-processing effect for NVGs (and handles destroying it when disabling NVs).  

**Arguments:**
- `_nv` - true if entering NV, false if exiting it

**Return Value:** None  

**Example:**
```

(begin example)
[true] call mti_equipment_fnc_nvg_setEffect;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_pickUpFlag

**Description:** Handles picking up a flag after it was deployed.  

**Arguments:**
- `_flag` - The flag being picked up
- `_unit` - The unit picking the flag up
- `_args` - Action args

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_equipment_fnc_pickUpFlag;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_placeFlag

**Description:** Places flag of given type in front of player. Based on ace_marker_flags_fnc_placeFlag.  

**Arguments:**
- `_unit` - Unit placing the flag
- `_item` - Type of flag to place

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_equipment_fnc_placeFlag;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_repairRadio

**Description:** Repairs the unit's fried radios  

**Arguments:**
- `_unit` - Unit to check

**Example:**
```

(begin example)
[ace_player] call mti_equipment_fnc_repairRadio;
(end)

```

**Author:** Arcanist 

## mti_equipment_fnc_retractBlades

**Description:** Retracts blades of given unit.  

**Arguments:**
- `_unit` - Unit

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_equipment_fnc_retractBlades;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_toggleKnife

**Description:** Toggles the unit's knife (if available).  

**Arguments:**
- `_unit` - Unit whose knife to toggle
- `_state` - True to pull knife, false to put it away

**Return Value:** None  

**Example:**
```

(begin example)
[player,true] call mti_equipment_fnc_toggleKnife;
(end)

```

**Author:** Mokka 

## mti_equipment_fnc_unhideHelmet

**Description:** Unhides previously hidden helmet, NVG and facewear  

**Arguments:**
- `_unit` - Unit whose helmet to unhide

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_equipment_fnc_unhideHelmet;
(end)

```

**Author:** Mokka 

