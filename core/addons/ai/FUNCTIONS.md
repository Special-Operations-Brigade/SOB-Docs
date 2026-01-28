# Function Reference

## mti_ai_fnc_3den_populateAO

**Description:** Internal helper function to run populateAI in 3den. Do not call directly unless you know what you're doing!  

**Arguments:**
- N/A

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_ai_fnc_3den_populateAO_3den;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_findSpawnPos

**Description:** Finds a safe position based on the given parameters, using BIS_fnc_randomPos.  White-/Blacklist can be:  Object - trigger String - marker Array - in format [center, radius] or [center, [a, b, angle, rect]] Location - location  

**Arguments:**
- `_whitelist` - Whitelisted areas, if empty the whole map is used
- `_blacklist` - Blacklisted areas, if empty water is blacklisted by default
- `_code` - Custom condition which should return true for current position _this
- `_timeout` - Abort position finding after that many attempts (default: 25)

**Return Value:** :Random safe position that fits the passed parameters or [0,0] if no valid position could be found after _timeout attempts  

**Example:**
```

(begin example)
_pos = [[[[0, 0, 0], 150],[]],["water"]] call mti_ai_fnc_findSpawnPos;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_getFactions

**Description:** Returns available factions for the Populate AO functionality both as class names and as readily compiled display names  

**Arguments:**
- `_force` - (Optional) Set to true to forcefully clear the cache and return a fresh result

**Return Value:** Array of factions, each faction entry has format [side, displayName, className]  

**Example:**
```

(begin example)
[] call mti_ai_fnc_getFactions;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_getRoadWaypoints

**Description:** Helper function to obtain waypoints on roads for the purpose of fnc_populateAO.  

**Arguments:**
- `_center` - Center of search pos
- `_radius` - Search radius
- `_minBound` - Lower bound, will increase search radius until we have enough positions

**Return Value:** Array of waypoints on roads  

**Example:**
```

(begin example)
[] call mti_ai_fnc_getRoadWaypoints;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_localityChangedEH

**Description:** Handles changes in locality, attempts to fix issues with garrisons.  

**Arguments:**
- `_unit` - The unit
- `_isLocal` - If _unit is local

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_ai_fnc_localityChangedEH;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_patrolRoad

**Description:** Sets up a patrol plotted along roads, rather than random positions dotted around the AO.  

**Arguments:**
- `_group` - Group to set up for patrol
- `_waypoints` - Array of waypoints (i.e. roads) to use for the patrol setup
- `_patrolLength` - Length of the patrol path, array in format [min, max], default: [4, 8]

**Return Value:** :Nothing.  

**Example:**
```

(begin example)
[] call mti_ai_fnc_patrolRoad;
(end)

```

**Author:** Mokka 

## mti_ai_fnc_populateAO

**Description:** Quickly populates an entire AO according to a variety of parameters. Available factions have to be defined as subclasses of MTI_PopulateAO_Factions.  

**Arguments:**
- `_grpPrefix` - The prefix for the group IDs <STRING>
- `_center` - The center position of the area we want to populate <POSITION 3D>
- `_radius` - The radius of the area we want to populate <SCALAR>
- `_faction` - The faction which we want to use for populating the AO (subclass of MTI_PopulateAO_Factions) <STRING>
- `_args` _garr - Garrison Parameters <ARRAY OF [Group Count, Radius]>
- `_args` _inf - Infantry Parameters <ARRAY OF [Min Amount of Groups, Random Upper Bound of Groups]>
- `_args` _inf_aa - AA Parameters <ARRAY OF [Min Amount of Groups, Random Upper Bound of Groups]>
- `_args` _inf_at - AT Parameters <ARRAY OF [Min Amount of Groups, Random Upper Bound of Groups]>
- `_args` _sniper - Sniper Parameters <ARRAY OF [Min Amount of Groups, Random Upper Bound of Groups]>
- `_args` _veh_light - Light Vehicles Parameters <ARRAY OF [Min Amount of Vehicles, Random Upper Bound of Vehicles]>
- `_args` _veh_heavy - Heavy/Armoured Vehicle Parameters <ARRAY OF [Min Amount of Vehicles, Random Upper Bound of Vehicles]>
- `_args` _veh_random - Random Vehicles Parameters <ARRAY OF [Min Amount of Vehicles, Random Upper Bound of Vehicles]>
- `_args` _air - Air Assets Parameters <ARRAY OF [Min Amount of Aircraft, Random Upper Bound of Aircraft, Altitude]>
- `_patrolMethod` - Method to use for plotting the patrol paths <STRING, one of ["RANDOM", "ROADS"], default: "RANDOM">

**Return Value:** None  

**Example:**
```

(begin example)
[
"aurek",
[2955.43,6010.11,0],
500,
"MTI_CIS",
[5, 100],
[3, 5],
[2, 3],
[3, 4],
[2, 3],
[4, 5],
[2, 3],
[2, 3],
[1, 1, 100]
"RANDOM"
] call mti_ai_fnc_populateAO;
(end)

```

**Author:** MitchJC, Mokka 

