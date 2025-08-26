# Function Reference

## mti_katarnOS_fnc_activateBeacon

**Description:** Activates the emergency beacon of the given unit.  

**Arguments:**
- `_unit` - Unit activating the beacon
- `_target` - Target unit in possession of the beacon

**Return Value:** Success?  

**Example:**
```

(begin example)
[player,cursorTarget] call mti_katarnOS_fnc_activateBeacon;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_activateDispenser

**Description:** Activates the backpack-integrated mine dispenser.  

**Arguments:**
- `_unit` - Unit whose dispenser to activate
- `_type` - 0 = mines, 1 = caltrops

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_activateDispenser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_activateRepulsorBlast

**Description:** Activates the Repulsor Blast  

**Arguments:**
- `_unit` - client

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_katarnOS_fnc_activateRepulsorBlast;
(end)

```

**Author:** Chimera 

## mti_katarnOS_fnc_activateSquadShield

**Description:** Handles activation of the squad shield.  

**Arguments:**
- `_unit` - Unit that activated the squad shield

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_activateSquadShield;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_activateTaser

**Description:** Handles activation of the ST-91 wrist-place stun device.  

**Arguments:**
- `_unit` - Unit whose taser to activate

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_activateTaser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_canActivateBeacon

**Description:** Checks if given unit can activate the beacon of the given target  

**Arguments:**
- `_unit` - Unit attempting to activate beacon
- `_target` - Target unit in possession of the beacon

**Return Value:** canActivateBeacon?  

**Example:**
```

(begin example)
[ACE_Player,cursorTarget] call mti_katarnOS_fnc_canActivateBeacon;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_canActivateRepulsorBlast

**Description:** Checks if unit has repulsor loaded  

**Arguments:**
- `_unit` - client

**Return Value:** Bool  

**Example:**
```

(begin example)
[] call mti_katarnOS_fnc_canActivateRepulsor;
(end)

```

**Author:** Chimera 

## mti_katarnOS_fnc_canActivateSquadShield

**Description:** Checks if given unit can activate the squad shield of the given target  

**Arguments:**
- `_unit` - Unit attempting to activate squad shield
- `_target` - Target unit in possession of the squad shield

**Return Value:** canActivateSquadShield?  

**Example:**
```

(begin example)
[ACE_Player,cursorTarget] call mti_katarnOS_fnc_canActivateSquadShield;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_canActivateTaser

**Description:** Returns whether given unit can activate taser. Does NOT check if unit actually has a taser.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canActivateTaser?  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_canActivateTaser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_canReloadRepulsorBlast

**Description:** Checks if client can reload the repulsor blast  

**Arguments:**
- `_unit` - Client

**Return Value:** Bool  

**Example:**
```

(begin example)
[] call mti_katarnOS_fnc_canReloadRepulsorBlast;
(end)

```

**Author:** Chimera 

## mti_katarnOS_fnc_canReloadTaser

**Description:** Returns whether the given unit can reload the taser. Does NOT check if unit actually has a taser.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canReloadTaser?  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_canReloadTaser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_canUseDispenser

**Description:** Checks if the given unit can use the integrated mine dispenser.  

**Arguments:**
- `_unit` - Unit to check
- `_type` - 0 = mines, 1 = caltrops

**Return Value:** canUseDispenser?  

**Example:**
```

(begin example)
[ACE_player, 0] call mti_katarnOS_fnc_canUseDispenser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_getID

**Description:** Returns the unit's commando ID.  

**Arguments:**
- `_unit` - Unit

**Return Value:** commandoID  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_getID;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_handlePanelSwitch

**Description:** Takes care of skipping the custom panels if HUD projector is not equipped.  

**Arguments:**
- `_isLeft` - is left side? if false, side is right
- `_isPrev` - is first action a previous one?

**Return Value:** None  

**Example:**
```

(begin example)
[true, false] call mti_katarnOS_fnc_handlePanelSwitch;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasBackpack

**Description:** Checks if given unit has equipped KatarnOS compatible backpack.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasBackpack?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasBackpack;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasBeacon

**Description:** Checks if given unit has equipped KatarnOS compatible Beacon.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasBeacon?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasBeacon;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasHelmet

**Description:** Checks if given unit has equipped KatarnOS compatible Helmet.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasHelmet?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasHelmet;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasHUD

**Description:** Checks if given unit has equipped KatarnOS compatible HUD projector.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasHUD?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasHUD;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasNV

**Description:** Checks if given unit has equipped KatarnOS compatible NV.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasNV?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasNV;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasOS

**Description:** Checks if given unit has equipped KatarnOS compatible OS equipment.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasOS?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasOS;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasSquadShield

**Description:** Returns whether given unit has access to the backpack-deployed squad shields.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasSquadShield?  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_hasSquadShield;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasSuit

**Description:** Checks if given unit has equipped KatarnOS compatible Suit.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasSuit?  

**Example:**
```

(begin example)
[ACE_Player] call mti_katarnOS_fnc_hasSuit;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasTaser

**Description:** Returns true if given unit has a wrist_plate tazer equipped.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasTaser?  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_hasTaser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_hasTRX

**Description:** Checks whether given unit as access to the integrated TRX-200 Mine Detection System.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasTRX?  

**Example:**
```

(begin example)
[ACE_player] call mti_katarnOS_fnc_hasTRX;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_HUD_Status_PFEH

**Description:** Per-frame Handler that takes care of updating the status HUD.  

**Arguments:**
- `_args` - Passed arguments
- `_handle` - PFH handle

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_katarnOS_fnc_HUD_Status_PFEH;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_HUD_Team_PFEH

**Description:** Per-frame Handler that takes care of updating the team HUD.  

**Arguments:**
- `_args` - Passed arguments
- `_handle` - PFH handle

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_katarnOS_fnc_HUD_Team_PFEH;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_onVisionModeChanged

**Description:** Handles entering nightvision.  

**Arguments:**
- `_unit` - Player unit
- `_visionMode` - The new vision mode

**Return Value:** None  

**Example:**
```

(begin example)
[player, 1] call mti_katarnOS_fnc_onVisionModeChanged;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_reloadRepulsorBlast

**Description:** Description...  

**Arguments:**
- `_` - expl.

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_katarnOS_fnc_reloadRepulsorBlast;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_reloadTaser

**Description:** Reloads the taser.  

**Arguments:**
- `_unit` - Unit to reload taser for
- `_force` - If taser should be forcefully reloaded (skip sanity checks)

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_reloadTaser;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_resetSystems

**Description:** Resets systems.  

**Arguments:**
- `_unit` - Unit to reset systems for

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_resetSystems;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_taser_getTarget

**Description:** Returns closest available target for the taser (or objNull is none found)  

**Arguments:**
- `_unit` - Unit to check for

**Return Value:** Nearest target (or objNull if none found)  

**Example:**
```

(begin example)
[player] call mti_katarnOS_fnc_taser_getTarget;
(end)

```

**Author:** Mokka 

## mti_katarnOS_fnc_toggleLowlight

**Description:** Toggles low light vision mode  

**Arguments:**
- `_unit` - The unit to set low light mode for
- `_enable` - If low light mode is to be enabled or disabled

**Return Value:** None  

**Example:**
```

(begin example)
[player,true] call mti_katarnOS_fnc_toggleLowlight;
(end)

```

**Author:** Mokka 

