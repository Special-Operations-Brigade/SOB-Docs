# Function Reference

## mti_zeus_fnc_activateDispenser

**Description:** Handles the activation of droid dispensers  

**Arguments:**
- `_dispenser` - The dispenser

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_activateDispenser;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_deactivateDispenser

**Description:** Handles the deactivation of droid dispensers  

**Arguments:**
- `_dispenser` - The dispenser

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_deactivateDispenser;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_editDispenser

**Description:** Handles changing the droid dispenser's settings using ZEN Dialog.  

**Arguments:**
- `_dispenser` - The dispenser we want to edit

**Return Value:** None  

**Example:**
```

(begin example)
[_hoveredEntity] call mti_zeus_fnc_editDispenser;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_setCaptive

**Description:** Sets the selected units as captive with the given restraint type  

**Arguments:**
- `_objects` - Selected objects
- `_type` - Class-name of the type of restraint used

**Return Value:** None  

**Example:**
```

(begin example)
[[player],"MTI_CableTie_Medium"] call mti_zeus_fnc_setCaptive;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_ui_addFortifyComposition

**Description:** UI to add a fortify composition to an object.  

**Arguments:**
- `_object` - Object

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_ui_addFortifyComposition;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_ui_addFortifyPreset

**Description:** UI to add a fortify preset to an object.  

**Arguments:**
- `_object` - Object

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_ui_addFortifyPreset;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_ui_emergencyBeacon

**Description:** Wrapper to trigger an emergency beacon.  

**Arguments:**
- `_pos` - Position
- `_object` - Object (null if none)

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_ui_emergencyBeacon;
(end)

```

**Author:** Mokka 

## mti_zeus_fnc_ui_registerTeleporter

**Description:** Wrapper to register a teleporter.  

**Arguments:**
- `_object` - Object

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_zeus_fnc_ui_registerTeleporter;
(end)

```

**Author:** Mokka 

