# Function Reference

## fnc_addSelfDestruct.sqf

No documentation available.

## fnc_b2_boomer.sqf

No documentation available.

## fnc_b2_melee.sqf

No documentation available.

## mti_factions_cis_fnc_bx_disguiseAsBlufor

**Description:** Picks a random BLUFOR player and moves to a position near them. The unit will become passive and mimic the stance of the target and will stop following if the target dies or if the unit dies. The unit will also stop following if the target moves too far away or if the time limit is reached. After 30 seconds, the unit will stop following and will return to its original behaviour. (In this case, the unit will open fire on the target if it is still alive)  

**Arguments:**
- `_unit` - The unit that will disguise itself as a BLUFOR player

**Return Value:** Nothing  

**Example:**
```

(begin example)
[_unit] call mti_factions_cis_fnc_bx_disguiseAsBlufor
(end)

```

**Author:** Ramsey, Dart 

## mti_factions_cis_fnc_bx_looting

**Description:** Loots the body of a unit and gives the items to the unit. Basically forces players to have to chase their gear down if they get downed and get caught by the Mimic  

**Arguments:**
- `_unit` - The unit that will loot the body
- `_body` - The body that will be looted

**Return Value:** Nothing  

**Example:**
```

(begin example)
[_unit] call mti_factions_cis_fnc_bx_looting
(end)

```

**Author:** Ramsey 

## fnc_bx_melee.sqf

No documentation available.

## fnc_bx_mimic.sqf

No documentation available.

## mti_factions_cis_fnc_charge

**Description:** Unit plays an animation and charges at the target  

**Arguments:**
- `_unit` - The unit that will make the noise
- `_anim` - The animation that will be played

**Return Value:** Nothing  

**Example:**
```

(begin example)
[_unit] call mti_factions_cis_fnc_charge
(end)

```

**Author:** Ramsey, Dart 

## fnc_droidmelee.sqf

No documentation available.

## fnc_initB1Prototype.sqf

No documentation available.

## fnc_initProtoJammer.sqf

No documentation available.

## fnc_jetpackeffect_b2.sqf

No documentation available.

## fnc_pilotskill.sqf

No documentation available.

## fnc_revive.sqf

No documentation available.

## fnc_spawnSuitcaseNuke.sqf

No documentation available.

## fnc_speakerdroid.sqf

No documentation available.

