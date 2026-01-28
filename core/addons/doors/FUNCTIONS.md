# Function Reference

## fnc_ace_addHouseActions.inc.sqf

No documentation available.

## mti_doors_fnc_addHouseActions

**Description:** Scans for nearby buildings, and adds actions. Based on ace_interact_menu_fnc_userActions_addHouseActions: (https://github.com/acemod/ACE3/blob/master/addons/interact_menu/functions/fnc_userActions_addHouseActions.sqf)  

**Arguments:**
- `_interactionType` - Interact Menu Type (0 - world, 1 - self)

**Return Value:** None  

**Example:**
```

(begin example)
[0] call mti_doors_fnc_addHouseActions;
(end)

```

**Author:** PabstMirror, Mokka 

## mti_doors_fnc_breakDownAxe

**Description:** Handles axe functionality. Three different functions: "canBreak": returns BOOL if breaking with axe is possible "startBreak": starts the process "finishBreak": on completions, forces the door open  Based on ACE_VehicleLock_fnc_lockpick: (https://github.com/acemod/ACE3/blob/master/addons/vehiclelock/functions/fnc_lockpick.sqf)  

**Arguments:**
- `_unit` - Unit (Player)
- `_building` - Building
- `_helperPos` - Position of Door Helper Object
- `_doorNumber` - Number of the door
- `_memPoint` - Memory point of the door
- `_funcType` - Function Type, see above

**Return Value:** "canLockpick  

**Example:**
```

(begin example)
[ACE_player, ACE_Interaction_Target, 1, _mem, 'canBreak'] call mti_doors_fnc_breakDownAxe;
(end)

```

**Author:** PabstMirror, Mokka 

## mti_doors_fnc_canButtKick

**Description:** Checks, whether the passed _unit can use the "butt kick" action provided by Webknight's IMS.  

**Arguments:**
- `_unit` - Unit (Player)

**Return Value:** canButtKick  

**Example:**
```

(begin example)
[ACE_player] call mti_doors_fnc_canButtKick;
(end)

```

**Author:** PabstMirror, Mokka 

## mti_doors_fnc_canKick

**Description:** Checks, whether the passed _unit can use the "kick" action provided by Webknight's IMS.  

**Arguments:**
- `_unit` - Unit (Player)

**Return Value:** canKick  

**Example:**
```

(begin example)
[ACE_player] call mti_doors_fnc_canKick;
(end)

```

**Author:** PabstMirror, Mokka 

## mti_doors_fnc_getDoorAnim

**Description:** Returns the animationName of the supplied door.  

**Arguments:**
- `_building` - Building the door is in
- `_doorNumber` - Number of the door
- `_memPoint` - Mempoint of the door (unused)

**Return Value:** animationName of door  

**Example:**
```

(begin example)
[ACE_Interaction_Target, 1, ""] call mti_doors_fnc_getDoorAnim;
(end)

```

**Author:** Mokka */  params ["_building", "_doorNumber", "_memPoint"]; TRACE_3("params",_building,_doorNumber,_memPoint);  // sanity checks if (!(_building isKindOf "HOUSE")) exitWith { ERROR("_building is invalid"); ""}; if (_doorNumber <= 0) exitWith {ERROR_1("_doornumber is invalid: %1",_doorNumber); ""};  private _door = format ["door_%1", _doorNumber]; private _door_2 = format ["door%1", _doorNumber];  /* //Check if door is glass because then we need to find the proper location of the door so we can use it if ((_memPoint find "glass") != -1) then { _memPoint = [10, _building, _memPoint] call ace_interaction_fnc_getGlassDoor; }; 

## mti_doors_fnc_getHouseActions

**Description:** Scans the building type and returns memPoints and actions. Based on ace_interact_menu_fnc_userActions_getHouseActions: (https://github.com/acemod/ACE3/blob/master/addons/interact_menu/functions/fnc_userActions_getHouseActions.sqf)  

**Arguments:**
- `_typeOfBuilding` - Building class name

**Return Value:** [[Array of MemPoints], [Array Of Actions]]  

**Example:**
```

(begin example)
["Land_i_House_Big_01_V1_F"] call mti_doors_fnc_getHouseActions;
(end)

```

**Author:** PabstMirror, Mokka 

## mti_doors_fnc_handleButtKickKeyDown

**Description:** Handles key events for sfx_kickButt, to be able to open doors.  

**Arguments:**
- None

**Return Value:** Nothing  

**Example:**
```

(begin example)
[] call mti_doors_fnc_handleButtKickKeyDown;
(end)

```

**Author:** Mokka 

## mti_doors_fnc_handleKickKeyDown

**Description:** Handles key events for WBK_LegPunch, to be able to open doors using the kick.  

**Arguments:**
- None

**Return Value:** Nothing  

**Example:**
```

(begin example)
[] call mti_doors_fnc_handleKickKeyDown;
(end)

```

**Author:** Mokka 

## mti_doors_fnc_lockpick

**Description:** Handles lockpick functionality. Three different functions: "canLockpick": returns BOOL if lockpick is possible "startLockpick": starts the process "finishLockpick": on completions, opens the lock  Mode is one of: 0 - slow 1 - fast  Based on ACE_VehicleLock_fnc_lockpick: (https://github.com/acemod/ACE3/blob/master/addons/vehiclelock/functions/fnc_lockpick.sqf)  

**Arguments:**
- `_unit` - Unit (Player)
- `_building` - Building
- `_helperPos` - Position of Door Helper Object
- `_doorNumber` - Number of the door
- `_funcType` - Function Type, see above
- `_mode` - Lockpick mode, see above

**Return Value:** "canLockpick  

**Example:**
```

(begin example)
[ACE_player, ACE_Interaction_Target, 'canLockpick'] call mti_doors_fnc_lockpick;
(end)

```

**Author:** PabstMirror, Mokka 

