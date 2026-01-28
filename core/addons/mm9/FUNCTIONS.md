# Function Reference

## mti_mm9_fnc_attackProfile_mm9

**Description:** Attack profile for the MM-9.  

**Arguments:**
- Missile Guidance Arg

**Return Value:** Missile AIM posASL  

**Example:**
```

(begin example)
[] call mti_mm9_fnc_attackProfile_mm9;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_findTargetMM9

**Description:** Attempts to find a suitable target for the MM9.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_mm9_fnc_findTargetMM9;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_fireMM9

**Description:** Handles firing the MM9 Rocket System.  

**Arguments:**
- `_unit` - Unit whose MM9 to fire
- `_target` - The target

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorTarget] call mti_mm9_fnc_fireMM9;
(end)

Mokka
```

## mti_mm9_fnc_hasMM9

**Description:** Checks whether given unit has access to the MM9 Rocket System.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasMM9?  

**Example:**
```

(begin example)
[player] call mti_mm9_fnc_hasMM9;
(end)

Mokka
```

## mti_mm9_fnc_hasMM9Rocket

**Description:** Checks whether given unit has a suitable MM9 Rocket in their inventory.  

**Arguments:**
- `_unit` - Unit to check
- `_type` - Type of rocket to check for, optional

**Return Value:** hasMM9Rocket?  

**Example:**
```

(begin example)
[player] call mti_mm9_fnc_hasMM9Rocket;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_insertReloadActions

**Description:** Insert reload actions for each type of  

**Arguments:**
- `_player` - Player unit

**Return Value:** reloadActions  

**Example:**
```

(begin example)
[ace_player] call mti_mm9_fnc_insertReloadActions;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_mm9_onFiredNav

**Description:** Sets up variables for the MM-9 missile guidance navigation type.  

**Arguments:**
- Missile Guidance Arg

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_mm9_fnc_mm9_onFiredNav;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_navigationType_mm9

**Description:** Navigation function for the MM-9.  

**Arguments:**
- Guidance Arg Array

**Return Value:** Commanded acceleration normal to LOS in world space  

**Example:**
```

(begin example)
[] call mti_mm9_fnc_navigationType_mm9;
(end)

```

**Author:** tcvm, Mokka 

## mti_mm9_fnc_prepareMM9

**Description:** Prepares the MM9 Rocket System, initiating the targetting sequence and adding action to "Fire".  

**Arguments:**
- `_unit` - Unit whose MM9 to prepare

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_mm9_fnc_prepareMM9;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_reloadMM9

**Description:** Reload MM9 rocket system.  

**Arguments:**
- `_unit` - Unit whose MM9 to reload
- `_type` - Rocket type, optional

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_mm9_fnc_reloadMM9;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_seekerType_mm9

**Description:** Seeker Type function for ace_missileguidance for the mm9  

**Arguments:**
- Guidance Arg Array

**Return Value:** Missile Aim PosASL  

**Example:**
```

(begin example)
[...] call mti_mm9_fnc_seekerType_mm9;
(end)

```

**Author:** Mokka 

## mti_mm9_fnc_unloadMM9

**Description:** Unloads the MM-9 and adds the used reload item back to the unit's inventory.  

**Arguments:**
- `_unit` - Unit

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_mm9_fnc_unloadMM9;
(end)

```

**Author:** Mokka 

