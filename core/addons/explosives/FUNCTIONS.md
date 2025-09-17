# Function Reference

## mti_explosives_fnc_addAdvSetupActions

**Description:** Adds explosives actions for the advanced explosive setup.  

**Arguments:**
- `_unit` - The unit to add the action for
- `_detonator` - The clacker that is used, not used

**Return Value:** Explosives actions  

**Example:**
```

(begin example)
[player, "MTI_Clacker"] call mti_explosives_fnc_addAdvSetupActions;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_addAdvSetupChildren

**Description:** Adds children actions for the advanced explosive setup.  

**Arguments:**
- `_unit` - The unit to add the action for
- `_range` - The max. range that the detonator works at
- `_explosive` - Array: Explosive Object, Fuse Time
- `_detonator` - The clacker that is used

**Return Value:** Children actions  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_addAdvSetupChildren;
(end)

```

**Author:** Mokka */  params ["_unit", "_range", "_explosive", "_detonator"]; TRACE_4("params",_unit,_range,_explosive,_detonator);  private _config = configFile >> "CfgMagazines" >> (_explosive select 3);  private _children = [];  // timer private _canUseTimer = GET_BOOL(_config >> QGVAR(timer)); //TRACE_1("timer",_canUseTimer);  if (_canUseTimer) then { private _timerAction = [ "timer", "Timer", "", // icontodo {(_this select 2) call FUNC(advSetupTimer)}, {!([GVAR(advSetup_hash_armed),((_this select 2) select 2) select 0,false] call CBA_fnc_hashGet)}, {}, [_unit,_range,_explosive,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_timerAction, [], _unit]; };  // prox. sensor private _canUseProx = GET_BOOL(_config >> QGVAR(proximitySensor)); //TRACE_1("prox",_canUseProx);  if (_canUseProx) then { private _proxAction = [ "prox", "Proximity Sensor", "", // icontodo {[QGVAR(advSetup_mag_prox),(_this select 2)] call FUNC(advSetupPlace)}, {!([GVAR(advSetup_hash_armed),((_this select 2) select 2) select 0,false] call CBA_fnc_hashGet)}, {}, [_unit,_range,_explosive,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_proxAction, [], _unit]; };  // ir sensor private _canUseIR = GET_BOOL(_config >> QGVAR(IRSensor)); //TRACE_1("ir",_canUseIR);  if (_canUseIR) then { private _irAction = [ "ir", "IR Sensor", "", // icontodo {[QGVAR(advSetup_mag_ir),(_this select 2)] call FUNC(advSetupPlace)}, {!([GVAR(advSetup_hash_armed),((_this select 2) select 2) select 0,false] call CBA_fnc_hashGet)}, {}, [_unit,_range,_explosive,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_irAction, [], _unit]; };  // tripwire private _canUseTripwire = GET_BOOL(_config >> QGVAR(tripwire)); //TRACE_1("tripwire",_canUseTripwire);  if (_canUseTripwire) then { private _tripwireAction = [ "tripwire", "Tripwire", "", // icontodo {[QGVAR(advSetup_mag_tripwire),(_this select 2)] call FUNC(advSetupPlace)}, {!([GVAR(advSetup_hash_armed),((_this select 2) select 2) select 0,false] call CBA_fnc_hashGet)}, {}, [_unit,_range,_explosive,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_tripwireAction, [], _unit]; };  // disconnect adv. setup  private _disconnectAction = [ "disconnect", "Disconnect Adv. Setup Component", "", // icontodo {(_this select 2) call FUNC(advSetupDisconnect)}, {([GVAR(advSetup_hash_armed),((_this select 2) select 2) select 0,false] call CBA_fnc_hashGet)}, {}, [_unit,_range,_explosive,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_disconnectAction, [], _unit];  TRACE_1("return",_children);  _children  /* private _action = [ format ["Explosive_%1", _forEachIndex], _x select 2, getText(_item >> "picture"), {}, {true}, {(_this select 2) call FUNC(addAdvSetupChildren)}, [_unit,_range,_x,_detonator] ] call ace_interact_menu_fnc_createAction;  _children pushBack [_action, [], _unit]; 

## mti_explosives_fnc_advSetupCanUse

**Description:** Checks whether given unit can use the advanced setup system.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canUse?  

**Example:**
```

(begin example)
[_player] call mti_explosives_fnc_advSetupCanUse;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_advSetupDisconnect

**Description:** Disconnects a previously set advSetup component.  

**Arguments:**
- `_unit` - unused
- `_range` - Max. range
- `_explosive` - The explosive object
- `_detonator` - unused

**Return Value:** None  

**Example:**
```

(begin example)
[this] call mti_explosives_fnc_advSetupDisconnect;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_advSetupInit

**Description:** Handles initialization of an adv. setup dummy explosive.  

**Arguments:**
- `_object` - The explosive place object

**Return Value:** None  

**Example:**
```

(begin example)
[_this] call mti_explosives_fnc_advSetupInit;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_advSetupPlace

**Description:** Handles placing a remote trigger "dummy" for advanced setup.  

**Arguments:**
- `_class` - The class name of the dummy explosive to use
- `_args` - Action args

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_advSetupPlace;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_advSetupTimer

**Description:** Sets up a timer for an already placed explosive. Based on ACE_explosives_fnc_openTimerUI: https://github.com/acemod/ACE3/blob/master/addons/explosives/functions/fnc_openTimerUI.sqf  

**Arguments:**
- `_unit` - unused
- `_range` - Max. range
- `_explosive` - The explosive object
- `_detonator` - unused

**Return Value:** None  

**Example:**
```

(begin example)
[this] call mti_explosives_fnc_advSetupTimer;
(end)

```

**Author:** mharis001, modified by Mokka 

## mti_explosives_fnc_breachTarget

**Description:** Breaches the nearest applicable target.  

**Arguments:**
- `_anchor` - The anchor the breaching charge is attached to
- `_target` - The target object to (attempt to) breach

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorObject] call mti_explosives_fnc_breachTarget;
(end)

```

**Author:** Mokka */  params ["_anchor", "_target"];  // house/door if (_target isKindOf "HOUSE") exitWith { private _startPos = (getPosASL _anchor) vectorAdd [0, 0, 0]; private _endPos = _startPos vectorAdd (vectorUp _anchor);  private _intersections = [_target, "GEOM"] intersect [ASLToAGL _startPos, ASLToAGL _endPos]; private _door = toLower ((_intersections select 0) select 0);  if (isNil "_door") exitWith {};  if ((_door find "glass") isNotEqualTo -1) then { _door = [10, _target, _door] call ace_interaction_fnc_getGlassDoor; };  private _animName = ""; private _animNames = animationNames _target;  if (({_x isEqualTo _door} count _animNames) > 0) then { _animName = _door + ""; };  if (({_x isEqualTo (_door + "_rot")} count _animNames) > 0) then { _animName = _door + "_rot"; };  if (_animName isEqualTo "") exitWith {};  _target animate [_animName, 1, true];  // todo: "break" the door and stop it from being closed again /* // find door number, base it on this? private _cfgNameSplit = (configName _actionPath) splitString "_";  if ((count _cfgNameSplit) == 2) then { private _doorNumber = parseNumber (_cfgNameSplit select 1);  if (_doorNumber > 0) then { private _doorString = format ["bis_disabled_door_%1", _doorNumber]; }; }; 

## mti_explosives_fnc_grenadeThrown

**Description:** Handles magnetic attaching when a compatible grenade has been thrown.  

**Arguments:**
- `_grenade` - The grenade projectile

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_grenadeThrown;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_hasMED

**Description:** Checks whether given unit has an MED-compatible magazine  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** hasMED?  

**Example:**
```

(begin example)
[] call mti_explosives_fnc_hasMED;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_initAAMine

**Description:** Initializes a newly deployed AA Mine.  

**Arguments:**
- `_pos` - Position to create the AA Mine at
- `_side` - Side the AA Mine is friendly to

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_initAAMine;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_initBreachingCharge

**Description:** Initializes a breaching charges after it was put down.  

**Arguments:**
- `_charge` - The planted charge

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_explosives_fnc_initBreachingCharge;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_initCrewBuster

**Description:** Initializes crew buster ammo and sets attached vehicles up for crew destruction upon detonation.  

**Arguments:**
- `_explosive` - The explosive that was placed down
- `_dir` - Unused
- `_pitch` - Unused
- `_unit` - The unit that placed the explosive

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_initCrewBuster;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_initDP3

**Description:** Initializes the DP-3 and sets attached vehicles up for destruction upon detonation.  

**Arguments:**
- `_explosive` - The explosive that was placed down
- `_dir` - Unused
- `_pitch` - Unused
- `_unit` - The unit that placed the explosive

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_initDP3;
(end)

```

**Author:** Mokka 

## fnc_placeExplosive.sqf

No documentation available.

## mti_explosives_fnc_setPosition

**Description:** Handles setting up the pitch and orientation of the breaching charge.  

**Arguments:**
- `_charge` - The explosive that was put down

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_explosives_fnc_setPosition;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_setTimerMED

**Description:** Sets the explosion delay for the MED. Based on ACE_explosives_fnc_openTimerUI: https://github.com/acemod/ACE3/blob/master/addons/explosives/functions/fnc_openTimerUI.sqf  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[this] call mti_explosives_fnc_setTimerMED;
(end)

```

**Author:** mharis001, modified by Mokka 

## mti_explosives_fnc_spawnSecondaries

**Description:** Helper function to spawn secondary explosions in a circle or sphere around given position.  

**Arguments:**
- `_pos` - Position to spawn around
- `_radius` - Array consisting of radius min and radius max in which secondaries should spawn
- `_sphere` - Whether secondaries should be spawn in a sphere (true) or a circle (false)
- `_count` - Array consisting of min. count and max. count of secondaries
- `_delay` - Array consisting of min. delay and max. delay before spawning secondaries
- `_types` - Array consisting of classnames of secondary explosions to spawn

**Return Value:** None  

**Example:**
```

(begin example)
[[45343,11723,30],[5,20],true,[1,5],[0.1,2],["SmallSecondary"]] call mti_explosives_fnc_spawnSecondaries;
(end)

```

**Author:** Mokka 

## mti_explosives_fnc_thrownRemoteSetup

**Description:** Handles connecting a thrown remote explosive to the unit's clacker.  

**Arguments:**
- `_unit` - The unit to connect the explosive to
- `_grenade` - The thrown projectile

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_explosives_fnc_thrownRemoteSetup;
(end)

```

**Author:** Mokka 

