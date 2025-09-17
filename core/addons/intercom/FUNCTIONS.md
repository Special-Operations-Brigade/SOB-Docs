# Function Reference

## mti_intercom_fnc_activate

**Description:** Activates the group intercom.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
call mti_intercom_fnc_activate;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_canActivate

**Description:** Checks whether the group intercom can be activated  

**Return Value:** canActivate?  

**Example:**
```

(begin example)
call mti_intercom_fnc_canActivate;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_canChangeVolume

**Description:** Checks whether the intercoms volume can be changed in the given direction (up or down).  

**Arguments:**
- `_direction` - If 'true', checks for increasing volume, 'false' checks for decreasing volume

**Return Value:** canChangeVolume?  

**Example:**
```

(begin example)
[true] call mti_intercom_fnc_canChangeVolume;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_canDeactivate

**Description:** Checks whether the group intercom can be deactivated  

**Return Value:** canDeactivate?  

**Example:**
```

(begin example)
call mti_intercom_fnc_canDeactivate;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_canSwitchChannel

**Description:** Checks, whether the group intercom can be switched to the given channel.  

**Arguments:**
- `_channel` - Channel to check against

**Return Value:** canSwitchChannel?  

**Example:**
```

(begin example)
[1] call mti_intercom_fnc_canSwitchChannel;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_changeVolume

**Description:** Changes the intercom volume in the given direction.  

**Arguments:**
- `_direction` - If 'true', increases volume, if 'false' decreases it

**Return Value:** None  

**Example:**
```

(begin example)
[true] call mti_intercom_fnc_changeVolume;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_deactivate

**Description:** Deactivates the group intercom.  

**Arguments:**
- `_keepAlive` - Whether connection should be "kept alive" and reestablished when back in range

**Return Value:** None  

**Example:**
```

(begin example)
[false] call mti_intercom_fnc_deactivate;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_hasIntercom

**Description:** Checks whether the player has a group intercom.  

**Arguments:**
- None

**Return Value:** hasIntercom?  

**Example:**
```

(begin example)
call mti_intercom_fnc_hasIntercom;
(end)

```

**Author:** Mokka */  if (!isNil QGVAR(hasIntercomCache)) exitWith { GVAR(hasIntercomCache) };  if !(GVAR(systemEnabled)) exitWith { false };  /* // go through all unique items and check if mti_intercom_hasIntercom is set for any of them private _items = [ACE_Player] call ace_common_fnc_uniqueItems; _items pushBack (headgear ACE_Player); _items pushBack (uniform ACE_Player); _items pushBack (vest ACE_Player); _items pushBack (goggles ACE_Player); _items append (assignedItems ACE_Player);  private _uniqueItems = [_items] call ace_common_fnc_uniqueElements;  private _iCount = { (GET_BOOL(configFile >> "CfgWeapons" >> _x >> QGVAR(hasIntercom))) } count _uniqueItems;  // need to check backpack separately since it's a CfgVehicles entry _iCount = _iCount + GET_NUMBER(configFile >> "CfgVehicles" >> (backpack ACE_Player) >> QGVAR(hasIntercom), 0);  private _hasIntercom = _iCount > 0; 

## mti_intercom_fnc_isInRange

**Description:** Checks whether player is in range of any other group members for intercom purposes  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_intercom_fnc_isInRange;
(end)

```

**Author:** Mokka 

## mti_intercom_fnc_switchChannel

**Description:** Switches the group intercom to the selected channel.  

**Arguments:**
- `_channel` - Intercom channel to switch to

**Return Value:** None  

**Example:**
```

(begin example)
[0] call mti_intercom_fnc_switchChannel;
(end)

```

**Author:** Mokka 

## fnc_tfar_onSpeakVolumeChanged.inc.sqf

No documentation available.

## tfar_fnc_preparePositionCoordinates

**Description:** Prepares the position coordinates of the passed unit. Based on: https://github.com/michail-nikolaev/task-force-arma-3-radio/blob/master/addons/core/functions/fnc_preparePositionCoordinates.sqf Will be removed once Saborknight's External Intercom PR gets merged.  

**Arguments:**
- `_unit` - Unit to prepare position coordinates for
- `_nearPlayer` - Is unit near player?
- `_unitName` - Name of the unit

**Return Value:** prepared Data  

**Example:**
```

(begin example)
[params] call tfar_fnc_preparePositionCoordinates;
(end)

```

**Author:** NKey, modified by Mokka 

## TFAR_fnc_vehicleId

**Description:** Returns a string with information about the player vehicle, used at the plugin side. Based on: https://github.com/michail-nikolaev/task-force-arma-3-radio/blob/master/addons/core/functions/fnc_vehicleId.sqf  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** [NetworkID, Turned Out]  

**Example:**
```

(begin example)
_vehId = [player] call TFAR_fnc_vehicleId;
(end)

```

**Author:** NKey, modified by Mokka 

