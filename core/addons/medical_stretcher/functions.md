# Function Reference

## mti_medical_stretcher_fnc_canDeploy

**Description:** Checks if unit can deploy stretcher.  

**Arguments:**
- `_player` - Player

**Return Value:** canDeploy?  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_canDeploy;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_canEjectPatient

**Description:** Checks whether player can eject patient from the stretcher.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_canEjectPatient;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_canLoadViV

**Description:** Checks whether stretcher can be loaded into a nearby vehicle via ViV.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_canLoadViV;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_canMove

**Description:** Checks whether stretcher can be moved by player.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_canMove;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_deploy

**Description:** Deploys stretcher from folded inventory object.  

**Arguments:**
- `_player` - Player
- `_item` - Item to deploy

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_deploy;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_ejectPatient

**Description:** Ejects patient from the stretcher.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_ejectPatient;
(end)

```

**Author:** Mokka 

## mti_drones_fnc_getAssembleActions

**Description:** Returns child actions for stretcher assembly based on current inventory.  

**Arguments:**
- `_player` - Player unit

**Return Value:** assembleActions  

**Example:**
```

(begin example)
[ace_player] call mti_drones_fnc_getAssembleActions;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_handleScrollWheel

**Description:** Handles height adjustment for the stretcher.  

**Arguments:**
- `_scroll` - Scroll amount

**Return Value:** handled?  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_handleScrollWheel;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_initStretcher

**Description:** Handles init for the stretcher vehicle. Sets up the alert system for patients.  

**Arguments:**
- `_stretcher` - The stretcher object

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_initStretcher;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_loadViV

**Description:** Loads stretcher into nearby vehicle via ViV.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_loadViV;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_move

**Description:** Handles moving/beingMoved the stretcher  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher
- `_type` - Type of move action, one of: CONST_PUSH, CONST_PULL, CONST_ADJUST

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_move;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_movePFH

**Description:** PFH to check if moving stretcher should be aborted  

**Arguments:**
- `_args` - PFH args
- `_handle` - PFH handle

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_movePFH;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_packUp

**Description:** Pack up the stretcher into its folded variant.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_packUp;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_stopMoving

**Description:** Handles detaching the stretcher and resetting variable after moving completed.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_stopMoving;
(end)

```

**Author:** Mokka 

## mti_medical_stretcher_fnc_unloadViV

**Description:** Unloads stretcher from vehicle via ViV.  

**Arguments:**
- `_player` - Player
- `_stretcher` - Stretcher

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_stretcher_fnc_unloadViV;
(end)

```

**Author:** Mokka 

