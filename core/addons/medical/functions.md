# Function Reference

## fnc_ace_onMedicationUsage.inc.sqf

No documentation available.

## fnc_ace_updateHeartRate.inc.sqf

No documentation available.

## mti_medical_fnc_addDamageRaw

**Description:** Adds raw damage (eg from hitPart) to given unit.  

**Arguments:**
- `_unit` - Unit to damage
- `_selection` - Bodypart/Bodypart to damage
- `_damage` - Raw damage

**Return Value:** None  

**Example:**
```

(begin example)
[player, "Head", 100] call mti_medical_fnc_addDamageRaw
(end)

```

**Author:** Mokka 

## mti_medical_fnc_bandage

**Description:** Bandages open wounds on the given body part of the patient.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated
- `_bandage` - (Type of) bandage used

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorTarget, "Head", "FieldDressing"] call mti_medical_fnc_bandage
(end)

```

**Author:** Glowbal, Mokka 

## mti_medical_fnc_defibrillate

**Description:** Handles defibrillation of target units  

**Arguments:**
- `_unit` - Unit to defibrillate
- `_shooter` - The unit that initiated the defib
- `_ammo` - Ammo used for defibrillation

**Return Value:** None  

**Example:**
```

(begin example)
[player, "MTI_defibrillator_ammo"] call mti_medical_fnc_defibrillate;
(end)

```

**Author:** Mokka */  params ["_unit", "_shooter", "_ammo"]; TRACE_3("params",_unit,_shooter,_ammo);  if !(local _unit) exitWith { ERROR_1("cannot defibrillate %1: not local",_unit) };  /* option A: _unit is in cardiac arrest and actually in need of shock - check chance if defibrillation successful and return heart rate - add lots of pain option B: _unit is NOT in cardiac arrest - always put _unit unconscious and add lots of pain - check for chance if defibrillation induces cardiac arrest instead 

## mti_medical_fnc_disposeBodybag

**Description:** Disposes of a bodybag.  

**Arguments:**
- `_target` 

**Return Value:** None  

**Example:**
```

(begin example)
[cursorObject] call mti_medical_fnc_disposeBodybag
(end)

```

**Author:** Mokka 

## mti_medical_fnc_getAverageDamage

**Description:** Returns average damage from array  

**Arguments:**
- `_damage` - Array of damage dealt to bodyparts in format [damage, bodypart]

**Return Value:** Average damage  

**Example:**
```

(begin example)
[...] call mti_medical_fnc_getAverageDamage
(end)

```

**Author:** Mokka 

## mti_medical_fnc_getBandageTime

**Description:** Returns adjusted bandage time based on most effective wound.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated
- `_bandage` - (Type of) bandage used

**Return Value:** _bandageTime in seconds  

**Example:**
```

(begin example)
[player, cursorTarget, "Head", "FieldDressing"] call mti_medical_fnc_getBandageTime
(end)

```

**Author:** SilentSpike, Mokka 

## mti_medical_fnc_handleInhalder

**Description:** Handles the usage of the MTI_Inhaler, triggering the local inhaler handling  

**Arguments:**
- `_medic` - The medic "treating" the patient
- `_patient` - The patient

**Return Value:** None  

**Example:**
```

(begin example)
[_medic, _patient] call mti_medical_fnc_handleInhalder;
(end)

```

**Author:** arcanist 

## mti_medical_fnc_handleInhaler

**Description:** Removes all lung damage wounds and resets the 'halothane' counters  

**Arguments:**
- `_medic` - The medic "treating" the patient
- `_patient` - The patient

**Return Value:** None  

**Example:**
```

(begin example)
[_medic, _patient] call mti_medical_fnc_handleInhaler;
(end)

```

**Author:** arcanist 

## fnc_initUnit.sqf

No documentation available.

## fnc_localityChangedEH.sqf

No documentation available.

## fnc_medicalHint.sqf

No documentation available.

## mti_medical_fnc_medication

**Description:** Administers medication to the patient on the given body bodypart.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated
- `_className` - (Type of) medication used
- `_itemUsed` - Obsolete, unused
- `_usedItem` - Used Item

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorObject, "RightArm", "Morphine", objNull, "ACE_morphine"] call mti_medical_fnc_medication
(end)

```

**Author:** Glowbal, mharis001, Mokka 

## mti_medical_fnc_medisensor

**Description:** Handles medisensor event triggering.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorTarget, "Head"] call mti_medical_fnc_medisensor
(end)

```

**Author:** Glowbal, Mokka 

## mti_medical_fnc_medisensorLocal

**Description:** Local callback for medisensor scan.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated

**Return Value:** None  

**Example:**
```

(begin example)
[player, cursorTarget, "Head"] call mti_medical_fnc_medisensorLocal
(end)

```

**Author:** Glowbal, Mokka 

## mti_medical_fnc_nevastrin8_handleEffect

**Description:** Handles effects of Nevastrin-8.  

**Arguments:**
- `_patient` - Affected unit
- `_concentration` - Concentration of Nevastrin-8

**Return Value:** None  

**Example:**
```

(begin example)
[player, 0.4] call mti_medical_fnc_nevastrin8_handleEffect
(end)

```

**Author:** Mokka 

## mti_medical_fnc_nevastrin8_overdose

**Description:** Handles Nevastrin-8 overdose.  

**Arguments:**
- `_target` - affected unit
- `_className` - type of treatment classname
- `_overdosedMedications` - array of overdosed medications

**Return Value:** None  

**Example:**
```

(begin example)
[player, "Nevastrin8", []] call mti_medical_fnc_nevastrin8_overdose
(end)

```

**Author:** Mokka 

## mti_medical_fnc_overdose_deraformine

**Description:** Handles deraformine overdose.  

**Arguments:**
- `_target` - affected unit
- `_className` - type of treatment classname
- `_overdosedMedications` - array of overdosed medications

**Return Value:** None  

**Example:**
```

(begin example)
[player, "Deraformine", []] call mti_medical_fnc_overdose_deraformine
(end)

```

**Author:** Mokka 

## mti_medical_fnc_overdose_pba

**Description:** Handles PBA overdose.  

**Arguments:**
- `_target` - affected unit
- `_className` - type of treatment classname
- `_overdosedMedications` - array of overdosed medications

**Return Value:** None  

**Example:**
```

(begin example)
[player, "PBA", []] call mti_medical_fnc_overdose_pba
(end)

```

**Author:** Mokka */  params ["_target", ["_className", "PBA"], ["_overdoseMedications", []]];  if (!GVAR(pba_od_enabled)) exitWith {};  // if patient is already in overdrive, exit now if (_target getVariable [QGVAR(pba_overdrive), false]) exitWith {}; if (_target getVariable ["ACE_isUnconscious", false]) exitWith {LOG("unit is unconscious, exiting pba overdrive")};  if (hasInterface) then { ["Entering PBA Overdrive!"] call ace_common_fnc_displayTextStructured; };  // soldier "overdrive" state // this is essentially done by temporarily stopping the vitals update routine _target setVariable ["ace_medical_vitals_lastTimeUpdated", CBA_missionTime + GVAR(pba_od_time), true];  // we also increase the damage threshold private _damThreshold = (_target getVariable ["ace_medical_damageThreshold", [ace_medical_AIDamageThreshold,ace_medical_playerDamageThreshold] select (isPlayer _target)]); _damThreshold = _damThreshold * GVAR(pba_pain_boost) * 5;  _target setVariable ["ace_medical_damageThreshold", _damThreshold, true];  _target setVariable [QGVAR(pba_overdrive), true];  if (hasInterface) then { [{["PBA Overdrive is about to expire!"] call ace_common_fnc_displayTextStructured;}, [], ((GVAR(pba_od_time) - 5) - random 5)] call CBA_fnc_waitAndExecute; };  // todo: patients should scream like there's no tomorrow /* class ace_fire_scream_1 { name = "ace_fire_scream1"; sound[] = {"\z\ace\addons\fire\sounds\scream1.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_2 { name = "ace_fire_scream2"; sound[] = {"\z\ace\addons\fire\sounds\scream2.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_3 { name = "ace_fire_scream3"; sound[] = {"\z\ace\addons\fire\sounds\scream3.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_4 { name = "ace_fire_scream4"; sound[] = {"\z\ace\addons\fire\sounds\scream4.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_5 { name = "ace_fire_scream5"; sound[] = {"\z\ace\addons\fire\sounds\scream5.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_6 { name = "ace_fire_scream6"; sound[] = {"\z\ace\addons\fire\sounds\scream6.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_7 { name = "ace_fire_scream7"; sound[] = {"\z\ace\addons\fire\sounds\scream7.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_8 { name = "ace_fire_scream8"; sound[] = {"\z\ace\addons\fire\sounds\scream8.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_9 { name = "ace_fire_scream9"; sound[] = {"\z\ace\addons\fire\sounds\scream9.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_10 { name = "ace_fire_scream10"; sound[] = {"\z\ace\addons\fire\sounds\scream10.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_11 { name = "ace_fire_scream11"; sound[] = {"\z\ace\addons\fire\sounds\scream11.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_12 { name = "ace_fire_scream12"; sound[] = {"\z\ace\addons\fire\sounds\scream12.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_13 { name = "ace_fire_scream13"; sound[] = {"\z\ace\addons\fire\sounds\scream13.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_14 { name = "ace_fire_scream14"; sound[] = {"\z\ace\addons\fire\sounds\scream14.ogg", "db + 8", 1}; titles[] = {}; }; class ace_fire_scream_15 { name = "ace_fire_scream15"; sound[] = {"\z\ace\addons\fire\sounds\scream15.ogg", "db + 8", 1}; titles[] = {}; }; 

## fnc_postBandageLungDamage.sqf

No documentation available.

## mti_medical_fnc_postInitDiary

**Description:** Adds the medical-related entries to the in-game manual.  

**Arguments:**
- `_medic` - treating unit
- `_patient` - treated patient
- `_bodyPart` - body part to be treated
- `_className` - (Type of) medication used
- `_itemUsed` - Obsolete, unused
- `_usedItem` - Used Item

**Return Value:** None  

**Example:**
```

(begin example)
call mti_medical_fnc_postInitDiary
(end)

```

**Author:** Glowbal, mharis001, Mokka 

## fnc_preBandageLungDamage.sqf

No documentation available.

## mti_medical_fnc_randomDamage

**Description:** Randomly damages the given unit based on various parameters.  

**Arguments:**
- `_target` - The unit to damage
- `_damage` - Damage dealt for **each invidual wound**, either as number or in format [min, mid, max]
- `_count` - Amount of wounds, either as number or in format [min, mid, max]
- `_forceUnconscious` - True to force unconsciousness (optional)
- `_forceCardiacArrest` - True to force cardia arrest (optional)
- `_hitSelections` - Array of selections to damage (optional)
- `_damageTypes` - Array of types of damage to deal (optional)

**Return Value:** None  

**Example:**
```

(begin example)
[player, [0,0.2,1], [2,6,10], true, false] call mti_medical_fnc_randomDamage
(end)

```

**Author:** Mokka 

## mti_medical_fnc_reorient

**Description:** "Reorients" a patient in order to quickly wake them up if vitals allow for that. Based on ACE Pharmacy's reorient action: https://github.com/mazinskihenry/aceP/blob/main/addons/circulation/functions/fnc_treatmentAdvanced_ReorientationLocal.sqf  

**Arguments:**
- `_medic` - The medic "treating" the patient
- `_patient` - The patient

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_medical_fnc_reorient;
(end)

```

**Author:** 2LT.Mazinski, modified by Mokka 

## mti_medical_fnc_resetState

**Description:** Forcefully resets medical status of target, fixes the "stuck at 30 HR" bug.  

**Arguments:**
- `_target` - Target to reset

**Return Value:** None  

**Example:**
```

(begin example)
[player] call mti_medical_fnc_resetState;
(end)

```

**Author:** Mokka 

## mti_medical_fnc_updateMedicationState

**Description:** Handles custom medication effects.  

**Arguments:**
- `_unit` - The unit to handle updates for, should be local player

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_Player] call mti_medical_fnc_updateMedicationState
(end)

```

**Author:** Mokka 

