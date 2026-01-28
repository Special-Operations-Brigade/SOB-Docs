# Function Reference

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

