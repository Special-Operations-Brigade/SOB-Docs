# Function Reference

## mti_common_fnc_initArsenal

**Description:** Initializes a container as an MokTech Industries Arsenal.  

**Arguments:**
- `_object` - Player to init
- `_type` - Arsenal Type, any valid class in mti_arsenal_whitelists

**Return Value:** None  

**Example:**
```

(begin example)
[this, "Command"] call mti_common_fnc_initArsenal;
(end)

```

**Author:** Mokka 

## mti_common_fnc_initDefaultLoadouts

**Description:** Adds default loadouts to ACE arsenals.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
call mti_common_fnc_initDefaultLoadouts;
(end)

```

**Author:** Mokka 

## mti_arsenal_fnc_insertArmouryActions

**Description:** Returns child actions for the armoury system.  

**Arguments:**
- `_object` - Target object
- `_player` - Player interacting

**Return Value:** All marker types in format [class name, pretty name array]  

**Example:**
```

(begin example)
[] call mti_arsenal_fnc_insertArmouryActions;
(end)

```

**Author:** Mokka 

## mti_arsenal_fnc_parseLists

**Description:** PreInit function that parses the config and compiles the arsenal whitelists.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_arsenal_fnc_parseLists;
(end)

```

**Author:** Mokka 

## mti_common_fnc_postInit

**Description:** Post-init stuff to make preset arsenals.  

**Arguments:**
- `_object` 

**Return Value:** None  

**Example:**
```

(begin example)
[cursorObject] call mti_common_fnc_postInit;
(end)

```

**Author:** Mokka 

## mti_arsenal_fnc_setArmoury

**Description:** Sets up the given object as a  

**Arguments:**
- `_object` - Player to init

**Return Value:** None  

**Example:**
```

(begin example)
[this] call mti_arsenal_fnc_setArmoury;
(end)

```

**Author:** Mokka 

