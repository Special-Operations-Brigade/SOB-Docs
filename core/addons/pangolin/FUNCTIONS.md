# Function Reference

## mti_pangolin_fnc_activateShield

**Description:** Handles shield activation  

**Arguments:**
- `_unit` - Unit whose shield to activate

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_pangolin_fnc_activateShield;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_canActivateShield

**Description:** Checks whether shield can be activated.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canActivateShield?  

**Example:**
```

(begin example)
[player] call mti_pangolin_fnc_canActivateShield;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_canDeactivateShield

**Description:** Checks whether shield can be deactivated.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** canDeactivateShield?  

**Example:**
```

(begin example)
[player] call mti_pangolin_fnc_canDeactivateShield;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_deactivateShield

**Description:** Takes care of shield deactivation.  

**Arguments:**
- `_unit` - Unit whose shield to deactivate

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_pangolin_fnc_deactivateShield;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_getShieldData

**Description:** Calculates shield data for the given unit  

**Arguments:**
- `_unit` - Unit to process

**Return Value:** Shield data in format [maxCharge, regenRate, regenAllowed, regenTimeoutMod]  

**Example:**
```

(begin example)
[ace_player] call mti_pangolin_fnc_getShieldData;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_hasShield

**Description:** Checks if given unit has equipped Pangolin compatible Shield.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** hasShield?  

**Example:**
```

(begin example)
[ACE_Player] call mti_pangolin_fnc_hasShield;
(end)

```

**Author:** Mokka 

## fnc_initUnit.sqf

No documentation available.

## fnc_localityChangedEH.sqf

No documentation available.

## mti_pangolin_fnc_onHit

**Description:** Handles onHit events for units.  

**Arguments:**
- `_unit` - passed by EH
- `_shooter` - passed by EH
- `_projectile` - passed by EH
- `_position` - passed by EH
- `_velocity` - passed by EH
- `_selection` - passed by EH
- `_ammo` - passed by EH
- `_vector` - passed by EH
- `_radius` - passed by EH
- `_surfaceType` - passed by EH
- `_isDirect` - passed by EH

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_pangolin_fnc_onHit;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_onHitLocal

**Description:** Locally handles onHit, deals with energy reduction, regen timeout etc  

**Arguments:**
- `_unit` - passed by EH
- `_shooter` - passed by EH
- `_projectile` - passed by EH
- `_position` - passed by EH
- `_velocity` - passed by EH
- `_selection` - passed by EH
- `_ammo` - passed by EH
- `_vector` - passed by EH
- `_radius` - passed by EH
- `_surfaceType` - passed by EH
- `_isDirect` - passed by EH

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_pangolin_fnc_onHitLocal;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_particleEffects

**Description:** Takes care of spawning various particle effects.  

**Arguments:**
- `_unit` - Unit to spawn the particles on
- `_type` - Type of particle effects to spawn (hit/breach)

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_pangolin_fnc_particleEffects;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_shieldPFH

**Description:** PFH that takes care of updating the given unit's shield status, regen and other things.  

**Arguments:**
- `_args` - Passed unit in array
- `_handle` - PFH handle

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_pangolin_fnc_shieldPFH;
(end)

```

**Author:** Mokka 

## mti_pangolin_fnc_woundHandler

**Description:** Custom ACE Medical wound handler for katarn shields.  

**Arguments:**
- See https://ace3.acemod.org/wiki/framework/medical-framework#44-wound-handler-function

**Return Value:** See https://ace3.acemod.org/wiki/framework/medical-framework#44-wound-handler-function  

**Example:**
```

(begin example)
[player, _allDamagesArray, "falling"] call mti_pangolin_fnc_woundHandler;
(end)

```

**Author:** DartRuffian */  params ["_unit", "_allDamages", "_typeOfDamage", "_ammo"]; TRACE_4("fnc_woundHandler",_unit,_allDamages,_typeOfDamage,_ammo);  /* Example output of _allDamages. Note that body parts are sorted by the damage they recieved. Values are: 0: Actual damage 1: Body part 2: Damage *before armor reduction* _allDamages = [ [1.06597, "Body", 17.0556], [1.06597, "LeftLeg", 17.0556], [1.06597, "RightLeg", 17.0556], [0.411558, "RightArm", 6.58492], [0.353302, "LeftArm", 5.65284], [0.189946, "Head", 2.27935], [0.0527364, "#structural", 0.210946] ] 

